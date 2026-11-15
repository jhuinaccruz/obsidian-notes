>*Data science is largely about manipulating matrices because almost all data can be represented as a matrix*

__Important parametrics for designing an algorithm__:
- Speed
- Memory Use
- Accuracy/Stability
- Scalability/Parallelization

>*Sometimes for the same question, the answers we get from a computer are very different from the answer we get mathematically!*

__IEEE-754__: The standard for floating-point arithmetic first coined in the 1980s
- `NaN`: Not a number
- `Infinity`: Can be both positive and negative
- `0`: Both positive and negative

__Cost__: In an algorithm, measured by counting the number of operations such as addition/subtractions and multiplication/divisions
- __Flops__: Said operations performed over floating numbers
	- Counting flops is primarily focused on the highest powered term as well as the order of the expression

>*In modern processors, each of these operations require only a single instruction*

__Big-O Notation__:
$$\exists f, g. f(n) = O(g(n)) \iff \exists c, k.\ \forall n > k,  |f(n)| ≤ c(g(n))$$
where
- `c` and `k` are witnesses

__Floating Point Operations__ (FLOPS):
- Arithmetic operations ($+, -, \times$, etc): 1
- Dot Product: $(n)(n-1) = 2n - 1$
- Matrix Multiplication: $C_{ij} = \sum^n_{k=1} A_{ik}B_{kj} \implies mp(2n-1)$
	- where $A = m\times n$, $B = n\times p$, $C = m\times p$
- Matrix Addition $C = mn$
- Matrix-vector Multiplication: $y_i = \sum^n_{j=1} A_{ij}x_j \implies m(2n-1)$
	- where $A = m\times n$, $x = n\times 1$, $y = m\times 1$