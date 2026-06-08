__Simple Regression__: When a dataset fits a line perfectly, it can be written as a set of parameters represented in a matrix equation
$$
X\beta = y
$$
- where variables correspond to specific matrices
	- $X$: Design Matrix (Independent Variables)
	- $y$: Observation Vector (Dependent Variables)
	- $\beta$: Parameter Vector

__Regression__: When trying to fit a line onto data that may not fir perfectly, it can be written as a set of parameters represented in a matrix equation, minimizing the sum of squared residuals
$$
\sum_i(X\beta - y_i)^2 = ||X\beta - y||^2
$$
- The sum of the squares of the residuals is exactly the squared distance between the vectors $X\beta$ and $y$
- *Steps*:
	1. Set up the design matrix $X$ and observation $y$
	2. Write out the normal equations $X^\top X\hat{\beta} = X^\top y$ and solve for the parameters ($\beta_0, \beta_1$)

__Feature Engineering__: M

>*Polynomial regression is multiple linear regression with engineered features*

__General Linear Model__: Denoted as $$y = \beta_0 + \beta_1u + \beta_2v + \beta_3u^2 + \beta_4uv + \beta_5v^2$$
- A linear model will arise whenever $y$ is predicted by an equation of a form similar to
 $$y = \beta_0f_0(u,v) + \beta_1f_1(u,v) + ... + \beta_kf_k(u,v)$$

>*Similar to KNN and k-means, regression is affected by unstandardized units, such that its geometry is useless otherwise, though not as bad as kNN and k-Means*

__Multicolinearity__: When features are perfectly correlated...
- The null space is nontrivial
- The design matrix loses rank

__Coefficient of Determination__: Denotes how well a model predicts the dependent variable, denoted as $R^2$ and calculcated as
$$
R^2 = 1 - \frac{SS_{res}}{SS_{tot}}.SS_{tot} = \sum_{i=1}^n(y_i - \bar{y}_i)^2 = ||r||^2, \ SS_{res} = \sum_{i=1}^n(y_i - X\hat{\beta})^2
$$
- $R^2 \in [0,1]$, where a 1 implies a perfect and a 0 implies the model only predicts the mean
- Adding the overall number of variables always makes $R^2$ increase
	- Increasing $R^2$ does not imply a better fit

__Anscombe Quartet__: A group of four graphs with similar mean, variance, correlation, regression line, and coefficient of determination with differing underlying structures
- Linear, curved, outlier-dominated linear, and leverage point (a single x-value mapping the entire regression line)
- Shows how one must always look at residual plots, since $R^2$ alone is misleading

__Residual Plots__: Should look like random noise, otherwise the model is misspecified and needs more polynomial terms/new features

>*A regression of degree $n-1$ passes through all of $n$ data points exactly, but generalizes terribly*

__Regularization__: Prevents overfitting of a model by adding a penalty to a model's complexity, such that the $R^2$ is lowered, thus making it more robust on new data
- L1: Known as a lasso, adds $\lambda||\beta||_1$ to the model
	- Represents the sum of absolute coefficients
	- Useful for shrinking coefficients to exactly zero, effectively as a "feature selection" tool
	- Geometrically looks like a diamond
- L2: Known as a ridge, adds $\lambda||\beta||_2^2$ to the model
	- Represents the sum of squared coefficients
	- Useful for shrinking coefficients closer to zero, effective when distributing weight across multicollinear variables
	- Geometrically looks like a circle