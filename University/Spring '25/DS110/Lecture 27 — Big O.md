## Time Complexity
__Time complexity__: Measures input size (n) versus time in the form of O(n)

__Linear Time__: O(n) (plotted looks like a diagonal straight line)

__Constant Time__: O(1) (plotted looks like a horizontal line)

__Quadratic Time__: O(n^2) (plotted looks like a parabola)

__Desirable attributes of a running time classification system__:
- Focus on what happens when the input gets too big
- Count operations to evaluate the category
- Small differences don't matter too much

__Looking for an item in a set has a time complexity of__: O(1)

__Looking for an item in a list has a time complexity of__: O(N)

$$
f = O(g(n))
$$
$$
f(n) ≤ cg(n)
$$

where:
- f is a function of natural numbers
- O(g(n)) if
	- c and n_0 is positive
	- n > n_0 (as the input gets bigger)
- cg(n) means that constants (c) can be ignored no matter how large they are

