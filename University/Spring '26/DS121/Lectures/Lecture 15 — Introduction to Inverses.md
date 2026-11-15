__One-To-One Transformation__: Denoted and defined as
$$
T: \mathbb{R}^n \rightarrow \mathbb{R}^m \implies \forall b \in \mathbb{R}^m, b \text{ is an image of at most one }x \in \mathbb{R}^n
$$
- In other words, $\forall b, T(x) = b. b = 0 \lor 1$

>*Hence, the concept of one-to-one is asking a uniqueness question about solutions to the equation $T(x) = b$*
- If $A$ is an $m \times n$ matrix, and $T(x) = Ax$, then the following are true
	- $T$ is one-to-one
	- $\forall b \in \mathbb{R}^m,\ T(x) = b$ has at most one solution
		- The equation $Ax = b$ has a unique solution or is inconsistent
	- $Ax = 0$ has only the trivial solution
	- The columns of $A$ are linearly independent
	- $A$ has a pivot in every column
	- The range of $T$ has a dimension $n$
	- 0 is not an eigenvalue of $A$

__Onto Transformation__: Denoted and defined as
$$
T = \mathbb{R}^n \rightarrow \mathbb{R}^m. T \text{ is onto } \mathbb{R}^m \implies \forall b \in \mathbb{R}^m \text{ is the image of at least one } x \in \mathbb{R}^n
$$

# Need to Finish