>*An `m` x `n` matrix has `m` rows and `n` columns*

__Square Matrix__: `n x n`

__Identity Matrix__: A square matrix that has ones on the main diagonal and zeroes elsewhere

__Transpose__: $$B = A^\intercal \implies \forall b_{i,j} \in B = a_{j,i} \in A$$$$(A^{\intercal})^{\intercal} == A$$
$$
(A + B)^\intercal = A^\intercal + B^\intercal
$$
$$\forall r, (rA)^\intercal = r(A^\intercal)$$
$$(AB)^\intercal = B^\intercal A^\intercal$$

__Matrix Addition/Scalar Multiplication__: $\forall m\times n \text{ matrices } A,B,C\ \land \forall r,s \in \mathbb{R}:$
- $A+B = B + A$
- $(A+ B) + C = A + (B + C)$
- $(A + 0) = A$
- $r(A + B) = rA + rB$
- $(r+s)A = rA + sA$
- $(r)sA = (rs)A$

__Basic Variables__: Relate to the columns that contain pivots
-  If not a basic variable it is considered a __Free Variable__

__Consistency__: Results in a matrix with no free variables
__Inconsistent__: A zeroes row with a non-zero solution