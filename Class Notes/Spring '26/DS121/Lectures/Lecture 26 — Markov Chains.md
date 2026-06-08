__Markov Chains__: Systems that moves between states in discrete time steps (1, 2, 3...), the set of states is finite, and can only be in one state at a time
- The state of the system at time $k$ is denoted as $$\forall x_k \in R^n\land n≥0,\ x_{k+1} = Ax_k$$
- Markov chains can be defined as a system whose state is a probability vector that changes based on a stochastic matrix, denoted as $$x_k = P(x_{k-1}) = ...=P^kx_0$$
	- __Probability Vector__ ($x$): Contains non-negative entries that sum up to 1
		- Describes how things are distributed across various categories
		- __Initial State Vector__ ($x_0$): The first probability vector; describes the initial distribution of objects in each state at the beginning of a system
	- __Stochastic__ (Transition) __Matrix__ ($P$): Square matrix whose columns sum up to 1
		- Describes changes at each time step
- __Steady State Vector__ ($q$): A probability vector such that $Pq = q$
	- Every stochastic matrix has at least one steady-state vector
		- In other words, for every Stochastic matrix, there is a limit where continued Markov chain calculations result in the same probability vector being returned
		- Some may have more than one steady-state vector
	- To find the steady-state vector:
		1. Rewrite $Pq = q$ as $$(P-I)x = 0$$ and solve for the augmented matrix
			- If the vector results in an infinite set of solutions, input a random value to get a set of solutions, then divide by the sum of the set's values

>*Markov Chains are useful for analyzing stock price movements, dynamics of animal populations, and implemented in the PageRank algorithm*

>*The largest eigenvalue of a Markov Chain is 1*