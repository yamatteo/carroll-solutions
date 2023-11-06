>Verify that $\partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} = 0$ is indeed equivalent to $\partial_{[\mu} F_{\nu\lambda]} = 0$, and that they are both equivalent to the set of equations $\tilde\epsilon^{ijk} \partial_j E_k + \partial_0 B^i = 0$ and $\partial_i B^i = 0$.

By definition $$\begin{eqnarray}
\partial_{[\mu} F_{\nu\lambda]} & = & \frac16 \left(\partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} - \partial_\mu F_{\lambda\nu} - \partial_\nu F_{\mu\lambda} - \partial_\lambda F_{\nu\mu}\right) \\
 & & \text{by the anti-symmetry of } F_{\mu\nu} \\
 & = & \frac16 \left(\partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} + \partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu}\right) \\
 & = & \frac13 \left(\partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu}\right)
\end{eqnarray}$$
so if one is zero, so is the other. Then consider that for any value of $\mu$, $\nu$ and $\lambda$, each permutation of those values give back the same equation in $\partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} = 0$. So let's consider first the spatial values $\{1, 2, 3\}$. Expanding on the definition of $F_{\mu\nu}$ we find $$\begin{eqnarray}
0 & = & \partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} \\
& = & \partial_1 F_{23} + \partial_2 F_{3 1} + \partial_3 F_{1 2} \\
& = & \partial_1 B_1 + \partial_2 B_2 + \partial_3 B_3 \\
& & \text{being that } B_i = B^i\\
& = & \partial_i B^i
\end{eqnarray}$$
Then, consider indices $\{0, 2, 3\}$, we get $$\begin{eqnarray}
0 & = & \partial_\mu F_{\nu\lambda} + \partial_\nu F_{\lambda \mu} + \partial_\lambda F_{\mu \nu} \\
& = & \partial_0 F_{23} + \partial_2 F_{3 0} + \partial_3 F_{0 2} \\
& = & \partial_0 B_1 + \partial_2 E_3 - \partial_3 E_2
\end{eqnarray}$$ and similarly, sets $\{0, 1, 3\}$ and $\{0, 1, 2\}$ gives the other equations in $\tilde\epsilon^{ijk} \partial_j E_k + \partial_0 B^i = 0$.
On the other hand, if we take repeating indices, we already know it is $0$ becase of the equivalence with $\partial_{[\mu} F_{\nu\lambda]} = 0$.