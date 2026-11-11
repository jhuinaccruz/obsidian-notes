__Rank__: A measure of the number of linearly independent rows or columns in a matrix, denoted as
$$
p(A). p(A) ≤ i == j 
$$
... where:
- A is any given matrix
- i is the number of rows
- j is the number of columns

__To find the rank of a matrix, perform__: Gauss-Jordan Elimination on it to find the number of rows that are linearly independent
- 
>*It essentially determines the dimensionality of the vector space formed by the rows or columns of the matrix*

__Singularity__: When a square matrix does not have an inverse or when its determinant is zero

__When a matrix has a rank the size of n__ (for a matrix of dimensions n\*n):
- A is non singular
- The rows and columns of A are linearly independent respectively
- Any linear system with matrix of coefficients A has a unique solution

__Transpose__: Represented by A^T, obtained by swapping the rows and columns of the matrix, giving a new matrix of dimensions m\*n (if the original matrix is of dimensions n\*m). Some important properties of a matrix
- __Orthogonality__:
$$
A = n*n.\ A^TA = I
$$
	where *I* is the identity matrix
- __Symmetry__: The transpose is the same as the original, such that
$$
A = n*n.\ A^T = A
$$
- __Skew-symmetric Matrix__:
$$
A = n*n.\ A^T = -A
$$
- Transposition Operations:
	- __Double Transpose of a Matrix__:
$$
A = n*m.\ {A^T}^T = A
$$
	- __Transpose Product__:
$$
(AB)^T = B^TA^T
$$
	- __Transpose Addition__:
$$
(A+B)^T = A^T + B^T
$$

__Determinant__: A scalar value from a square matrix, zero if the matrix is singular, denoted by
$$
det(A) \iff |A| \iff \Delta A
$$
- for a 2\*2 matrix, the formula is
$$
A = 2*2 = \begin{bmatrix}
a \ b \\
c \ d \\
\end{bmatrix}.
\ |A| = ad - bc
$$

__Minor of an Element of a Matrix__: The determinants for every element of a matrix obtained by eliminating the rows and columns of said element, such that
$$
|M_{ij}| =  [a_{bc}] \in A.\ bc ≠ ij
$$
- where M_ij is the minor matrix created by eliminating

__Cofactor of Element of a Matrix__:
$$
C_{ij} = (-1)^{i+j} M_{ij}
$$

__Inverse of a Matrix__: A matrix that, when multiplied by the original matrix, results in the identity matrix. For a matrix to have an inverse, it must be
$$
\exists A. A = n*n, |A| ≠ 0 \iff \forall A, AA^{-1} = I
$$
- where A^-1 is the inverse of matrix A

__Two main ways of computing Matrix Inverses__:
- Determinant Method
- Elementary Transformation Method

__Adjoint__: For square matrices, the transpose of a cofactor matrix of a transpose matrix, denoted as
$$
A = n*n \iff adj(A) = [a_{ij}]_{n*n}
$$
__Determinant Method__: Defined as
$$
A = n*n \iff A^-1 = \frac{adj(A)}{|A|}
$$
__Elementary Transformation Method__: Using Gauss Jordan Elimination, the inverse of a matrix can be solved by
1. Rewrite the given matrix A as
$$
A = IA
$$
2. Use Gauss Jordan Operations until the identity matrix is on one side and the resulting inverse is on the other

