__Inner Dot Product__:
$$
\exists u, v \in \mathbb{R}^n \implies \vec{u} .\vec{v} = u^\top v
$$
its properties include
$$
\exists u, v w \in \mathbb{R}^n, c \in \mathbb{R}
$$
- Symmetry
$$
u^\top v = v^\top u
$$
- Distributive
$$
(u + v)^\top w = u^\top w + v^\top w
$$
- Associative
$$
(cu)^\top v = c(u^\top v) = u^\top(cv)
$$
- Non-negativity (only if `u` ≠ 0)
$$
u^\top u ≥ 0
$$

__Magnitude__: The length of a vector, denoted as a non-negative scalar
$$
||v|| = \sqrt(v^\top v) = \sqrt{\sum_{i=1}^n v^2_i} = \sqrt{v^2_1 + v^2_2 + ... + v^2_n}
$$
__Unit Vector__: A vector whose magnitude equals one
$$
\vec{u} = \frac{1}{||v||} v
$$
__Distance between vectors__: The length of the difference between vectors, denoted as
$$
dist(u, v) = ||u - v||
$$

__Orthogonality__: Two vectors are orthogonal if they form a right angle at the origin, solved by
$$
||u-v||^2 = ||u||^2 + ||v||^2 - 2u^\top v
$$
In other words, orthogonality can be determined if
$$
u^\top v = 0
$$

__Law of Cosines__: For solving for a side of a triangle
$$
c^2 = a^2 + b^2 - 2ab\cos\theta
$$
for vectors, where each vector is a side of a "triangle", you get
$$
||u - v||^2 = ||u||^2 + ||v||^2 - 2||u||\ ||v||\cos\theta
$$
from this you can extract that
$$
u^\top v = ||u||\ ||v|| \cos\theta \iff \cos\theta = \frac{u^\top v}{||u||\ ||v||} \iff \cos\theta = (\frac{u^\top}{||u||})(\frac{v}{||v||})
$$
where the transpose of u divided by its magnitude and its counterpart in v are both unit vectors