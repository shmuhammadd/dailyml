## Output activation

If you want to learn something new, the best strategy is to practice it until things start making sense.

Alina wanted to do that. She wasn't confident in understanding classification problems and neural networks, so she tried a few ideas. She implemented a neural network from scratch, including different loss functions and the backpropagation process.

It was time to look into activation functions for the output layer of the network, and here is where Alina had the most questions.

Which of the following activation functions could work in the output layer of a neural network that solves a classification problem?


1. Rectifier linear activation function (ReLU)
2. Tanh
3. f(x) = 1 if x > 0 else 0
4. f(x) = 0 if x > 0 else 1

## Answer

Whenever we are working on a classification task, we need the network to output a finite range of values. Alina can use any of the choices on this question except ReLU.

ReLU returns its same input if positive or zero otherwise. Assuming the input to an output layer using ReLU is a positive value, the result will be the same, which won't help Alina classify the sample.

The other three choices will help Alina classify images in one of two classes. Tanh will return a result between -1 and 1, so she can decide whether the image belongs to one class if the output is negative or the other if positive. The other two functions return a discrete value depending on their input.

Notice that, although not strictly required, we usually prefer activation functions to be differentiable. While tanh is differentiable, the other three options aren't. However, just like ReLU, this question's third and fourth functions are differentiable except at x = 0, which is enough for them to work without too much trouble.



## Recommended reading

1. "A Gentle Introduction to the Rectified Linear Unit (ReLU)"](https://machinelearningmastery.com/rectified-linear-activation-function-for-deep-learning-neural-networks) is a great introduction to ReLU.

2. Check out ["Neural Network Binary Classification With Tanh Output Activation"](https://jamesmccaffrey.wordpress.com/2020/11/02/neural-network-binary-classification-with-tanh-output-activation/) for the source code of a binary classifier using a tanh activation function.