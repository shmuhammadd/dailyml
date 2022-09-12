## Broken bottles

Parker works at a drink factory concerned with classifying defects as bottles come out of the line. She built a computer vision model to classify bottles into three classes: "ready," "almost ready," and "waste."

Most of the bottles that come out are "ready," and there are only a few samples that classify as "almost ready" or "waste." Parker is very aware of this imbalance.

The factory uses Parker's model to reduce the number of defective bottles that ship to customers (any bottle that's not "ready" is defective.) They consider each of the three classes equally important and wants to ensure the evaluation process reflects that.

Which metric should Parker use to evaluate her model?

1. The accuracy of the model.
2. The Micro-average F1-Score of the model.
3. The Macro-average F1-Score of the model.
4. The Weighted F1-Score of the model.

## Answer

Since Parker is working on a very imbalanced problem, she shouldn't use accuracy to evaluate her model's quality. If 99% of the bottles are "ready," Parker's model will have 99% accuracy, even if she ignores every sample belonging to the other two classes.

The F1-Score is helpful in these situations, but it depends on how we compute it in a multi-class classification problem.

The Micro-average F1-Score calculates the proportion of correctly classified samples out of all instances, the same as the model's accuracy definition. Therefore, if we use the Micro-average F1-Score, we'll have the same issue we see when using accuracy.

The Weighted F1-Score scales the individual F1-Score of each class. This method favors the majority classes, which in Parker's case are the bottles classified as "ready." The factory considers every category equally important, and that's why the Weighted F1-Score is not the correct answer.

Finally, the Macro-average F1-Score penalizes the model equally for any class that doesn't perform well, regardless of its importance or how many support samples it has. This metric is the correct answer where every category is important, irrespective of how many instances we have in the dataset. This is the metric that Parker should use to evaluate her model.


## Recommended reading


1. Check ["When accuracy doesn't help"](https://articles.bnomial.com/when-accuracy-doesnt-help) for an introduction to precision, recall, and f1-score metrics to measure a machine learning model's performance.

2. ["Micro, Macro & Weighted Averages of F1 Score, Clearly Explained"](https://towardsdatascience.com/micro-macro-weighted-averages-of-f1-score-clearly-explained-b603420b292f) is a great article covering how to compute a global F1-Score metric in multi-class classification problem.

3. Check ["Confusion Matrix"](https://articles.bnomial.com/confusion-matrix) for a full explanation of how a confusion matrix works and how you can use them as part of your work.