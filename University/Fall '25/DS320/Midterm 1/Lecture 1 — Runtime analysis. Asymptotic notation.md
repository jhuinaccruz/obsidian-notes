## Asymptotic Notation

__Upper Bound (O)__: For a pair of functions *f,g : N -> R*, we can write
$$
{f} \in {O(g(n))} \iff \exists {c_1, c_2} . c_2 > 0 \land \forall {n ≥ c_1}, (f(n) ≤ c_2g(n) \iff f(n) = O(g(n)))
$$
where:
- *f(n)* represents the function you are trying to find the runtime of
- *g(n)* represents the rate to compare against
- c2 is a constant that scales *g(n)* such that it is eventually bigger than *f(n)*
- c1 is the threshold after which *f(n)* stays below *c2g(n)*

__Lower Bound (Ω)__: For a pair of functions *f,g : N -> R*, we can write
$$
f \in {O(g(n))} \iff \exists c_1, c_2. c_2 > 0 \land \forall n ≥ 1, f(n) ≥ c_2(g(n)))
$$
in this case:
- *f(n)* and *g(n)* remain the same
- c2 is the constant that scales *g(n)* such that it is no smaller than the constant of the dominant term of f(n)
- c1 is the threshold after which *f(n)* stays above c2g(n)

__Tight Bound (θ)__: For a pair of functions *f,g : N -> R*, we can write
$$
f \in \theta(g(n)) \iff f(n) = O(g(n)) = Ω(g(n))
$$
or:
$$
\lim_{n \rightarrow \infty} \frac{f(n)}{g(n)}
$$
if the limit is:
- 0: Upper limit only
- Infinity: Lower limit only
- Otherwise, it is a tight bound

## Asymptotic Properties
- Multiplication by a constant
$$
f(n) = O(g(n)) \implies \forall c > 0. c, f(n) = O(g(n))
$$
- Transitivity
$$
f(n) = O(h(n)) \land h(n) = O(g(n)) \implies f(n) = O(g(n))
$$
- Symmetry
$$
f(n) = O(g(n)) \implies g(n) = Ω(g(n))
$$
$$
f(n) = \theta(g(n)) \implies g(n) = \theta(f(n))
$$
- Dominant Terms
$$
f(n) = O(g(n)) \land d(n) = O(e(n)) \implies f(n) + d(n) = O(max[g(n), e(n)]) = O(g(n) + e(n))
$$

## Common Functions
- __Polynomials__:
$$
a_= + a_1n + ... + a_dn^d \implies \exists{a_d} > 0, \Theta(n^d)
$$
	- __Polynomial Time__: Running time is *O(n^d)* for some constant d independent of input size n
- __Logarithms__:
$$
\forall a, b > 0: log_a{n} = \theta(log_bn)
$$
... Every log is roughly equal to one another
$$
\forall x>0, log(n) = o(n^x)
$$
... Every log grows slower than every polynomial
- __Exponential__:
$$
\forall r >1, d >0 . n^d = o(r^n)
$$
... Every polynomial grows slower than every exponential
- __Factorial__: (Sterling's formula)
$$
n! = (\sqrt{2\pi n})(\frac{n}{e})^n(1 + o(1)) = 2^{\Theta(n\ log\ n)}
$$
## Strict Bounds
__Strict Upper Bound o()__:
$$
f(n) < c_2g(n)
$$

__Strict Lower Bound ω()__:
$$
f(n) > c_2g(n)
$$