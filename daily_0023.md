# High-speed train distance

Ladybug and Lemon are working on a machine learning system to control high-speed trains.

They decided to use k-Nearest Neighbors in one of the system modules but had to stop when they realized they had to work with categorical data.
After thinking about it, they used one-hot encoding to convert the data into a vector of zeros and ones. All left was to pick the appropriate distance measure to compute the similarity between two one-hot-encoded columns.

Which of the following is the appropriate measure to compute the distance between two one-hot encoded vectors?

- Minkowski distance
- Euclidean distance
- Manhattan distance
- Hamming distance

## Answer

The Minkowski distance is a generalization of the Euclidean and Manhattan distances. Both of these work with real-value vectors, but the Euclidean distance is the shortest path between objects, while the Manhattan distance is the rectilinear distance between them. Using the Minkowski distance, we can control which approach to use depending on the data.

Ladybug and Lemon, however, need the distance between categorical features encoded using one-hot encoding.

The Hamming distance computes the distance between two binary vectors. It's the ideal function for one-hot encoded vectors.

## Recommended reading

1. ["4 Distance Measures for Machine Learning"](https://machinelearningmastery.com/distance-measures-for-machine-learning/) for a complete explanation of these four distance measures.

2. ["Five Common Distance Measures in Data Science With Formulas and Examples"](https://regenerativetoday.com/five-common-distance-measures-in-data-science-with-formulas-and-examples/) is a deeper dive into these distance measures.
