> In Euclidean three-space, let $p$ be the point with coordinates $(x, y, z) = (1, 0, -1)$. Consider the following curves that pass through $p$: $$x^i (\lambda) = (\lambda, (\lambda -1)^2, -\lambda) $$$$x^i(\mu) = (\cos \mu, \sin\mu, \mu - 1) $$$$x^i(\sigma) = (\sigma^2, \sigma^3 + \sigma^2, \sigma)$$
> **(a)** Calculate the components of the tangent vectors to these curves at $p$ in the coordinate basis $\{ \partial_x, \partial_y, \partial_z \}$.
> **(b)** Let $f = x^2 + y^2 - yz$. Calculate $df / d\lambda$, $df / d\mu$ and $df / d\sigma$.


Independently of the curves, the partial derivatives of $f$ are $\partial_i f = (2x, 2y - z, -y)$. 

Let's consider $\lambda$. When $\lambda = 1$ the curves pass through $p$. The tangent vector to the curve is $dx^i / d\lambda = (1, 2*(\lambda -1), -1) = (1, 0, -1)$. The ordinary derivative of $f$ along the curve is $df/d\lambda = \partial_i f d x^i / d\lambda = (2\lambda, 2(\lambda - 1)^2 + \lambda, -(\lambda - 1)^2) \cdot (1, 2(\lambda -1), -1)$ = $2\lambda +4(\lambda - 1)^2 + 2\lambda(\lambda -1)^2 + (\lambda - 1)^2  = 2$

The same calculations for the other cases.