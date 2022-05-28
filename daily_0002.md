
## Question on Loss Function: Choosing a loss function

Martin met an old friend for a coffee.

Ariana and Zach need to compute how different their model predictions are from the expected results.
 
They have been going back and forth between two different loss functions: Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE). These two metrics have properties that will shine depending on the problem they want to solve.
 
Which of the following is the correct way to think about these two metrics?
 
 1. RMSE penalizes larger differences between the predictions and the expected results.
 2. RMSE is significantly faster to compute than MAE.
 3. From both metrics, RMSE is the only one indifferent to the direction of the error.
 4. From both metrics, MAE is the only one indifferent to the direction of the error

## Answer

Almost there!
When we train a machine learning model, we need to compute how different our predictions are from the expected results. For example, if we predict a house's price as $150,000, but the correct answer is $200,000, our "error" is $50,000.

There are multiple ways we can compute this error, but two common choices are:

RMSE — Root Mean Squared Error
MAE — Mean Absolute Error
These have different properties that will shine depending on the problem we want to solve. Remember that the optimizer will use this error to adjust the model. We want to set up the right incentives so the model learns appropriately.

Let's focus on a critical difference between these two metrics. Remember the "squared" portion of the RMSE? You are "squaring" the difference between the prediction and the expected value. Why is this relevant?

Squaring the difference "penalizes" larger values. If you expect a prediction to be 2, but you get 10, using RMSE, the error will be (2 - 10)² = 64. However, if you get 5, the error will be (2 - 5)² = 9. Do you see how it penalizes larger errors?

MAE doesn't have the same property. The error increases proportionally with the difference between predictions and target values. Understanding this is important to decide which metric is better for each case.

Predicting a house's price is a good example where $10,000 off is twice as bad as $5,000. We don't necessarily need to rely on RMSE here, and MAE may be all we need.

But predicting the pressure of a tank may work differently. While 5 psi off may be within the expected range, 10 psi off may be a complete disaster. Here "10" is much worse than just two times "5", so RMSE may be a better solution.

Looking at the first choice, we already know it is a correct answer. RMSE penalizes larger differences between predictions and expected results.

Looking at both formulas, RMSE has extra squaring and root squaring operations, so it can't be faster to compute than MAE. The second choice is, therefore, not correct.

The third choice states that RSME is indifferent to the direction of the error, but MAE isn't. This is not correct: MAE uses the absolute value of the error, so both negative and positive values will end up being the same.

The fourth choice states that MAE is indifferent to the direction of the error, but RMSE isn't. This is not correct either: RMSE squares the error, so both negative and positive values will be th∑e same.

In summary, the only correct answer to this question is the first choice.

## Recommended reading

1. ["RMSE vs MAE, which should I use?"](https://stephenallwright.com/rmse-vs-mae/) this is a great summary by Stephen Allwright about the properties of these two functions and how you should think about them.
2.["Root-mean-square deviation"](https://en.wikipedia.org/wiki/Root-mean-square_deviation) is the Wikipedia page covering RMSE.
3. [Mean absolute error"](https://en.wikipedia.org/wiki/Mean_absolute_error) is the Wikipedia page covering MAE.
4. [MAE and RMSE which is better?](https://medium.com/human-in-a-machine-world/mae-and-rmse-which-metric-is-better-e60ac3bde13d)
5. [MAE vs RSME](http://www.eumetrain.org/data/4/451/english/msg/ver_cont_var/uos3/uos3_ko1.htm)

