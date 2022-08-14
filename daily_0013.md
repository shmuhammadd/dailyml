## Data splits

Eleanor had just started her machine learning course. Over the first few lessons, the class covered working with data and preparing it to train a model.

Unfortunately, the course was somewhat prescriptive and rushed. Although it covered the need to split the data into train, validation, and test sets, it didn't spend any time explaining the reasons.

Eleanor knows that making progress without understanding the why behind every decision is not good.

Select every choice from the following statements that explain why we split a dataset before training a model?


1. Having independent datasets can prevent the model from underfitting.

2. Having independent datasets can prevent the model from overfitting.

3. Having independent datasets can make the training process faster.

3. Having independent datasets can accurately evaluate the model's performance.

## Answer


Imagine teaching a math class, and it's time to evaluate your students. You decide to leave them 100 exercises as their homework. These problems cover the content they need to master for acing the exam.

How can you design an exam that effectively identifies those who learned the material?

Let's assume you pick 20 of the same homework exercises and use them in your test. This strategy might result in some false positives: students who memorize the solutions to their homework may get a high score, although they don't necessarily know how to reason. In machine learning, we call this "overfitting."

To ensure students don't overfit to their training exercises, you don't want to use the same homework to test their knowledge. Instead, you want to find new problems that evaluate the same material but are different enough to force the students to show their skills.

We want to do the same when training machine learning models. If we only evaluate our work in the same data we use to train the model, we might overfit and have a model that isn't capable of generalizing to different data. In other words, the model may "memorize" the training data and learn to return excellent predictions when tested.

If we split the dataset and leave a portion of it to evaluate how much the model learned, we will ensure that overfit won't happen. Therefore, the second and fourth choices are correct: we can accurately assess the model's performance and avoid overfitting.

Getting back to the previous analogy, those students that can't solve the homework in the first place are underfitting. Underfitting happens when the model cannot learn the training data, so we don't need separate splits to detect underfitting. The training data is enough, so the first choice is not correct.

Finally, we don't split the data to improve the training process speed; we do it to evaluate its performance accurately.

## Recommended reading

1. ["Overfitting and Underfitting With Machine Learning Algorithms"](https://machinelearningmastery.com/overfitting-and-underfitting-with-machine-learning-algorithms/) is an excellent article about overfitting, underfitting, and their differences.

2. Check out ["Overfitting vs. Underfitting in Machine Learning: Everything You Need to Know"](https://neptune.ai/blog/overfitting-vs-underfitting-in-machine-learning) for another take on the same topic.

3. ["Train, Validation, Test Split for Machine Learning"](https://blog.roboflow.com/train-test-split/) goes into detail about the importance of each split.


