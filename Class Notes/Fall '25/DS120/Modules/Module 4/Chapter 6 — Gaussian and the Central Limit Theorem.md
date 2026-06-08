__Gaussian Distribution__ (Normal Distribution): A probability density function resulting from the sum of many independent and identically distributed random variables. Some characteristics include
- Symmetry around the mean
- The means, median, and mode are equal
- The area under the curve is equal to 1.0
- Dense in the center and less dense in the tails
- Defined by two parameters; its mean (`µ`) and standard deviation `σ`)
- 68% of the area of a normal distribution is within one standard deviation of the mean
- 95% of the area of a normal distribution is within two standard deviations of the mean
- The density is calculated by
$$
f(x) = \frac{1}{\sqrt{2pi\sigma^2}}e^{\frac{-(x-\mu)^2}{2\sigma^2}}
$$

__Bell Curve__: The curve traced by the upper values of the normal distribution

__Law of Large Numbers__: Reality will meet the expectations more closely as the number of trials increases. In other words, the sample mean `X` converges to `µ` as `n` converses to infinity

__Variance__: Denoted by
$$
Var[\tilde{X}] = \frac{nVar[X]}{n^2} = \frac{Var[X]}{n} = \frac{\sigma^2}{n}
$$
__Central Limit Theorem__ (CLT): Two main forms of the theorem:
- If samples of size `n` are collected with a large enough `n`, the sample means are calculated, and a histogram is created of said means, the histogram will have an approximate normal bell shape
- If samples of size `n` are collected with a large enough `n`, the sum of each sample are calculated, and a histogram is created of said sums, the histogram will also have an approximate bell shape

__"Large Enough" Sample__: At least size 30 or should come from a normal distribution


