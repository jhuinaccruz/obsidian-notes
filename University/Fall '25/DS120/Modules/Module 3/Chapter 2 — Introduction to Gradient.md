__Gradient of a Multivariable Function__: A vector that packages all the partial derivatives of a function, denoted by
$$
\nabla f = \begin{bmatrix}\frac{\partial{f}}{\partial{x}} \\
\frac{\partial{f}}{\partial{y}} \\...
\end{bmatrix}
$$
__Unit Vector__ (In the direction of v): Defined as u, or
$$
\vec{u} = \frac{1}{|\vec{v}|}\begin{bmatrix}v_1 \\v_2\end{bmatrix} = \begin{bmatrix}u_1 \\ u_2\end{bmatrix} = \frac{\nabla f}{|\nabla{f}|}
$$


__Directional Derivative__: Taken along some vector v in the input space, or the rate of change of f as you nudge along the direction of vector v, denoted by
$$
\nabla_{\vec{v}}f \iff \frac{\partial{f}}{\partial{\vec{v}}} \iff f'_v \iff D_\vec{v}f \iff \partial_{\vec{v}}f = \nabla f(x_0, y_0) / \vec{u}
$$
$$
\nabla_{\vec{u}}f(x_0,y_0) = \frac{\partial f(x_0,y_0)}{d_x}u_1 + \frac{\partial f(x_0,y_0)}{d_y}u_2 = \nabla{f(x_0,y_0)*\vec{u}}
$$
1. Find the unit vector u in the direction of vector v
2. Find the gradient vector
3. Find the gradient vector in the direction of the coordinates
4. Multiply the gradient vector in the direction of the coordinates by the unit vector

__Maximizing a Directional Derivative__:
$$
\nabla_\vec{u}{f} = |\nabla{f}||\vec{u}|\cos(\theta).\cos\theta = 1
$$
