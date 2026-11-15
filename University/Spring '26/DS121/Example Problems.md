# Lectures
### Is $x$ an eigenvector of $A$? If so, what are the corresponding eigenvalues?

1. Solve the equation $Ax$, then compare against $\lambda x$ and solve for $\lambda$
$$
Ax = \lambda x
$$

### Show that $\lambda$ is an eigenvalue of the matrix $A$ and find the corresponding eigenvector

We need to solve for some eigenvector $x$
1. Rewrite the equation such that $$Ax = \lambda x \implies Ax - \lambda x = 0 \implies Ax - \lambda Ix  = 0 \implies (A-\lambda I)x = 0$$
	We assume there is a non-trivial answer to this, so we solve as a normal equation through row reduction

### Is $\lambda$ an eigenvalue of $A$?
We need to determine whether there is a nontrivial solution to the equation $(A-\lambda I)x = 0$

1. Solve similar to the previous problem
	- If there is at least one free variable, the answer is *yes*
### Given $A$ and $\lambda$, find a basis for the corresponding eigenspace
In other words, we are looking for the eigenspace in the null space of $A - \lambda I$

1. Row reduce the augmented matrix from $$(A - \lambda I)x = 0$$
2. Assuming the resulting vector is nontrivial, express the vector as a sum of its free variables times numerical vectors
	- The resulting vectors make up the basis subspace

### Solving for the Eigenvalues
We need to find all the values of scalar $\lambda$ such that the Characteristic Equation is true

1. Set up and solve the Characteristic Equation for the determinant
2. Set the determinant to zero and solve

### Solving for the Eigenvectors

1. Solve for the eigenvalue(s), then solve the equations

### Prove that if $A^2$ is the zero matrix, then the only eigenvalue of $A$ is $0$

### Prove that two similar matrices have the same characteristic polynomials
$$
B = P^{-1}AP
$$
$$
B - \lambda I = P^{-1}AP - \lambda I
$$
$$
\ = P^{-1}AP - \lambda P^{-1}P
$$
$$
\ = P^{-1}(AP - \lambda P)
$$
$$
\ = P^{-1}(A - \lambda I)P
$$
Then to determine the characteristic polynomial
$$
\det(B - \lambda I) = \det([P^{-1}(A - \lambda I)P])
$$
$$
\ = \det(P^{-1})\det(A - \lambda I)\det(P)
$$
$$
\ = \det(P^{-1})\det(P)\det(A - \lambda I)
$$
$$
\ = \det(I)\det(A - \lambda I)
$$
$$
\det(B - \lambda I)= \det(A - \lambda I)
$$
### Find the steady-state vector for a Markov Chain
Since a steady-state vector is really just an eigenvector of the schoastic matrix, we can solve for the stady-state vector for a Markov chain by:

1. Set the linear system as
$$
Pq = q \iff Pq - q = 0 \iff (P - I)q = 0
$$
2. Obtain a general solution through Gauss-Jordan Elimination
3. Pick any specific solution for the free variable, then scale it down such that it becomes an eigenvector

### If possible, diagonalize $A$

1. Find the eigenvalues of $A$
2. Determine whether $A$ can be diagonalized by solving for each eigenvalue's free variables
3. If the resulting eigenvectors make up $n\times n$, then construct $P$ using the eigenvectors
4. Construct $D$ using the eigenvectors based on their position in $P$
	- Ensure algebraic repetition (multiplication) if the eigenvalue has an algebraic multiplicity greater than 1
## Find the Orthogonal Diagonalization of a Matrix

1. Find its eigenvalues
2. Find its eigenvectors
3. Ensure orthonormality within the eigenvectors
4. Construct $P$ and $Q$

# Homeworks
## 1
### If $v$ and $w$ are vectors in $\mathbb{R}^n$ and have the same magnitude, then the magnitude of $v-w$ is $0$

$$
\vec{v} = \begin{bmatrix}v_1 \\ v_2\end{bmatrix}, \vec{w} = \begin{bmatrix}w_1 \\ w_2\end{bmatrix}
$$
$$
||\vec{v}|| = ||\vec{w}|| \rightarrow \sqrt{v_1^2 + v_2^2} = \sqrt{w_1^2 + w_2^2} \rightarrow v_1^2 + v_2^2 = w_1^2 + w_2^2
$$
Rearranging terms, we see that
$$
v_1^2 + v_2^2 - w_1^2 - w_2^2 = 0 \rightarrow \vec{v} - \vec{w} = 0
$$

### If $\vec{v}$ is orthogonal to $\vec{v}$ and $\vec{w}$, then $\vec{v}$ is parallel to $\vec{w}$

This is true for vectors in a two-dimensional space, but it is not necessarily true for spaces spanning larger than two dimensions. Vectors can be orthogonal to a specific vector at the same point, yet not be parallel to each other.

### If $\vec{u}$ is orthogonal to $\vec{v}$ and $\vec{w}$, then $\vec{u}$ is orthogonal to $-\vec{v} + 3 \vec{w}$

Firstly, we are given
$$
\vec{u} ^\top \vec{v} = 0,\ \vec{u}^\top \vec{w} = 0
$$

To determine whether this is true, we have to check whether
$$
\vec{u}^\top (-\vec{v} + 3\vec{w}) = 0
$$
Rewriting the problem by distributing $\vec{u}$, we get something like
$$
\vec{u}^\top \vec{v} + 3\vec{u}^\top \vec{w} = 0
$$

