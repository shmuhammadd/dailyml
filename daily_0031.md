## Euclidean distance

Many machine learning algorithms need a way to measure the similarity between observations.

For example, when using an algorithm like K-Means, we need a way to determine how close different samples are in our dataset before deciding whether those samples belong in the same cluster.

There are different metrics to compute the distance between observations, and one of the most popular ones is the Euclidean distance.

From the following list, select every correct statement about the Euclidean distance.


1. The Euclidean distance is a way to compute the distance between two points in two-dimensional spaces. The Euclidean distance doesn't work in multidimensional spaces.

2. The Euclidean distance between two points does not depend on which of the two points is the start and which is the destination. In other words, the distance between p and q is the same as between q and p.

3. The Euclidean distance between two distinct points is always positive.

4. Traveling from a point p to a point q via a point r cannot be any shorter than traveling directly from p to q.


## Answer

We can use the Euclidean distance in one or more dimensions. For example, in a line, the distance between two points is the numerical difference between their coordinates. In a plane, the distance is the Pythagorean distance.

But can we use it in multidimensional spaces?

The answer is yes; the Euclidean distance works in multidimensional spaces. Intuitively, this should make sense because we can use it as the metric to compute the distance between multi-feature observations in our dataset. Therefore, the first choice is incorrect.

The distance from a point p to another point q is the same regardless of whether we start from p or q. This distance is always a positive value as long as p and q are different points. If p and q are the same point, the distance is 0.

In the Euclidean plane, the distance between any two distant points is the length of the line segment joining them. So this segment joining points p and q can't be any shorter, regardless of whether we get from p to q via a third point r.

In summary, the last three choices are correct.


## Recommended reading


Recommended reading

1. Check ["Euclidean Distance In 'n'-Dimensional Space"](https://hlab.stanford.edu/brian/euclidean_distance_in.html) for a summary and visualization of how the Euclidean distance works in multi-dimensional spaces.

2. ["Euclidean distance"]((https://en.wikipedia.org/wiki/Euclidean_distance) and ["Euclidean space"]((https://en.wikipedia.org/wiki/Euclidean_space) are Wikipedia articles that will help with this topic.

3. [9 Distance Measures in Data Science](https://towardsdatascience.com/9-distance-measures-in-data-science-918109d069fa)

4. [4 Distance Measures for Machine Learning](https://machinelearningmastery.com/distance-measures-for-machine-learning/)

5. [Why is Euclidean distance not a good metric in high dimensions?](https://stats.stackexchange.com/questions/99171/why-is-euclidean-distance-not-a-good-metric-in-high-dimensions) 

 
 
