__Derivative__: The slope of the tangent to a line, denoted as 
$$
df/dx = f'(x) = \lim_{x\rightarrow{0}}\frac{f(x+\Delta{x}) - f(x)}{\Delta{x}} = \frac{\Delta{f}}{\Delta{x}}
$$
- __Trigonometry Rules__:
$$
f(x) = \sin(x) \iff f'(x) = \cos(x)
$$
$$
f(x) = cos(x) \iff f'(x) = -sin(x)
$$
$$
f(x) = tan(x) \iff f'(x) = sec^2(x)
$$
- __Power Rule__:
$$
f(x) = x^n \iff f'(x) = nx^{n-1}
$$
- __Sum/Difference Rule__:
$$
f(x) = g(x) \pm h(x) \iff f'(x) = g'(x) + h'(x)
$$
- __Product Rule__:
$$
f(x) = g(x)h(x) \iff f'(x) = g'(x)h(x) + g(x)h'(x)
$$
	- __Multiplication by a Constant__:
$$
f(x) = a*h(x) \iff f'(x) = a*h'(x)
$$
- __Quotient Rule__:
$$
f(x) = \frac{g(x)}{h(x)} \iff f'(x) = \frac{g'(x)h(x) - g(x)h'(x)}{h^2(x)}
$$
- __Reciprocal Rule__:
$$
f(x) = \frac{1}{g(x)} \iff f'(x) = \frac{-g'(x)}{g^2(x)}
$$
- __Chain Rule__:
$$
f(x) = h(g(x)) = f'(g(x))g'(x)
$$

__Partial Derivative__: When dealing with multivariate equations, taking the derivative of only one variable and treating the rest as constants, denoted as
$$
f_a(x,y,..) = \frac{\partial f(x,y,...)}{\partial{a}}
$$
where a is the variable to find the partial derivative of

__Second Order of Derivatives__: The derivative of a derivative, denoted as
$$
f_{aa} = \frac{\partial^2{f}}{\partial{x^2}}
$$
__Local Maximum/Minimum Point__: A peak/inverted peak in a graph, when f'(a) = 0
- __Local Maximum__: The output/value of a function that creates said peak/inverted peak in its graph representation
$$
D = f_{xx}(x_0, y_0)f_{yy}(x_0, y_0) - f_{xy}(x_0, y_0)^2
$$
- If D > 0
	- and if f_xx < 0 then the critical point is a Local Maximum Point and f(x_0, y_0) is a Local Maximum
	- and if f_xx > 0 then the critical point is a Local Minimum Point and f(x_0, y_0) is a Local Minimum
- If D < 0, then (x_0, y_0) is a saddle point
- If D = 0, then the test is inconclusive

__To find Critical Points__:
1. Put the first order partial derivatives into a system of equations, solving for each variable when it is zero
2. The resulting value gets put back into the main function, such that there is now pairings of (x, y), which are critical points