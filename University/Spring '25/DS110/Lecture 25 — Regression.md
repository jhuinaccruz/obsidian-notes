## Regression
>*A regression model tries to predict continuous values from features, as opposed to classification where the output is a label.*

### Linear
>*in a simple linear regression, we're trying to find the line of the form*
$$
\hat{y} = mx + b
$$
>*that is best fit to the dependent variable y. The hat over the y indicated that it's a prediction, not the value y observed in the data*

__Best fit__: The line that minimizes the residual sum of squares (the sum of all points of the square of the difference between y and the actual y)

$$
RSS(\hat{y}, y) = \sum_i(\hat{y}_i - y_i)^2
$$

>*The optimal model can be found straightforwardly using linear algebra*

### Multiple Regression
>*Multiple regression refers to a linear regression tha has more than one independent variable*

>*Multiple regression tries to find a function*
$$
\hat{y} = \beta_0 + \beta_1x_1 + \beta_2x_2 + ... \beta_nx_n
$$
>*that fits the data.*

>*The function is still called linear because it is simply a weighted sum of its inputs and has no more complex functions in it.*

>*That's good for getting a very direct sense of how important the different factors are to the outcome — you can just compare the coefficients.*

>*If the fit is no longer visualizable ass a line, it's a plane for two independent variables, and after that, we can't visualize the whole function, which is a "hyperplane"*

