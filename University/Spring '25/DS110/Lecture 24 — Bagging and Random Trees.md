## Bagging
__Bagging__ (Bootstrap Aggregation): Used to Reduce variance in a data set

### Sampling With Replacement
>*Instead of training one classifier train K with K different samples-with-replacement (of the same size as the original data)*


>*If original dataset had N points, draw N points for each new dataset, but draws are with replacements*

### Voting
>*Instead of training one classifier, train K with K different samples-with-replacement (of the same size as original data)*

>*Once trained, each trained classifier votes on new examples*

## Random Forests

>*Decision trees are often correlated in their responses, even after bagging. To further vary decision tree structure, some fraction of the attributes are used for potential splits*

>- *Train K trees instead of one*
>- *Extra work randomly sampling attributes to split on*
>- *sqrt(F) attributes to try instead of F per node*
>- *No need to prune the trees — the voting in the end mitigates overfitting*
>- *Highly parallelizable, since the trees can be trained apart from each other*

### Error
__Out-of-bag-Error__: Makes efficient use fo data points without need for a separate validation test by:
- For every training example, classifying the example using trees that were not trained with it
- Find the accuracy over all examples
