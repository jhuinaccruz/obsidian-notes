__Clustering__: Partitioning data points into groups of similar ones
- Examples include k-center/means/median, hierarchical agglomerative clustering
- Near(est)-Neighbor Search: Find a point similar in a query in the database

__Data Set__: A collection of points in some space with a related notion of distance or similarity

>*Your input for the* closest pair of points *problem is a set P of n points in R^2*

__The goal of a Closest Pair of Points problem is__: Minimize the Euclidean L_2 distance
$$
d(p_1, p_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
$$
- The naive solution runs in `O(n^2)`, where all points end up being compared