> Consider $\mathbb R^3$ as a manifold with the flat Euclidean metric, and coordinates $x, y, z$. Introduce spherical polar coordinates $r, \theta, \phi$ related to $x, y, z$ by 
> $$\begin{array}{rcl} x &=& r \sin(\theta) \cos(\phi) \\ y &=& r \sin(\theta)\sin(\phi) \\ z &=& r\cos(\theta)\end{array}\tag{2.99}$$
> so that the metric takes the form $$ ds^2 = dr^2 + r^2 d\theta^2 + r^2 \sin^2 \theta d\phi^2 \tag{2.100}$$
> A particle moves along a parameterized curve given by $$x(\lambda) = \cos \lambda, \quad y(\lambda) = \sin \lambda, \quad z(\lambda) = \lambda \tag{2.101}$$
> Express the path of the curve in the $\{r, \theta, \phi\}$ system.
> Calculate the components of the tangent vector to the curve in both the Cartesian and spherical polar coordinate systems.

First $r = \sqrt{x^2 + y^2 + z^2} = \sqrt{\cos^2 \lambda + \sin^2 \lambda + \lambda ^2} = \sqrt{1 + \lambda^2}$, so that 
$$\begin{array}{rcl}
z &=& r \cos \theta \\
\lambda &=& \sqrt{1 + \lambda^2} \cos \theta \\
\arccos\left(\frac{\lambda}{\sqrt{1 + \lambda^2}}\right) &=& \theta
\end{array}$$
Then, since $r \sin\theta = \sqrt{x^2 + y^2} = \sqrt{\cos^2\lambda + \sin^2\lambda} = 1$, we identify $\phi = \lambda$.
For the tangent vector we calculate
$$\begin{eqnarray}
\frac{d}{d\lambda} &=& \frac{\partial x}{\partial \lambda}\partial_x + \frac{\partial y}{\partial \lambda}\partial_y + \frac{\partial z}{\partial \lambda}\partial_z \\ \\
&=& -\sin (\lambda) \partial_x + \cos(\lambda)\partial_y + \partial_z \\ \\ 
&=& -y \partial_x + x\partial_y + \partial_z
\end{eqnarray}$$
Or, on the other system, 

$$\begin{eqnarray}
\frac{d}{d\lambda} &=& \frac{\partial r}{\partial \lambda}\partial_r + \frac{\partial \theta}{\partial \lambda}\partial_\theta + \frac{\partial \phi}{\partial \lambda}\partial_\phi \\ \\
&=& \frac{\lambda}{\sqrt{1 + \lambda^2}} \partial_r - \frac{1}{1 + \lambda^2} \partial_\theta + \partial_\phi \\ \\
&=& \cos\theta \partial_r - \frac{1}{r^2}\partial_\theta + \partial_\phi
\end{eqnarray}$$