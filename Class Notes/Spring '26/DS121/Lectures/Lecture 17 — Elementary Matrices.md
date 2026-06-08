__Elementary Matrix__: A matrix obtained by performing a single elementary row operation on the identity matrix
- Swapping: Swap the ones of the identity matrix
- Multiplication by a scalar: Change the one of the row you are multiplying by a scalar with the appropriate scalar $c$
- Adding a row to another row: If adding `x` row to `y` row, change the 0 at $M_{yx}$ to the number of times `x` is being added to `y`

>*Every elementary row operation on a matrix is a linear transformation*

__Inverting Elementary Matrices__:
- Swapping: Stays the same
- Multiplication by a scalar: Change the scalar $c$ to $\frac{1}{c}$
- Adding a row to another row: Change the scalar $d$ to $-d$

>*Multiplying elementary row operations is also straightforward; simply apply the operation indicated by the left matrix to the right matrix*