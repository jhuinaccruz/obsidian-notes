__Shear Matrix__: Performs a linear transformation (`R^2`) by shifting points in a direction parallel to a fixed axis
- Horizontal Shear (shifts `x` coordinates while keeping `y` fixed $$\begin{bmatrix}1 \ s_x \\ 0 \ 1\end{bmatrix}$$
- Vertical Shear (shifts `y` coordinates while keeping `x` fixed) $$\begin{bmatrix}1 \ 0 \\ s_y \ 1\end{bmatrix}$$
where `s` is the shear factor

__Reflection__: Mirroring through an axis
- Reflection over `x`-axis $$\begin{bmatrix}1 \ 0 \\ 0 \ -1\end{bmatrix}$$
- Reflection over `y`-axis $$\begin{bmatrix}-1 \ 0 \\ 0 \ 1\end{bmatrix}$$
- Reflection over `y=x` $$\begin{bmatrix}0 \ 1 \\ 1 \ 0\end{bmatrix}$$
- Reflection over `y = -x` $$\begin{bmatrix}0 \ -1 \\ -1 \ 0\end{bmatrix}$$

__Projection__: Putting it onto an axis
- Projection onto the `x`-axis $$\begin{bmatrix}1 \ 0 \\ 0 \ 0\end{bmatrix}$$

__Rotation__: Transformation that rotates each points about the origin through an angle `Ø`