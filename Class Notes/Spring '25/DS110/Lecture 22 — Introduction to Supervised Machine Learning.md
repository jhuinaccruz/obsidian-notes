>*Supervised machine learning generally accomplishes one of two tasks:*
>- *Classification*
>- *Regression*

__Classification__: Identifying categories of things

__Regression__: Fitting a function (typically with a numerical output) to some data

## K-Nearest Neighbors
>*To find the correct classification of a point, we consult its neighbors - the k closest examples that it does have a label for. If they all agree on their own classification, then this is a very good guess for the new point. But if they disagree, then they must vote, and the majority rule determines the label*

>**

$$
d = \sqrt{\Delta{x}_1^2 + \Delta{x}_2^2 + ... \Delta{x}_n^2} 
$$

Where:
- d = distance (measuring closeness between data vectors) 
## Train/Test Split and Overfitting
>*In general, most classifiers...shouldn't evaluate solely on...training data, or the results won't give a sense of how well you do on genuinely new data points.*

>*In fact, many algorithms run the risk of getting too cozy with the training data and overfitting to its idiosyncracies*

__Overfitting__: When machines learn rules that only happen to be true of the training data in particular

>*So, at the very least, you must split the data into training and testing data.*

## Validation Data
>*...once you've looked at the test data, any changes you make could start creating improvement that doesn't carry over to the real world. Your choices from here on out could cause overfitting to the test data*

>*A way to avoid this problem is to split the training data yet again, splitting off a portion of the training data to be "validation data"*

>*A still more clever idea is to rotate which fraction of your training data is the validation set. So you train on the first 80 and then test on 20%, then train on the first 60% and last 20%, while training on that missing 20%, and so on 5 times. ideally, this is still separate from the test data, which is reserved for final testing. This is called "cross-validation"*

