__Decision Trees__: Machine learning that builds a classifier in response to data that is distinct from the data, taking on the form of a tree

>*When classifying, the algorithm starts at the top, asks the first question, and moves left or right as a result of the answer being yes or no. The questions continue until a leaf is reached, and that is the classification*

>*Decision trees have the advantage of being inspectable and transparent compared to other methods.*

>*However, this is also a limitation, as the classifier needs to stick closely with the original features of the dataset when coming up with its new rules; it can't come up with new unintuitive features as easily as a neural network*

### Construction of Decision Trees
__Greedy__: A term for algorithms that try to do the best looking thing in the moment, without rethinking earlier decisions

>*What makes for a good decision? Ideally, it's a decision that makes it so that examples that answer "yes" all agree on their classification, and examples that answer "no" all agree on their classification

## Entropy
__Entropy__: A measure of how much surprise is possible in a stream of symbols
$$
\sum_{i} -p_{i} log_{2}p_{i}
$$
where p<sub>i</sub> = frequency of the symbol (from 0-1)

$$
Pr(yes)Entropy(yes) + Pr(no)Entropy(no)
$$
>*... where Pr(yes/no)  = count of examples answering "yes/no" to decision / count of both "yes" and "no" examples"*

