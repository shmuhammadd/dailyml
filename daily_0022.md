## Data augmentation on YouTube

Amara is writing a script for a YouTube video about data augmentation.

She wants to cover some of the most critical aspects of using the technique on a dataset of pictures.

Here is Amara's list with the key takeaways she wants to leave for her audience.

Which of the following statements would you let Amara share with her audience?

1. Using data augmentation, we can artificially increase the amount of data by generating new samples from existing data.

2. Generative Adversarial Networks (GANs) and Style Transfer are advanced techniques that can help with data augmentation.

3. Data augmentation has a regularization effect when used to increase the amount of data before training a model.

4. Data augmentation helps remove the inherent bias present in the original data.

## Answer

The first choice is the definition of data augmentation: we can augment the size of the dataset by generating new samples from our existing data.

Generative Adversarial Networks (GANs) are a popular way to generate synthetic images. We can also use Style Transfer to create new data based on existing samples.

The third choice is also correct: Data augmentation has a regularization effect. Increasing the training data through data augmentation decreases the model's variance and, in turn, increases the model's generalization ability.

Finally, when we use data augmentation, we will propagate any of the biases already present in the original data. Remember that data augmentation uses existing data as the foundation for any new data, so any problems with the original dataset will persist on the augmented one. Therefore, the fourth choice is incorrect.

## Recommended reading

1. ["STaDA: Style Transfer as Data Augmentation"](https://arxiv.org/abs/1909.01056) is a paper illustrating how to use Style Transfer for data augmentation.

2. ["The Essential Guide to Data Augmentation in Deep Learning"](https://www.v7labs.com/blog/data-augmentation-guide) is an excellent article discussing data augmentation in detail.

3. Check ["Test-Time augmentation"](https://articles.bnomial.com/test-time-augmentation) for an introduction that will help you make better predictions with your machine learning model.
