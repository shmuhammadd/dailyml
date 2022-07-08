## What model is she using? 

Alicia's team was having a hard time with their model.

Everything was going according to plan until the customer showed up with more data.

The team decided to retrain the model with the new data, and to their surprise, they discovered that the test error increased significantly during evaluation.

They kept training the model with different portions of the data and testing it with their test dataset. Still, none of the models was good enough: the model was learning something different depending on the portion of the data that Alicia's team used.

If you were to guess the model that Alicia's team is building, which of the following would be your picks?


1.Alicia is probably using a Linear Regression model.

2. Alicia is probably using a Logistic Regression model.

3. Alicia is probably using a k-Nearest Neighbors model.

4. Alicia is probably using a Decision Tree model.


# Answer

The problem description has an essential clue: The testing error is high as we use different data portions to train the model. The various models can't generalize.

High-variance models usually suffer from this problem.

"Variance is the amount that the estimate of the target function will change if different training data was used."

As we change the training data, a low-variance model should still return good predictions on the test data, but Alice's model doesn't.

Often, linear models are low-variance, and nonlinear models are high-variance. This means that Alicia is probably using a k-Nearest Neighbors or a Decision Tree model since they are high-variance models.

# 
Recommended reading

1. Here is Jason Brownlee's article I mentioned before: ["Gentle Introduction to the Bias-Variance Trade-Off](https://machinelearningmastery.com/gentle-introduction-to-the-bias-variance-trade-off-in-machine-learning/) in Machine Learning".

2. The Wikipedia page on bias and variance is also a good resource: ["Bias–variance tradeoff"](https://en.wikipedia.org/wiki/Bias–variance_tradeoff).

3. [Theoretical ML Interview Question: Bias-Variance Tradeoff](https://www.kaggle.com/general/198890)

4. [What is Bias, Variance and Under fitting, Over fitting](https://www.kaggle.com/general/219378)


