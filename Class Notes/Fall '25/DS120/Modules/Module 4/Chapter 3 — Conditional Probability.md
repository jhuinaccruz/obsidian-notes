__Conditional Probability__: Dynamic and based on changes (or potential thereof) from conditions imposed at the beginning of the experiment

__Conditional Probability Formula__:
$$
\Pr(A|B) = \frac{n(A\cap B)}{n(B)} = \frac{\frac{n(A\cap B)}{n(S)}}{\frac{n(B)}{n(S)}} = \frac{\Pr(A\cap B)}{\Pr{(B)}}
$$
read as *the conditional probability of A given B*
- when `Pr(A|B) = Pr(A)` `A` and `B` are independent
$$
\Pr(A|B) = Pr(A) \iff \Pr(B|A) = \Pr(B)
$$

__Bayes' Rule__: A formula for flipping conditional probabilities
$$
\Pr(B|A) = \frac{\Pr(A|B)\times \Pr(B)}{\Pr(A)}
$$
