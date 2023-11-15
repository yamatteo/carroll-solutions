> Prolate spheroidal coordinates can be used to simplify the Kepler problem in celestial mechanics. They are related to the usual cartesian coordinates $(x, y, z)$ of Euclidean three-space by $$\begin{eqnarray}x &=& \sinh\chi \sin \theta \cos \phi \\y &=& \sinh \chi \sin \theta \sin \phi \\z &=& \cosh \chi \cos \theta \end{eqnarray}$$
> Restrict your attention to the plane $y = 0$ and answer the following questions.
> **(a)** What is the coordinate transformation matrix $\partial x^\mu / \partial x^{\nu'}$ relating $(x, z)$ to $(\chi, \theta)$?
> **(b)** What does the line element $ds^2$ look like in prolate spheroidal coordinates?

Let's just list them:
$$\begin{eqnarray}
\frac{\partial x}{\partial \chi} =& \cosh \chi \sin \theta \\
\frac{\partial x}{\partial \theta} =& \sinh \chi \cos \theta \\
\frac{\partial z}{\partial \chi} =& \sinh \chi \cos \theta \\
\frac{\partial z}{\partial \theta} =& -\cosh \chi \sin \theta
\end{eqnarray}$$
And the line element is 
$$\begin{eqnarray}
ds^2 &=& dx^2 + dz^2 \\
&=& \left(\frac{\partial x}{\partial \chi}d\chi + \frac{\partial x}{\partial \theta}d\theta\right)^2 + \left(\frac{\partial z}{\partial \chi}d\chi + \frac{\partial z}{\partial \theta}d\theta\right)^2 \\
&=& \left(\cosh^2 \chi \sin^2 \theta + \sinh^2 \chi \cos^2 \theta\right)\left(d\chi^2 + d\theta^2\right) \\ 
&=& \left(\sin^2 \theta + \sinh^2 \chi\right)\left(d\chi^2 + d\theta^2\right) 

\end{eqnarray}$$