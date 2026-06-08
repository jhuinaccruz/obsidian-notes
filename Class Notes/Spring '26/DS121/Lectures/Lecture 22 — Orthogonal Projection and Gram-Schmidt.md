__Projection__: (Also known as coordinate computation) Given two vectors $\vec{y}$ and $\vec{u}$, decomposes $y$ into the sum of two vectors $y = \hat{y} + z$  so that
- The orthogonal projection $\hat{y}=\alpha u$ for some scalar $\alpha$
	- $\alpha = \frac{y^\top u}{u^\top u} \implies \hat{y}=\frac{y^\top u}{u^\top u} u$
	- $\hat{y} = \operatorname{proj}_Ly$ 
- The orthogonal component $z$ multiplied by $u$ equals 0
	- $z = y - \hat{y} = y - \alpha u$

>*The projection...is determined by... $\operatorname{Span}\{u\}$, not the vector $u$* 

__Distance to a subspace__: The distance from $y$ to $L$, or the length of the perpendicular from $y$ to its orthogonal projection on $L$ ($\hat{y}$), calculated as $y - \hat{y}$ (also called the norm of $z$)
$$
||y - \hat{y}|| = ||z||
$$
