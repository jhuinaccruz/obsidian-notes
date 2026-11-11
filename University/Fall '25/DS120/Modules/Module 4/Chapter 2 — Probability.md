__Probability__: A degree of certainty about a statement between 0 and 1 (or 0 and 100 in percents), where 0 is certainly not true and 1 is certainly true, denoted as
$$
Pr(\text{Event}) = x \iff P(\text{Variable}) = x
$$
where `x` is the degree of certainty

>*...the probabilities of all possible disjoint (non-overlapping) outcomes must sum to 1*

$$
\text{The probability of an event happening} = \frac{\text{Number of ways it can happen}}{\text{Total number of outcomes}} = \frac{|E|}{|S|}
$$
where `|E|` is the number of the desired outcomes and the `|S|` is the number of total outcomes

__Random Variables__: Associated with a set of possible outcomes and a distribution of probabilities

__Experiment__: A repeatable process with a set of possible outcomes

__Outcome__: A possible result of an experiment

__Trial__: A single performance of an experiment

__Sample Space__: All possible outcomes of an experiment

__Sample Point__: One of the possible outcomes

__Event__: One or more outcomes of an experiment
- __Independent__: When an event doesn't influence the occurrence of the other, and vice versa

$$
Pr(\text{A and B and C and...}) = Pr(A) \times Pr(B) \times Pr(C) \times \text{...}
$$

__Binomial Distribution__: A discrete probability distribution for experiments with only two outcomes
- `p`: Probability of success
- `q`: Probability of failure
$$
q = 1 - p
$$
- Bernoulli trial: An iteration of an experiment involving only two outcomes
- `n`: Number of Bernoulli trials
- `r`: Number of successes
- Repetition: Conditions remain the same for each trial, such that `p` and `q` are constant across all trials
$$
\Pr(\text{Event}) = \text{Number of ways an event can occur}\ \times \Pr(\text{One occurrance})
$$

__Binomial Distribution Formula__:
$$
\Pr(X = r;\ n,\ p) = C(n,\ r) p^r (1-p)^{n-r} = \frac{n!}{r!(n-r)!} p^r (1-p)^{n-r}
$$