__K-Means Clustering__: 
$$
\sum_{x\in S}\min_{q\in Q}(dist(x,q))^2
$$
where
- `S` is a set of points
- `k` is an integer greater than one
- `Q` is a set that minimizes

__K-Median Clustering__:
$$
\sum_{x \in S} \min_{q \in Q} dist(x, q)
$$
__K-Center Clustering__: Cover all the points in the dataset with `k` identical balls of radius as small as possible
$$
\max_{x \in S} \min_{q \in Q}dist(x,q)
$$

__Approximation Algorithms__: Greedy approaches that produce a "sufficiently good" approximation
- Multiplicative a-approximation
$$
X ≤ \alpha{X_*}
$$
	where
	- X: The value to be minimized
	- X_\*: Optimum value
