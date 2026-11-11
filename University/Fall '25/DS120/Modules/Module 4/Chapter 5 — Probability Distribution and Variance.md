__Random Variable__: A variable that takes on different values determined by chance
- *Discrete*: A random variable that takes on a finite or countably infinite number of values
- *Continuous*: A random variable that takes on a non-countable infinite number of values

__Probability Distribution Functions__ (PMF): A function that provides the distribution of probabilities for the possible outcomes of the random variable `X`, typically denoted as `f(x)`
- *Probability Mass Functions* (PMF): The probability distribution for a discrete random variable
$$
f(x) = P(X = x).\ x \in \text{sample space} \implies f(x) > 0, \sum_x f(x) = 1 
$$

- *Probability Density Functions* (PDF): The probability distribution for a continuous random variable `X`
$$
\Pr(X = x) = 0. x \in \text{sample space} \implies f(x) > 0
$$
	additionally, when solving for PDF, PDF ≠ `P(X = x)`, but rather the area under the curve
- *Cumulative Distribution Function*: A function that gives the probability that a random variable `X` is less than or equal to `x`
$$
F(x) = P(X ≤ x)
$$
