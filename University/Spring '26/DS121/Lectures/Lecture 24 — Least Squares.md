__Least-Squares Problem__: Find $\vec{x}$ that makes $||Ax - b||$ as small as possible, such that we minimize the total squared length of the residuals, or the error difference between estimated value and actual value
$$
||Ax - b||^2 = \sum_i(y_i - b_i)^2
$$
- where $y_i$ is the estimated value and $b_i$ is the measured value
- *Solution*: If $A$ is $m\times n$ and $b$ is in $\mathbb{R}^m$, the solution is $\hat{x}$ in $\mathbb{R}^n$ such that $||A\hat{x} - b|| ≤ ||Ax - b||$ for all $x$ in $\mathbb{R}^n$
	- In other words, $b$ is outside $\text{Col }A$, and $\top{x}$ specifies the closest point in $\text{Col }A$ to $b$
	- The residual $b - A\hat{x}$ is perpendicular to $\text{Col }A$
	- The set of least-squares solutions of $Ax = b$ is equal to the nonempty set of solutions, denoted as $$Ax = b \implies A^\top Ax = A^\top b$$