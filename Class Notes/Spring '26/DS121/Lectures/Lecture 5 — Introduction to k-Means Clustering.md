__Clustering__: Grouping similar data points together based on similarity or lack thereof (dissimilarity)

__Dissimilarity__: Can be calculated as
- A distance function denoted as
$$
d(x, y)
$$
	and satisfies the following properties
	- Zero distance means two points are identical
	- Distances are non-negative
	- Symmetry
$$
d(x,y) = d(y,x)
$$
	- Triangle inequality:
$$
d(x,z) ≤ d(x,y) + d(y,z)
$$

__Cosine Similarity__: Denoted and calculated as
$$
\cos(\theta_{x,y}) = \frac{x^\top y}{|x||y|}
$$
- where `x` and `y` are two vectors of different lengths being compared on their direction rather than their magnitude
- can be converted to dissimilarity as
$$
1 - \cos{\theta}
$$

__Partitional Clustering__: Each points to exactly one cluster, and every point is assigned

__Centroid__: The center/mean of a set of vectors `x` (also known as the center of mass of the points) denoted and calculated as
$$
\bar{x} = \frac{1}{n}\sum^n_{i=1}x_i
$$
__K-Means__: Given `n` data points and a number of clusters `k`, find `k` centroids that minimize the cost function
$$
\text{Cost} = \sum_{i = 1}^n = ||x_i - c_{j(i)}||
$$
where `j_i` is the index of the centroid closest to x_i
1. Initialize: Pick `k` starting centers (randomly or otherwise)
2. Assign: Put each point in the cluster of its nearest center
3. Update: Recompute each center as the centroid of its cluster
4. Repeat steps 2-3 until nothing changes

>*K-Means minimizes the total squared distance from each point to its nearest center*