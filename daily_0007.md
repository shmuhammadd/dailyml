##  Tensors and trolls

Yesterday was Samantha's first day, and she started learning how to use a deep learning library.

Unsurprisingly, "Tensors" was the first concept she needed to understand. Samantha read everything she could about them and is now ready to write a short article with everything she learned.

But she knows that making a mistake online will bring people out of the woodwork to troll her forever.

Samantha has to get this right. Which of the following are accurate descriptions of tensors of different ranks?


1. A vector that contains only one number is called a "scalar" or a rank-0 tensor. An example of a scalar is any numeric value like a person's age or today's temperature.

2. An array of numbers is called a "vector" or a rank-1 tensor. An example of a vector is an array containing the age of every person represented in a dataset.

3. An array with two dimensions is called a matrix or a rank-2 tensor. An example is an array containing the age and the sex of every person represented in a dataset.

4. An array with three dimensions is a rank-3 tensor. An example is a 3D array containing the information of an image: its width, height, and the number of channels.
There you go!

## Answer


The rank of a tensor refers to its number of axes—or dimensions. For example:

The rank of a scalar is 0.
The rank of a vector is 1.
The rank of a matrix is 2.
The rank of a 3D tensor is 3.

A scalar, or 0D tensor, has a rank of 0 and contains a single number. These are also called "0-dimensional tensors." Therefore, the first choice is correct.

A vector, or 1D tensor, has a rank of 1 and represents an array of numbers. Therefore, the second choice is also correct.

A matrix, or 2D tensor, has a rank of 2 and represents an array of vectors. We refer to the two axes of a matrix as "rows" and "columns." Therefore, the third choice is also correct.

You can obtain higher-dimensional tensors (3D, 4D, etc.) by packing lower-dimensional tensors in an array. For example, packing a 2D tensor in an array gives you a 3D tensor.

For example, to store a color image, we need three dimensions: one representing the image's width, another representing the height, and a final dimension for the color channels. Assuming we have three channels (red, blue, and green), you can think of having three different matrices, each containing the pixels for each one of the channels. Therefore, the fourth choice is also correct.


## Recommended reading

1. [Deep Learning with Python, Second Edition](https://www.amazon.com/gp/product/1617296864/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1617296864&linkCode=as2&tag=bnomial-20&linkId=14cba0ab0bb2afeafebfaa399fd2628f) covers the topic of tensors really well.

2. Check ["A Gentle Introduction to Tensors for Machine Learning with NumPy"](https://machinelearningmastery.com/introduction-to-tensors-for-machine-learning/) for a quick introduction to tensors and practical code.

