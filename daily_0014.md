## Inattentive drivers

Summer started working for Tesla.

Her first assignment is to build a model that will use the camera in the cabin to detect whether drivers are paying attention or are too tired.

The system's ultimate goal is to provide audio and visual alerts to help drivers stay safe. Tesla hopes this feature will significantly decrease the number of accidents.

Before the work starts, Summer wants to decide which of the following will be the best way to evaluate the model:


1. Summer should use the recall of the model, while keeping an eye on its precision.

2. Summer should use the accuracy of the model.

3. Summer should use the precision of the model, while keeping an eye on its recall.

4. Summer should use the training loss of the model.


## Answer

There will be many more situations where Summer's system will find that the driver is correctly paying attention than not. If she uses the accuracy of her model as the evaluation metric, she could end up with a struggling model that still shows high accuracy. Remember that accuracy is not a good metric when facing an imbalanced problem. You can achieve very high accuracy even with a model that does nothing useful.

Let's assume Summer's model misses most cases where the driver is tired and not paying attention. Think of a model that detects a single issue correctly, doesn't have any false positives, and ignores all other dangerous situations. That model will have perfect precision, but it won't help much in reducing traffic accidents because it doesn't detect every problematic situation. Precision is not a good metric for this problem.

The training loss of the model won't help Summer either. We use the loss to determine whether the model learned, but it doesn't tell us anything about the capacity of the model to detect inattentive drivers. Like accuracy, we could have a low loss model that doesn't do well with problematic situations.

Summer should focus on the recall of her model while keeping an eye on its precision. A high recall will ensure that Summer's model detects as many problematic situations as possible.


## Recommended reading

1. Check ["When accuracy doesn't help"](https://articles.bnomial.com/when-accuracy-doesnt-help) for an introduction to precision, recall, and f1-score metrics to measure a machine learning model's performance.

2. Check ["Confusion Matrix"](https://articles.bnomial.com/confusion-matrix) for a full explanation of how a confusion matrix works and how you can use them as part of your work.

4. [Precision and recall](https://en.wikipedia.org/wiki/Precision_and_recall)