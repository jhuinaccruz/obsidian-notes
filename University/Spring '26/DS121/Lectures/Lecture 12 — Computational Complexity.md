>*A floating point is an approximation of some particular real number*

__Rounding__: Implies `x` will be replaced with its floating point counterpart, meaning the closest floating point number, denoted as
$$fl(x)$$
- __Rounding Error__: The process by which a number is rounded, denoted as $$fl(x) = x(1 + \epsilon)$$
__Absolute Error__: Calculated as $$|x - fl(x)|$$
__Relative Error__: Calculated as $$\frac{|x - fl(x)|}{|x|}$$

__Machine Epsilon__: Calculated as half the distance between one and the next larger floating point number, denoted with an `ε`