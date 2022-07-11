## Pictures and tensors

I've been teaching a friend a little bit of computer vision.

Well, I'll be honest, I'm focusing directly on deep learning and how to use pre-trained models to tell cat pictures apart from dog pictures.

We have a dataset of 1,000 color pictures of size 512 x 512. Five hundred of those are images of cats, and the other half are images of dogs.

Soon after we started looking into the problem, he asked a question that I hadn't thought about in a long time.

What's the correct shape of a tensor capable of storing all of this data at once?


1. We can store it in a tensor of shape (1000, 512, 512)

2. We can store it in a tensor of shape (512, 512, 3)

3. We can store it in a tensor of shape (1000, 512, 512, 3)

4. We can store it in a tensor of shape (500, 512, 512, 1)


## Solution

When working with images, we need to store three components: the height, the width, and the color depth. Color images have three color channels (one for red, one for green, and one for blue), and grayscale images have a single color channel.

In other words, assuming our pictures are of size 512 x 512, we need to store the 3 RGB values for each pixel in the image, so we need a tensor of shape (512, 512, 3). If we don't care about colors, we could keep every pixel of a single image in a tensor of shape (512, 512).

But even when working with grayscale images, we always add a dimension to store the color depth by convention. That's nice because we can use the same structure for grayscale and color images. If we don't care about color, we could store one picture in a (512, 512, 1) tensor. Since we are working with color pictures, our tensor will be (512, 512, 3) to accommodate the three channels.

Great! So far, we know how to store a single color picture of size 512 x 512. How about keeping 1,000 of them? We need another dimension: (1000, 512, 512, 3).

The order I chose for each dimension is intentional. By convention, we structure tensors that hold images the following way: (samples, height, width, channels). There's a different convention where channels go in front of the dimensions of the images, but most people use them at the end.

## Recommended reading

1. Deep Learning with Python, Second Edition covers the topic of tensors really well.
2. Check "A Gentle Introduction to Tensors for Machine Learning with NumPy" for a quick introduction to tensors and practical code.
