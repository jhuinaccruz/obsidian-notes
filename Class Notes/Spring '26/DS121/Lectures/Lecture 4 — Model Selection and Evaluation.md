__Train/Test Split__: Divide training data into train data and test data, such that the model is trained on the test data only and evaluated on the test data

__Train/Validation/Test Split__: To prevent tuning `k` to the test set, we can split the test data into three: a train set to fit the model, a validation data to tune hyperparameters (like `k`), and a test evaluation data set used at the end
- Can be through either
	- Random Subsampling: Multiple random splits, then average the result
	- Cross-validation: Systematically use all data for both training and testing

__Model Selection__: The process of evaluating a good value for `k`
- As polynomial order increases, training error (`E(w)`) decreases and test error decreases then increases

__Polynomial Regression__: Denoted as
$$
y(x, w) = w_0 + w_1x + w_2x^2 + ... + w_kx^k
$$

>*The best test error is at `k` = 3, since higher-order polynomials overfit*

__Hyperparameter__: A setting that is chosen before training using validation data
- Polynomial degree `k`
- Number of neighbors in `k`-NN
- Learning rate, regularization strength

__Random Subsampling__: Randomly split data multiple times, then train/evaluate on each split, then average the results

__Cross-Validation__: Also known as `k`-fold cross-validation; splits data into k parts, where each part takes a turn as a validation set
- Variants include 5/10-fold (common defaults) and leave-one-out (`k` = dataset size)

>*Larger `k` = more training data per fold, but also more computation*

__Grid Search__: Try multiple hyperparameter values, then picks the best using cross-validation

__Accuracy__: Calculated as fraction-correct (`x`% positive)
- Not good as a metric for learning models

__Confusion Matrix__: Denoted as a 2x2 table, where the x-axis reflects the classifier predictions, and the y-axis the actual values; each axis with two classifications of either positive or negative