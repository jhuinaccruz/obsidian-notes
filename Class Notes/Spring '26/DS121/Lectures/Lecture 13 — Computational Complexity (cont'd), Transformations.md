__Approximate Computing__: When computing with floating point numbers, it is important to follow these principles
1. Compare floating point numbers for closeness, not equality
	- *If two numbers should be equal, the relative error of the difference in the floating point should be small*
2. Relative error can be magnified during subtractions
	- *Id two numbers have errors at `x`th significant digit, but its first digits cancel out, the relative error is large*
3. Beware of ill-conditioned problems
	- __Ill-Conditioned Problem__: When the outputs of a function vary greatly based on small differences in output (e.g. `1/(a-b))
	- Ill-conditioned problems come up as well when solving certain problems involving matrices that are almost uninvertible

>*Because most real numbers cannot be represented exactly in a computer, any computation involving real numbers can introduce some error*

>*In `Ax = b`, we can think of `A` as a function that is "acting on" the vector `x` to create a new vector `b`. This gives us a new way of thinking about solving the function; we are finding the vector(s) `x` that are transformed into `b` under the "action" of `A`*

>*In other words... `A` transforms `x` into `b`*

__Transformation__: A function/mapping from `R^n` to `R^m`that assigns each vector in `R^n` to a vector `T(x)` in `R^m`, denoted as $$T:\ \mathbb{R}^n \implies \mathbb{R}^m$$
- __Domain__: The set `R^n`
- __Codomain__: The set `R^m`
- __Image__: The vector `T(x)` (is an image of `x` under `T`), denoted as $$x \mapsto T(x)$$
- __Range__: The set of images of all images `T(x)`

__Linear Transformation__: A transformation (`T`) is linear if $$\forall u, v \in \text{dom}(T).\ T(u+v) = T(u) + T(v)$$
$$\forall c \in \mathbb{R}\ \land\ \forall a \in \text{dom}(T). T(cu) = cT(u)$$
- Adversely, you can use the following function that combines both of the previous equations into one, denoted as $$T(cu + dv) = cT(u) + dT(v)$$

__Contraction__: A transformation (`T: R^2 -> R^2. T(x) = rx`) when 0 ≤ r ≤ 1
__Dilation__: A transformation (`T: R^2 -> R^2. T(x) = rx`) when r > 1

__Linear Transformation Matrix__: If `T` is a linear transformation, there is a unique matrix `A` such that
$$T:\mathbb{R}^n \rightarrow \mathbb{R}^m \implies \forall x \in \mathbb{R} ^ n. \ T(x) = Ax$$

__Standard Matrix__ (Transformation Matrix): Of a transformation `T`, a standard matrix `A` is denoted as
$$T: m \times n. A = [T(e_j)... T(e_n)] $$
- __Reflections__:
	- 