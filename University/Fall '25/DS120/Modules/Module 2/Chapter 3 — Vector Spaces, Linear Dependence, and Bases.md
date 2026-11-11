__Vector Space__: Consists of a set of vectors and the operations of adding vectors and multiplication by scalar values, such that they are closed under such operations
	In other words, adding a multiple of any vector will result in a vector that is still in the space

__Closed Under Addition__: The following axioms hold true for all vector spaces
- Commutativeness

$$
\vec{x} + \vec{y} = \vec{y} + \vec{x}
$$
- Associativity
$$
(\vec{x} + \vec{y}) + \vec{z} = \vec{x} + (\vec{y} + \vec{z})
$$
- Zero Vector:
$$
{∃}\vec{0}\in{V}.\vec{x} + \vec{o} = \vec{x}
$$
- Inverse
$$
\forall \vec{x} \in V, \exists \vec{-x} \in {V}. \vec{-x} + \vec{x} = \vec{0}
$$

__Closed Under Multiplication__: The following axioms hold true for all vector spaces
- Distributiveness
	- Scalar over vector
$$
a(\vec{x} + \vec{y}) = a\vec{x} + a\vec{y}
$$
	- Vector over scalar
$$
(a=b)\vec{x} = a\vec{x} + b\vec{x}
$$
- Associativity
$$
a(b\vec{x}) = (ab)\vec{x}
$$
- Identity
$$
1\vec{x} = \vec{x}
$$

__Vector Subspace__: When two vectors subspaces have identical definitions of vector addition and scalar multiplication, and one is a subset of the other, then the former is a subspace of the latter. A subspace is defined by three axioms
- Non-empty
$$
W ≠ Ø
$$
- Addition
$$
\vec{x} \in W, \vec{y} \in {W} \implies {\vec{x} + \vec{y} \in {W}}
$$
- Scalar Multiplication
$$
\alpha \in {\mathbb{R}}, \vec{x} \in {W} \implies {\alpha \vec{x} \in {W}}
$$
	... where W is a subspace of V

__Linear combination__: When a vector in a vector space (over all real numbers) is a linear combinations of some vectors if some scalars (all real numbers) exist in a vector space such that
$$
\vec{y} \in V \in \mathbb{R}. \vec{y} = a_1\vec{x}_1 + ... a_n\vec{x}_n
$$
__Vector Span__: Over a set of vectors, it is the collection of all possible linear combinations of those vectors, denoted as
$$
a_1 \vec{x_1} + a_2\vec{x_2} + ... a_n\vec{x_n}
$$
__Vector Space Generating Set__: When a set of vectors spans an entire Vector Space

__Vector Linear Independence__: When a set of vectors from a real vector space has only one solution in the form of
$$
a_1\vec{x_1} + a_2\vec{x_2} + ... + a_n\vec{x_0} = 0.\ a_1 = a_2 = ... = a_n = 0
$$

__Basis__: For vector spaces, a set of vectors that are linearly independent and generate the vector space

__Minimal Spanning Set__: When the basis of a subspace cannot be subset to create the same subset

__Standard Basis__:
$$
\vec{e_1} \begin{bmatrix} 1 \\ 0 \\ 0 \\ . \\ . \\ . \\ 0\end{bmatrix}, \vec{e_2} = \begin{bmatrix} 0 \\ 1 \\ 0 \\ . \\ . \\ . \\ 0\end{bmatrix},..., \vec{e_n} = \begin{bmatrix} 0 \\ 0 \\ 0 \\ . \\ . \\ . \\ 1\end{bmatrix}
$$

__Changing Bases__: When there are two bases (a and b) and a vector v in one basis, we can find the coordinates of said vector in another
$$
v_1\vec{a_1} + v_2\vec{a_2} + ... + v_m\vec{a_m} = v_1\vec{b_1} + v_2\vec{b_2} + ... v_m\vec{b_m}
$$