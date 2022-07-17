## Illegitimate traffic

Rachel's team built a decision tree model to determine illegitimate requests to their application.

While working on a prototype with fake data, everything worked as expected. But as soon as they tried to use real traffic, it was clear that the problem was more complex than expected: most requests were legitimate, and the decision tree had difficulty finding the problematic ones.

Rachel still thought a decision tree was the right approach, so she decided to find a solution.

What's the appropriate next step to solving this problem?


1. Rachel should balance the dataset before training the decision tree. After doing this, she can fit the model again.

2. Rachel should fit the decision tree and then scale the model's results appropriately, following the weight of each class.

3. Rachel should fit the decision tree on each class separately—illegitimate and legitimate requests. Then, she should combine the results proportionally to the weight of each class.

4. Rachel cannot make a decision tree work with an imbalanced dataset. She should pick a different model.
You were really close!


## Answer 

Let's imagine there's no problem with 99% of the traffic. If Rachel's model classifies every request as legitimate, it will have 99% accuracy. Unfortunately, this is useless, so Rachel needs to find a different solution.

If Rachel balances the dataset before fitting the decision tree, she will have a better chance. There are many different strategies to balance a dataset, and they all aim to amplify the impact of the minority class so the model can better predict it.

The second choice is not a solution. It doesn't make sense to scale the model results following the weight of the classes. Something similar happens with the third choice: fitting the decision tree on each separate class doesn't make sense either.

Finally, the fourth choice argues that decision trees don't work with imbalanced datasets, which is not true. Besides balancing the dataset, Rachel could use each class' weight to penalize the model more harshly when it misses illegitimate requests.

## Recommended reading

1. Check ["Random Oversampling and Undersampling for Imbalanced Classification"](https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/) for an introduction to oversampling and undersampling.

2. ["Failure of Classification Accuracy for Imbalanced Class Distributions"](https://machinelearningmastery.com/failure-of-accuracy-for-imbalanced-class-distributions/) covers the problem of using accuracy as the metric in imbalanced classification problems.

3. ["Learning from imbalanced data"](https://www.jeremyjordan.me/imbalanced-data/) discusses a number of considerations and techniques for dealing with imbalanced data.
