## A classifier nobody saw coming


After several experiments, it was clear that something was happening: the model wasn't returning good predictions on the test data.

The team was tired and ready to get back to the drawing board to try and find a different approach to solve the problem, but Raelynn had an idea.

She took the training dataset, removed the target variable, and mixed it with all their available test data. She then created a new binary target and set it to 1 for every test sample and 0 for every training sample.

"Run a classifier on this dataset, and let me know how good the predictions are," she asked.

Her team seemed confused. What is Raelynn trying to do?


1. This classifier will estimate the performance of the team's model on unseen test data. It will help the team understand whether they are overfitting or underfitting the training data.

2. This classifier will turn the initial problem into a more straightforward approach that will serve as a baseline for the team to continue their work and find a better solution.

3. This classifier will estimate how different the training data is from the test data, potentially explaining why the team is struggling.

4. Combining the training and test data is never a good idea, so this classifier's results will not be valid.

## Answer
 
Raelynn's approach should be familiar if you have experience participating in Kaggle competitions.

Popular validation techniques, like cross-validation, allow you to test your models on unseen data, as long as that data comes from the same distribution as your training dataset. Unfortunately, that's not always the case, and even slight differences between the training and test data will considerably affect the result of your model.

Adversarial validation is a technique to estimate the degree of difference between your training and test data. The Kaggle Book introduces it as follows:

[adversarial validation] was long rumored among Kaggle participants and transmitted from team to team until it emerged publicly thanks to a post by Zygmunt Zając on his FastML blog.
Let's think about what Raelynn did. She created a new dataset by joining the training and test data. The target of that new dataset is a binary variable differentiating the training and test samples. She can determine how easy it's to separate both datasets by running a classifier on that new data.

Adversarial validation relies on computing the ROC-AUC, a graph showing the True Positive Rate and the False Positive Rate at different classification thresholds. The area under this curve (AUC) measures the model's performance. A perfect model will have an area of 1.0, while a model that only makes mistakes will have an area of 0.0.

If they run the classifier and the ROC-AUC is around 0.5, Raelynn will know that the training and test data are not easily distinguishable, which is good because it means the data comes from the same distribution. If the ROC-AUC is too high—closer to 1.0—the classifier can tell training and test data apart, which means they come from a different distribution.

Adversarial validation is a very clever technique. The result could help explain why the team is struggling and guide it on how to continue.

## Recommended reading

1. ["Adversarial validation"](https://blog.zakjost.com/post/adversarial_validation/) is a great introduction to adversarial validation.

2. Check ["What is Adversarial Validation?"](https://www.kaggle.com/code/carlmcbrideellis/what-is-adversarial-validation/notebook) for a discussion about this technique in Kaggle.

3. The [Kaggle Book](https://www.amazon.com/Data-Analysis-Machine-Learning-Kaggle/dp/1801817472?crid=2ZSVOUZJCXMO5&keywords=kaggle+book&qid=1650818962&sprefix=kaggle+book,aps,72&sr=8-3&linkCode=sl1&tag=bnomial-20&linkId=6cf9fd66daf5893153a64f03302971f7&language=en_US&ref_=as_li_ss_tl) is an amazing reference for those looking to participate in Kaggle.





