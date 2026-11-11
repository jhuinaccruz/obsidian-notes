>*When given a mathematical object, its "inverse" is another object that undoes the action of the first one*

__Invertible Linear Transformation__: Denoted and calculated as
$$
T: \mathbb{R}^n \rightarrow \mathbb{R}^n \iff S: \mathbb{R}^n \rightarrow \mathbb{R}^n. S(T(x)) = x \iff T(S(x)) = x 
$$
- $T$ is invertible
- $T$ is one-to-one
- $T$ is onto

__Invertible Matrix__: A matrix is invertible if there exists another matrix such that the two multiplied together results in the identity matrix
- If non-invertible, it is a __singular__ matrix, otherwise it is a __non-singular__ matrix
- If $A$ is an invertible matrix,
	- $(A^{-1})^{-1} = A$
	- $A^{\top} \iff (A^\top)^{-1} = (A^{-1})^\top$
	- If $B$ is also an invertible matrix, then so is $AB$, which means $(AB)^-1 = B^{-1}A^{-1}$

>*If $A$ is the standard matrix of a linear transformation $T$, the factor by which the area changes due to $T$ is...the determinant of $A$, $\det(A)$*

__Second-Order Determinant__: For any linear transformation, the area of its unit square is determined by a factor of $|ad - bc|$

__Determinant__: The factor by which an area of `A` changes due to transformation `T`
- $\det(AB) = det(A)det(B)$
- $\det(A^\top) = \det(A)$
- If `A` is triangular, then its determinant is the product of entries on the main diagonal of A
- If $\det(A) = 0$, then `A` is not invertible

>*If `A` is an invertible $n\times n$ matrix, then for each `b` in `R^n`, the equation $Ax = b$ has a unique solution $A^{-1} b$*

__Invertible Matrix Theorem__: For an $n \times n$ matrix `A`
- `A` is an invertible amtrix
- `A^T` is an invertible matrix
- The equation $Ax = b$ has a unique solution `b` in `R^n`
- `A` has `n` pivot positions
- `A` is row equivalent to the identity matrix
- The determinant of `A` is nonzero
- The homogenous equation $Ax = 0$ has only the trivial solution
- The columns of `A` form a linearly independent set
- The columns of `A` span `R^n`
- The linear transformation $x \mapsto Ax$ maps `R^n` onto `R^n`
- The linear transformation $x \mapsto Ax$ is one-to-one