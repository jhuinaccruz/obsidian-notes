>*A coordinate system gives a unique name to each point in a vector space*

__Unique Representation Theorem__: Given a basis for vector space $H$, each vector in $H$ can be written in only one way as a linear combination of the basis vectors


__Coordinate Vector__ ($B$-coordinate vector): $$B = \{b_1,...,b_p\} \text{ for } H \in \mathbb{R}^n.\ \exists [x]_B = \begin{bmatrix}c_1 \\ ... \\ c_p \end{bmatrix} \implies \vec{x} \in H = c_1b_1 + ... + c_pb_p$$
- $B$ is the basis for vector space $H$
- $\vec{x}$ can be any given vector in $H$
- $[x]_b$ is called the coordinate vector of $\vec{x}$ relative to $B$ (or simply the $B$-coordinate vector of $\vec{x}$)


>Coordinate axes do not need to be perpendicular to one another.

__Orthogonal Set__: A set of vectors in $\mathbb{R}^n$ where each pair of vectors from the set are orthogonal, denoted as
$$
S ={u_1,...,u_p} \in \mathbb{R}^n. u_i^\top u_j = 0
$$
- If $S$ is orthogonal and non-zero, then $S$ is linearly independent

__Orthogonal Basis__: A basis that is also an orthogonal set

__Computing coordinates in terms of basis $B$:
- Inefficiently: Set up a linear equation $Uc = y$, with a cost of $O(n^2m)$ (performing Gauss-Jordan on an $m \times n$ matrix)
- Efficiently: Compute $y^\top u_j = c_j(u_j^\top u_j) \implies c_j = \frac{y^\top u_j}{u_j^\top u_j}$, with a cost of $O(nm)$ (Dot products $m$ times)
$$
S \text{ is an orthogonal basis for } H \in \mathbb{R}^n. \forall y \in H, c_j = \frac{y^\top u_j}{||u_j||} \implies j = 1,...,p
$$
__Why use orthogonal bases?__:
- Coordinates are easy to compute (and more efficient)
- Orthogonal bases make it easier to find the closest point in a subspace to any vector (projections)