We can simplify further, since $\vec{u}$ is orthogonal to $\vec{v}$ and $\vec{w}$
$$
0 + 3\times0 = 0
$$
The statement is true.

### Given vectors $\vec{a}$ and $\vec{b}$...
#### - What is the length of $\vec{a}$?

Calculate the length (or magnitude) of the vector
#### - What is the inner product of $\vec{b}$ with itself?

Also known as simply the squared magnitude of itself
#### - What are two unit vectors parallel to $\vec{b}$?

There are two components to this question; the unit vector and parallelism calculation

Unit vectors are calculated by dividing a vector by its magnitude, so the unit vector of $\vec{b}$ is:
$$
\hat{b} = \frac{1}{||b||} \times \vec{b}
$$
Parallel vectors exist as a multiple of a vector. In other words, parallel vectors to any given vector are simply multiples of the same vector. In the case of parallel unit vectors, there are always two: itself and its negative multiple. In other words, the two parallel unit vectors are
$$
\hat{b}, -\hat{b}
$$

#### - Calculate the angle between $\vec{a}$ and $\vec{b}$

In order to find the angle, we must remember the formula
$$
\cos \theta = \frac{a^\top b}{||a||||b||}
$$
or, to solve this question
$$
\theta = \cos^{-1}({\frac{a^\top b}{||a||||b||}})
$$
#### - Provide a vector that is perpendicular to $\vec{a}$

### Use vector algebra to prove that the midpoint of the hypotenuse of a right triangle is equidistant from the three vertices

- Set the bisector equal to the half of the equation
	- (in the homework it looked like)
$$
\frac{v+w}{2} = \frac{v-w}{2}
$$
- Since we are solving for distance, find the magnitude of the two vectors sum/differences

## 2
## 3

## 4
### Is the transformation $T$ linear?

Remember, in order for the equation to be linear, it must be closed under addition and scalar multiplication. In other words, rewrite the transformation as
$$
T(c\vec{u} + d\vec{v}) = cT(\vec{u}) + dT(\vec{v})
$$
...and check if the inequality holds

### Given an RREF Augmented Matrix and a real value $y$, for which values of $y$ does the system...
#### - Have no solutions?

A system has no solutions when the right hand side has anything but a zero and the left hand side has all zeroes
#### - Have infinitely many solutions?

A system has infinitely many solutions when there are free variables (less pivots than the rank)

#### - Have a solution?

A system has one solution when there are no free variables and no contradictions ($\sum_1^x ≠ 0$)

### Provide the exact flop count...

Remember FLOP count:
- __Arithmetic__: $1$
- __Vector-Vector Operations__: $n$
- __Matrix-Vector Multiplication__: Given $A = m \times n$ and $\vec{v} = 1$: $A\vec{v} = m(2n-1)$
- __Matrices__:
	- Adding/Subtracting: $A, B = m \times n$: $A ± B = n^2$
	- Multiplication: Given $A = m \times n$ and $B = n \times p$: $AB = mn(2n-1)$
## 5
### If $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ is a linear transformation and $A$ is its standard matrix representation, what is the size of $A$?

$A: m \times n$
### $A$ is an onto transformation

$A$ is an onto transformation if and only if it has a pivot on every row

### $A$ is a one-to-one transformation

$A$ is a one-to-one transformation if and only if it has a pivot on every row

### Suppose $C$ is invertible, show that if $AC = BC$, then $A = B$

We are given implicitly that
$$
CC^{-1} = I
$$

That means, after multiplying both sides by the inverse of $C$
$$
ACC^{-1} = BCC^{-1}
$$
$$
AI = BI \rightarrow A = B
$$
### $A$ is an invertible matrix. Find the determinant of $A^\top A^{-1}$

We have to use the properties of determinants to solve this problem

$$
\det (A^\top A^{-1})
$$
$$
\det(A^\top)\det(A^{-1})
$$
$$
\det(A)\frac{1}{\det(A)} = 1
$$
## 6
### Given $A$, factorize into $LU$

The general steps are
1. Set up $L$ as a matrix with 1s on the diagonal, and $U$ with the first row of $A$ as its first row

### GIven A...
#### - Find the Column Space

To find the column space of a vector:
1. Reduce $A$ into RREF
2. Match the corresponding pivots to the original column vector in $A$; the resulting vector is the column space

#### - Find the Null Space

To find the null space:
1. Set the row equations in $A$ to zero and solve for any free variables
2. Factor out the resulting column variables: the remaining numerical vectors make up the null space

>*Important: $n = \text{Rank}(A) + \text{Col}(A)$.*

## 7
### Three given vectors form an orthogonal set

Simply multiply them each with one another, ensuring each of their dot products is zero

### Prove that if $U$ and $V$ are both orthogonal, then so is $UV$

We are given
$$
U^\top U = I, V^\top V = V
$$
And so, we are asked to prove
$$
(UV)^\top (UV) = I
$$
Using the property of transposes:
$$
(UV)^\top = V^\top U^\top
$$
$$
V^\top U^\top U V = V^\top (U^\top U)V
$$
$$
V^\top I V = V ^\top V
$$
$$
= I
$$

## 8
## Quiz Questions
### Given $y$, $u_1$, $u_1$, $W = \text{Span} \{u_1, u_2\}$ , and $u,v$ being orthogonal, which point in $W$ is closest to $y$

Since we know they vectors are orthogonal, we can project $y$ onto $W$ to find the point closest to $u_1$ and $u_2$. That is to say,
$$
\text{Answer} = \text{proj}_W^y = \text{proj}_{u_1}^y + \text{proj}_{u_2}^y
$$