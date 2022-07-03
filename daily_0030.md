## Rolling down the hill

Understanding how deep neural networks work is essential for anyone trying to become proficient at using them.

We don't know precisely how deep neural networks break down an image and distribute different patterns across the layers, but we have some general ideas.

Imagine that we are working with pictures of happy kitties. Which of the following statements reasonably simplifies how the network works?

1. The deeper layers of a neural network compute more complex features than earlier layers.

2. The earlier layers of a neural network compute more complex features than deeper layers.

3. The complexity of the features computed by the neural network layers is proportionally distributed among all layers.

4. The complexity of the features computed by the neural network layers has no relationship with the layer's position.


## Answer

Focus on a picture of a kitty. You'll see the eyes, nose, mouth, ears, fur, and other characteristics. Notice how groups of pixels form edges, shapes, and the rest of the cat's features.

A reasonable explanation for how a neural network works is to assume that earlier layers focus on detecting more basic features, like edges and shapes of the image. Later layers could use these earlier pieces to form more recognizable shapes like the eyes and nose of the cat.

While the network deals with pixels early on, the deeper we go into it, the more it will work with complete patterns until it reaches the output layer.

## Recommended reading

1. ["But what is a neural network?"](https://www.youtube.com/watch?v=aircAruvnKk) is Grant Sanderson's introduction to neural networks on YouTube. Highly recommended!
• [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/index.html) is a free online book written by Michael Nielsen.
