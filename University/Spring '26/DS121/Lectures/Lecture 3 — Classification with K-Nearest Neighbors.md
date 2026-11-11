__Supervised Learning__: Data has labels, such that it learns how to label new incoming data
__Unsupervised Learning__: There are no labels; the goal is to discover its structures and patterns
- Supervised data is given as a pair of values `{(x_i, y_i)}`
- The goal is to predict `y` for any new `x`
- Supervised learning assumes that the label depends on its features
- Its key principles include
	- There are a set of possible prediction rules, which it learns
	- The rules that work on training data can be extrapolated (generalized) to a larger dataset

>*Each data item is denoted as a vector `x`*

__Feature__: Each entry within `x` (independent variable)
__Target__: Each entry within `y` (dependent variable)

__Regression__: When `y` is continuous like a number
- Success is defined as when the predictions are close to the actual values
__Classification__: When `y` is discrete like a category
- Success is defined as when predictions are correct most of the time

__K-Nearest Neighbors__: Given a new data point x, find the `k`-closest points in the training data and use their labels to make a prediction
- Closeness is defined as the smallest Euclidean distance
- k-NN can be used for both classification and regression
	- For classification: labels are used to make a prediction based on the "majority vote" through either a
		- __Hard Classifier__: Returning the majority vote of the labels on the `k` nearest neighbors
			- May be indeterminate
		- __Soft Classifier__: Denoted as
$$
p(y = c\ |\  x, k) = \frac{\text{number of neighbors with label }c}{k}
$$
	- For Regression: labels are used to make a prediction based on the "average" of the neighbors' values
		- Larger `k`: Sensitive to noise with complex decision boundaries
		- Smaller `k`: Smoother boundaries that may miss local patterns

__Overfitting__: When k is too small, such that it fits the training data too well
__Underfitting__: When k is too large, the model becomes too simple, such that it ignores structure within the data