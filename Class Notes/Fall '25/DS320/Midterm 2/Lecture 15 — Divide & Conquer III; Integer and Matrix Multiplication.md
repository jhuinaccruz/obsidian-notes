>*Your input for the integer multiplication problem is two n-digit numbers x and y. The goal is to output their product, x \* y*

The naive solution to Integer Multipiication is: `O(n^2)`

__Karatsuba's Algorithm__: For the multiplication of some digits x and y
$$
xy = (a \times 10^{n/2} + b)(c\times 10^{n/2} + d)
$$
The resulting time complexity of said algorithm is about `O(n^1.58)`

__Matrix Multiplication__:
- Naively: `O(n^3)`, since for a 2\*2 matrix:
$$
\begin{bmatrix} A \ B \\ C \ D \end{bmatrix} \begin{bmatrix} E \ F \\ G \ H \end{bmatrix} = \begin{bmatrix} AE + BG \ AF + BH \\ CE+ DG \ CF + DH \end{bmatrix}
$$
	This leads to a recurrence of
$$
T(n) = 8T(n/2) + \Theta(n^2) = \Theta(n^3)
$$
- __Strassen's Algorithm__: Where there are 7 steps instead of 8, by computing the following:
	- P1 = A(F - H)
	- P2 = (A + B)H
	- P3 = (C + D)E
	- P4 = D(G - E)
	- P5 = (A+D) (E + H)
	- P6 = (B - D) (G + H)
	- P7 = (A - C) (E + F)
	such that the same multiplication for a 3\*3 matrix becomes
$$
\begin{bmatrix} (P5 + P4 - P2 + P6) \ (P1 + P2) \\ (P3 + P4) \ (P5 + P1 - P3 - P7) \end{bmatrix}
$$
	The recurrence for Strassen's Algorithm takes the form of
$$
T(n) = 7T(n/2) + \Theta(n^2) = O(n^{log_27}) \approx O(n^{2.8074})
$$

