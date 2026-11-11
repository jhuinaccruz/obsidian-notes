>*`k`-means splits the data vertically — it can't find specific shapes of clusters*

__`k`-means assumes__: Clusters are spherical and similar-sized, failing for other non=spherical clusters as well as unequal cluster sizes

>*Both `k`-NN and `k`-means rely on distance. In high dimensions, distance becomes meaningless

>*In high dimensions, your "nearest" neighbors are nearly the same distance as your farthest neighbors.*

__When there are many features__:
- Get more data
- Reduce dimensions
- Feature scaling

__`k`-means++__: Works by initially spreading out its centroids
1. Pick the first center c_1 (at random from the data)
2. For each remaining center c_j
	- Compute `D(x)` for every point x
	- Pick the next center with probability proportional to `D(x)^2`
		- This method is biased towards points farther away
3. Run `k`-means from said points c

__StandardScaler__: Transforms each feature to have a mean of zero and a standard deviation of 1, calculated by
$$
z = \frac{x - \mu}{\sigma}
$$
However, this doesn't work when there are
- Outliers which distort normalized data
- Meaningful scales in raw units
- Non-normal distributions (StandardScaler assumes normal data)

>*Alternatives to StandardScaler are MinMaxScaler and RobustScaler*

__How to choose `k`__:
- Elbow: Plot the `k`-means inertia for different values of k, looking for the elbow or the point where adding more clusters stop helping/changing
- Silhouette: Measures the separation between clusters
	- Starts by calculating a value for each point as
$$
s = \frac{b-a}{\max(a,b)}
$$
		where `a` is the mean distance to points in the same cluster and `b` is the mean distance to points in the nearest other cluster
	- Plot said points and find the maximum
- Rand Index: When ground truth labels are available, you can measure how well clustering matches by comparing all points and seeing if they agree, calculated by
$$
\text{Rand Index} = \frac{a+b}{\binom{n}{2}}
$$
	where `a` is the pairs in the same cluster from both labels, and `b` is the pairs in different clusters from both labels
	- If the index has a value of one, it means there is a perfect agreement with its true labels