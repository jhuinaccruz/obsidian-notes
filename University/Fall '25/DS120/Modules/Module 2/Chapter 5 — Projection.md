__Projection__: When relating to vectors, captures a vector with a representation that uses fewer dimensions, such that the vector between the projection and the original is orthogonal to the surface it is projected on
- A projection from two dimensions to one looks like a right triangle
It is denoted as
$$
Proj^{\vec{a}}_{\vec{b}} = \frac{\vec{a}.\vec{b}}{|\vec{b^2}|}\vec{b}
$$
where a is being projected onto b

__Projection on higher dimensions__: Generally projecting a vector in n dimensions into a subspace of m\*n dimensions
$$
\vec{\beta_1}, \vec{\beta_2}, ...\vec{\beta_n} \in M. Proj^\vec{v}_M = c_1\vec{\beta_1}, c_2\vec{\beta_2},... c_n\vec{\beta_n} = A\vec{c} = A(A^TA)^{-1}A^T\vec{v}
$$
where
- b_1, b_2,... are basis vectors spanning M
- vector v is a higher dimensional vector
- A is a matrix whose column vectors are the basis vectors for M
- vector c is a vector containing scalars c_1, c_2, etc

$$
A^T • (\vec{v} - A\vec{c}) = 0
$$
