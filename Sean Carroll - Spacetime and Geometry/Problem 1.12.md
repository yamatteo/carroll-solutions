>Consider the two field theories we explicitly discussed, Maxwell's electromagnetism (let $J^\mu = 0$) and the scalar field theory defined by $\mathcal L = - \frac12 \eta^{\mu\nu}(\partial_\mu \phi)(\partial_\nu \phi) - V(\phi)$.
> **(a)** Express the component of the energy-momentum tensor of each theory in three-vector notation, using the divergence, gradient, curl, electric, and magnetic fields, and an overdot to denote time derivatives.
> **(b)** Using the equation of motion, verify (in any notation you like) that the energy-momentum tensors are conserved.

#### Scalar field
As shown in the book (equation 1.170), the energy-momentum tensor is 
$$T^{\mu\nu}  = \eta^{\mu\lambda}\eta^{\nu\sigma}\partial_\lambda\phi\partial_\sigma\phi-\eta^{\mu\nu}\left[\frac12 \eta^{\lambda\sigma}\partial_\lambda\phi \partial_\sigma \phi + V(\phi)\right]$$
By components, $$ T^{00} = \dot\phi^2 + \frac12\left(\nabla\phi\cdot\nabla\phi - \dot\phi^2\right) + V(\phi) = \frac12 \nabla\phi\cdot\nabla\phi + \frac12 \dot\phi^2 + V(\phi)$$
And $T^{0i} = T^{i0} = -\dot\phi \partial_i\phi$ so we can say that $T^0 = -\dot\phi \nabla\phi$ is a three-vector. On the diagonal $T^{ii} = (\partial_i \phi)^2 - \frac12\left(\nabla\phi\cdot\nabla\phi - \dot\phi^2\right) - V(\phi)$ 

$$\begin{eqnarray}
T^{\mu\nu} & = & \eta^{\mu\lambda}\eta^{\nu\sigma}\partial_\lambda\phi\partial_\sigma\phi-\eta^{\mu\nu}\left[\frac12 \eta^{\lambda\sigma}\partial_\lambda\phi \partial_\sigma \phi + V(\phi)\right] \\
& = & (-1)^{(\mu=0)+(\nu=0)}\partial_\mu\phi\partial_\nu\phi
-\eta^{\mu\nu}\left[\frac12 (\nabla\phi\cdot\nabla\phi - \dot\phi^2) + V(\phi)\right] \\
& = & \frac12 \left(
(-1)^{(\mu=0)+(\nu=0)}2\partial_\mu\phi\partial_\nu\phi
-\eta^{\mu\nu}\nabla\phi\cdot\nabla\phi + \eta^{\mu\nu}\dot\phi^2
\right)- \eta^{\mu\nu} V(\phi) \\
& = & \frac12 \left(
(-1)^{(\mu=0)}(-1)^{(\nu=0)}2\partial_\mu\phi\partial_\nu\phi
+(-1)^{(\mu=0)}\delta^\mu_\nu(-\nabla\phi\cdot\nabla\phi + \dot\phi^2)
\right)- \eta^{\mu\nu} V(\phi) \\
& = & (-1)^{(\mu=0)}\frac12 \left(
(-1)^{(\nu=0)}2\partial_\mu\phi\partial_\nu\phi
+\delta^\mu_\nu(-\nabla\phi\cdot\nabla\phi + \dot\phi^2)
\right)- \eta^{\mu\nu} V(\phi)
\end{eqnarray}$$
#### Electromagnetism
