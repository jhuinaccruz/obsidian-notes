__Factorization__ (Decomposition):  An equation that expresses matrix $A$ as a product of multiple matrices
- *Why factor?*
	- To make computing with $A$ faster
	- To make working with $A$ easier
	- Expose important properties otherwise unavailable in $A$'s natural form

__LU Factorization__: Applicable to any matrix
- Importantly, LU factorization is possible for any matrix that can be converted into echelon form without needing to swap two rows
	- Only addition operations that add a multiple of one row to another row below it are needed
	- If the rules above are broken, then the corresponding matrices are both lower triangular matrices
$$
A = m\times n. A = LU \implies L = m^2, U = m\times n
$$
where:
- $L$ is a unit lower triangle matrix of dimensions $m\times m$
- *U* is an upper triangular matrix of dimensions $m\times n$

__Unit Lower Matrix__: A square matrix with only ones on the diagonals and zeroes below it
__Upper Triangular Matrix__: A matrix with zeroes above its pivots

>*The product of unit lower triangular matrices is still lower triangular. The inverse of a unit lower triangular matrix is also unit lower triangular*


__Closure Properties of Lower Triangles Theorem__: If $A$ can be converted in to echelon form $U$ by scaling or adding a multiple of a row to another row below it, then U can be represented as a set of *elementary* unit lower triangular matrices as such:
$$
E_p...E_2E_1A = U
$$
Recomputing and moving the equation around, we get:
$$
A = (E_p...E_2E_1)^{-1}U \implies L = (E_p...E_2E_1)^{-1}
$$

Extrapolating even further, we can rewrite Gauss-Jordan Elimination as
$$
U = L^{-1}A
$$
- where $L$ is unit lower triangle and $L^{-1}$ is the row reductions required to transform A to row echelon form

>*When $A = LU$, the equation $Ax = b$ can be written as $(LU\vec{x}) = b$*

>*Setting $Ux$ as $y$, you get the following linear equation*

$$
L\vec{y} = \vec{b}, U\vec{x} = \vec{y}
$$
- You can then solve for $y$ first, then solve for $x$

*Why more efficient?* (given $A\vec{x} = b$)
- With the inverse method (calculate the inverse of $A$, then for every new $b$, multiply the value), the initial cost of calculating $A^{-1}$ is $2n^3$, plus $2n^2$ for every new vector $b$
- With the Gauss-Jordan Method, calculating every individual linear system for every $b$ costs $\frac{2}{3} n^2$ 
	- Additionally, cannot be automated, since for each $b$ the linear equation will always need to be individually calculated
- LU Factorization is better because there is only an upfront cost of $\frac{2}{3}n^3$ flops (for $L$ and $U$) then using forward and backward substitutions you get a cost of $O(n^2)$ flops