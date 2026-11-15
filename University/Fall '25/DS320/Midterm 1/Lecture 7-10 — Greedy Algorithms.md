## I - Dijkstra's Algorithm
__Weight__: The value of an edge, defaulting to 1 when unweighted, otherwise considered weighted, denoted as
$$
w_e = w_{uv}
$$
where:
- w = weight value
- e  = edge name (can also be denoted by uv from (u, v))

__Greedy Stays Ahead Proof__: To prove a greedy algorithm's accuracy
1. Define the solutions the greedy algorithm takes, and the form some other solution takes
2. Find a measure by which greedy stays ahead of another solution being compared
3. Prove greedy stays ahead by said measure
4. Prove optimality

## II - Interval Scheduling

## III - Optimal Caching and Greedy Exchange
__Reduced Schedule__: When it does the minimal amount of work necessary in each step

__Greedy Exchange Argument__: Useful for proving some greedy algorithms find some optimal solution
1. Start from an arbitrary solution (the "greedy choice")
2. Prove the exchange argument, showing that there exists an optimal solution that includes the greedy choice
3. Prove optimal substructure, such that by induction, the greedy algorithm gives the optimal solution for the subproblem as well
## IV - Scheduling to Minimize Lateness