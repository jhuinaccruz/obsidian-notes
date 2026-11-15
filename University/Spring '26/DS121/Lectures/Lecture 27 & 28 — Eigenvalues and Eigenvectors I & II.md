__Eigenvector__: A vector such that, when transformed under $T$, results in a vector which is simply a scaled-up version of the same vector
$$
Ax = \lambda x
$$
- __Eigenvalue__ ($\lambda$): The scalar of $x$
	- $A$ must be square
	- $\lambda$ exists only if $A - \lambda I$ is singular ($\det(A - \lambda I) = 0$)
		- __Characteristic Polynomial__: The determinant of $\det(A - \lambda I) = 0$, a polynomial of degree $n$
		- __Characteristic Equation__: $\det(A - \lambda I) = 0$
		- An eigenvalue of 0 exists only if $A$ is not invertible
		- Things to be careful of for eigenvalues:
			- Eigenvalues be complex for "simple" matrices
			- Gaussian elimination does not preserve eigenvalues
- __Eigenspace__: The set of all eigenvectors corresponding to a particular eigenvalue
	- Described as *the eigenspace of $A$ corresponding to $\lambda$*
	- The eigenspace of $A$ is the null space of the matrix $A - \lambda I$
	- Eigenspaces are a subspace of $R^n$, where $n$ is the dimensions of $A$
