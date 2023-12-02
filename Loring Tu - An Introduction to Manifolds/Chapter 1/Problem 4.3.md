> Suppose the standard coordinates on $\mathbb{R}^2$ are called $r$ and $\theta$ (this $\mathbb{R}^2$ is the $(r, \theta)$-plane, not the $(x, y)$-plane). If $x = r\cos\theta$ and $y = r\sin\theta$, calculate $dx$, $dy$, and $dx \wedge dy$ in terms of $dr$ and $d\theta$.

If we think of $x(r, \theta) = r \cos \theta$ as a scalar function, then 
$$dx = \frac{\partial x}{\partial r} dr + \frac{\partial x}{\partial \theta} d\theta = \cos\theta dr - r\sin\theta d\theta$$
$$dy = \frac{\partial y}{\partial r}dr + \frac{\partial y}{\partial \theta}d\theta = \sin\theta dr + r\cos\theta d\theta$$
$$\begin{eqnarray}
dx \wedge dy =&& \left(\cos\theta dr - r\sin\theta d\theta\right) \wedge \left(\sin\theta dr + r\cos\theta d\theta\right) \\
=&& \cos\theta dr\wedge \left(\sin\theta dr + r\cos\theta d\theta\right) - r\sin\theta d\theta\wedge \left(\sin\theta dr + r\cos\theta d\theta\right) \\
=&& r\cos^2\theta (dr\wedge d\theta) - r\sin^2\theta (d\theta\wedge dr) \\
=&& r(dr \wedge d\theta)
\end{eqnarray}$$