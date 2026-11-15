__Regression__ A set of techniques for estimating and measuring relationships between variables

__Linear Regression__: Assumes
- Linearity: A linear relationship between an independent and dependent variable, such that its changes are proportional to one another
- Independence: Observations of each variable are independent
- Homogeneity of Variance: The size of the error in the prediction does not change significantly across the independent variable values
- Normality: The data follows a normal distribution

__Best-fit Line__ (Linear Regression): A straight line that represents the relationship between the independent and dependent variables, such that the line implies the least amount of error.
$$
y = mx + b
$$
where x and y represent the independent and dependent variables respectively

- __Zero Slope Intercept__:
$$
Proj^\vec{y}_\vec{x} = m\vec{x} = \frac{\vec{y}\vec{x}}{\vec{x}\vec{x}}\vec{x}
$$
- __Slope Intercept of B__
$$
\vec{y} = \vec{x}
\begin{bmatrix}
m \\
b
\end{bmatrix}
.Proj^\vec{y}_M = A\vec{c}
$$
 - __Exponential Model__:
$$
y = Ce^{mx}. \ln(y) = \ln(Ce^{mx}) = \ln{C}\ + mx
$$

- __Multiple Regression__
$$
y = m_1x_1 + m_2x_2 ... m_nx_n + b
$$
- __Fitting Polynomials__
$$
y = m_1x^1 + b + m_2x^2 + .. m_nx^n 
$$
