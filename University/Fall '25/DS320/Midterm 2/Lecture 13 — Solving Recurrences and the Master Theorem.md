__Recurrence__ (Running Time Intuition through Trees): Trees can be made of recursive calls made by the algorithm and the work done at each stage, such that the tree itself can be an intuition into the running time of the algorithm, denoted by the formula
$$
T(n) = \alpha T(n/b) + f(n)
$$
where
- alpha = the number of subproblems we make a call to
- n/b is the size of the subproblem
- f(n) the running time to divide and combine the subproblems

__Master Theorem__ (for Divide and Conquer runtime): 
$$
\forall a ≥ 1, \forall b > 1, T(n) = aT(n/b) + f(n), \epsilon > 0
$$
1. Case 1:
$$
f(n) = O(n^{log_ba - \epsilon}) \implies T(n) = \Theta(n^{log_ba})
$$
2. Case 2:
$$
f(n) = \Theta(n^{log_ba}) \implies T(n) = \Theta(n^{log_ba}\ log_2n)
$$
3. Case 3:
$$
c < 1.\ f(n) = \Omega(n^{log_ba + \epsilon})\ \land\ af(n/b) ≤ cf(n)) \implies T(n) = \Theta(f(n))
$$