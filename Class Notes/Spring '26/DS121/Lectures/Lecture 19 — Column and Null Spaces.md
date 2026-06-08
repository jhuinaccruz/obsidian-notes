__Vector Space__: A set of vectors together with rules for vector addition and scalar multiplication, such that the vectors are considered *closed* under these two operations
- $x + y = y + x$
- $x = (y + z) = (x + y) + z$
- $x + 0 = x$
- $x + -x = 0$
- $1x = x$
- $(c_1c_2)x = c_1(c_2x)$
- $c(x+y) = cx + cy$
- $(c_1 + c_2)x = c_1x+c_2x$

__Euclidian Space__: The space $\mathbb{R}^n$ consists of all column vectors $v$ with $n$ components
- Assume the usual addition and scalar multiplication

__Euclidian Subspace__: A subspace of $\mathbb{R}^n$ is any set $H$ of vectors $\mathbb{R}^n$ that satisfies following properties
- $\vec{0} \in H$
- $\forall u, v \in H: u + v \in H$ (Closed under addition)
- $\forall u \in H, cu \in H$ (Closed under scalar multiplication)

>*Each subspace is a vector space in its own right*

>*Every matrix has associated with it two vector spaces*

__Column Space__: The set $\text{Col}\ A$  of all linear combinations of the columns of $A$
- In an $m \times n$ matrix, its column space is a subspace of $\mathbb{R}^m$
	- In other words it is a subset of the codomain
- Algebraically, $\text{Col}\ A$ Is the set of all $b$ (from $Ax = b$) for which the system has a solution
- Geometrically, $\text{Col}\ A$ is the range of $T$ ($T: \mathbb{R}^n \leftarrow \mathbb{R}^m$)

__Null Space__ (Kernel): All the solutions of the homogenous equation $Ax = 0$, denoted as $\text{Nul}\ A$
- Geometrically, the set of vectors that are mapped to the zero vector
-  In an $m \times n$ matrix, the null space is a subspace of $\mathbb{R}^n$, 
	- In other words, it is a subset of the domain