> Suppose the standard coordinates on $\mathbb{R}^3$ are called $\rho$, $\phi$, and $\theta$. If $x = \rho\sin\phi\cos\theta$, $y = \rho\sin\phi\sin\theta$, and $z = \rho\cos\phi$, calculate $dx$, $dy$, $dz$, and $dx \wedge dy \wedge dz$ in terms of $d\rho$, $d\phi$, and $d\theta$.

As before, directly,
$$\begin{eqnarray}
dx &=& \sin\phi\cos\theta d\rho &+ \rho \cos\phi\cos\theta d\phi &- \rho\sin\phi\sin\theta d\theta \\  
dy &=& \sin\phi\sin\theta d\rho &+ \rho \cos\phi\sin\theta d\phi &+ \rho\sin\phi\cos\theta d\theta \\ 
dz &=& \cos\phi d\rho &- \rho \sin\phi d\phi \\ 
\end{eqnarray}$$
And so, jumping some steps,
$$\begin{eqnarray}
dx\wedge dy\wedge dz &=& -\rho^2\sin^3\phi\cos^2\theta(d\rho \wedge d\theta \wedge d\phi) \\
&&+ \rho^2\sin\phi\cos^2\phi\cos^2\theta (d\phi \wedge d\theta \wedge d\rho) \\
&&+ \rho^2\sin\phi\sin^2\theta(d\theta \wedge d\rho \wedge d\phi) \\
&=&\rho^2 \sin\phi\left( d\rho \wedge d\phi \wedge d\theta\right)
\end{eqnarray}$$