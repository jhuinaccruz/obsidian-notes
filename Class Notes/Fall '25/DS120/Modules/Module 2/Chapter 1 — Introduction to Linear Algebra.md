__Linear System__: A collection fo equations in which variables are multiplied by constants and summed, with the following conditions
- No powers of variables greater than one
- No fractional or negative powers of variables
- No two variables multiplied together

__General Linear Equation__: Represented as
$$
u_1x_1 + u_2x_2 + ... u_nx_n = v
$$
__Matrix__: A collection of objects arranged in rows and columns, where it can be represented as
$$
M = m*n
$$
where:
- M = Matrix
- m = number of rows
- n = number of columns

__Vector__: Matrices containing one row or one column

__Identity Matrix__: A matrix containing one's along its diagonal and 0's elsewhere

__Gauss Jordan Elimination__: A set of three rules to follow when manipulating an augmented matrix:
- __Multiplication/Division by a Scalar__: Possible unless it is a non-zero scalar
- __Row Combination__: Replace a row with the sum/difference of that row and a nonzero multiple of another row
- __Swapping__: Swap two rows

__Reduced Row Echelon Form__ (RREF): A matrix which has the following properties
- The pivot (the first non-zero element) of each row is 1
- The pivot is always to the right of the previous one above it
- The pivot is the only non-zero entry in its column

__Inconsistent System__: Equations that contradict each other, or when a row in an augmented matrix contains all zeroes except for the last column

__Dependent System__: Equations that directly provide the same information, such that when simplified mirror each other, or when a row in an augmented system leads to a row of all zeroes, and the number of remaining non-zero rows is less than the number of unknowns

__Non-Singular Matrix__: A square matrix that leads to unique solution

__Singular Matrix__: A square matrix that does not lead to a unique solution