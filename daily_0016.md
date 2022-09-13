## Job descriptions

Millie finished collecting a dataset with job descriptions and their corresponding salary ranges.

Unfortunately, there's a lot of noise in the dataset, and Millie is not sure how to proceed.

A colleague recommended bagging, but Millie is unfamiliar with this technique. She looked into it and came up with a few questions.

Select every statement below that's correct about bagging:

1. Bagging is an effective technique to reduce the variance of a model.

2. Bagging is an effective technique to reduce the bias of a model.

3. Bagging trains a group of models, each using a subset of data selected randomly without replacement from the original dataset.

4. Bagging trains a group of models, each using a subset of data selected randomly with replacement from the original dataset.

## Answer

Bagging is a popular ensemble learning technique.

Bagging trains a group of models in parallel and independently from each other. Each model uses a subset of the data randomly selected with replacement from the original dataset. That's why bagging is also known as "bootstrap aggregating:" because it draws bootstrap samples from the training dataset.

Bagging is an excellent approach to reducing the variance of a model, but it doesn't help reduce the bias. That's why we often use it with low-bias models, like unpruned decision trees. Here is a relevant quote from "What is bagging?" about how it helps reduce the variance of a model:

Bagging can reduce the variance within a learning algorithm. This is particularly helpful with high-dimensional data, where missing values can lead to higher variance, making it more prone to overfitting and preventing accurate generalization to new datasets.
In summary, the first and fourth choices answer this question correctly.


## Recommended reading

Recommended reading

1. Check IBM's ["What's Bagging?"](https://www.ibm.com/cloud/learn/bagging) summary for a detailed explanation of this technique.

2. [What is the difference between Bagging and Boosting?](https://quantdare.com/what-is-the-difference-between-bagging-and-boosting/) is a great summary of bagging and boosting and their advantages and disadvantages.