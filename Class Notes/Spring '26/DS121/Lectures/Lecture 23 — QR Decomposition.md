__Orthogonal Set__: An orthogonal set of unit vectors
- Lineariy independent by nature (since orthogonal sets are linearly independent)
- It's transpose times itself is the identity matrix
- *Preserve Lengths Theorem*: The linear transformation from $\vec{x} \mapsto U\vec{x}$ (Orthonormal Transformation) preserves lengths, inner products, and orthogonality
	- For a orthonormal matrix $m\times n$ and for some vectors $x, y \in \mathbb{R}^n$
		- $||U\vec{x}|| = ||x||$
		- $(U\vec{x})^\top(U\vec{y}) = x^\top y$ 
- __Orthonormal Column__: Within an orthogonal set/matrix, when the vectors within are orthogonal to one anotther

>*When they (orthonormal sets) span a space, they form an orthonormal basis for that space*

__Orthonormal Transformation__: A linear transformation $x \mapsto Ux$ that preserves lengths, inner products, and orthogonality

>*Orthonormal maps cannot decrease dimension, since orthonormal matrices cannot have a null space*

>*An $m\times n$ matrix with orthonormal/orthogonal must have more rows than columns*

__QR Factorization__: A fundamentally different way of solving linear systems whose key advantage over other methods is numerical stability (preventing rounding errors from accumulating) and main application lies with least-squares problems, as well as ill-conditioned systems.
- It's denoted as $A = QR$ where:
	- $A$ is an $m\times n$ matrix with linearly independent columns
	- $Q$ is an $m\times n$ whose column vectors are orthonormal
	- $R$ is an $n\times n$ upper triangular square matrix
- Steps for factorization
	1. Use Gram-Schmidt orthogonalization on the columns of $A$
	2. Find the columns of $Q$ by normalizing each column individually
	3. Calculate $R = Q^\top A$ 
- Rewriting $Ax = b$, you get $Rx = Q^\top b$
	- Runs faster since $R$ is an upper triangular matrix, requiring only backsubstitution instead of 
	- The initial cost of solving for $Q$ and $R$ is $\frac{2}{3}n^3$, then requiring $O(n^2)$ to solve

__Overdetermined Systems__: Systems $Ax = b$ where $b$ is not in $\text{Col }A$