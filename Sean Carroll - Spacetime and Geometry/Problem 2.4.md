> Verify the claims made about the commutator of two vector fields at the end of Section 2.3 (linearity, Leibniz, component formula, transformation as a vector field).

Linearity and Liebniz properties come from the same properties of vectors: $X(af + bg) = a X(f) + b X(g)$ and $X(fg) = X(f)g + fX(g)$. Apply them to $X$ and $Y$ to get those properties for $[X, Y]$.

If we derive the coordinate functions we get the components of the vector, so
$$\begin{array}{rcl}
[X, Y](x^\mu) & = & X(Y(x^\mu)) - Y(X(x^\mu)) \\
& = & X(Y^\lambda \partial_\lambda x^\mu) - Y(X^\lambda \partial_\lambda x^\mu) \\
& = & X(Y^\mu) - Y(X^\mu) \\
& = & X^\lambda \partial_\lambda Y^\mu - Y^\lambda \partial_\lambda X^\mu \\
& & \text{then changing to other coordinates} \\
& = & \frac{\partial x^{\lambda}}{\partial x^{\lambda'}}X^{\lambda'} \frac{\partial x^{\lambda'}}{\partial x^{\lambda}}\partial_{\lambda'} \frac{\partial x^{\mu}}{\partial x^{\mu'}}Y^{\mu'} - \frac{\partial x^{\lambda}}{\partial x^{\lambda'}}Y^{\lambda'} \frac{\partial x^{\lambda'}}{\partial x^{\lambda}}\partial_{\lambda'} \frac{\partial x^{\mu}}{\partial x^{\mu'}}X^{\mu'} \\
& = & X^{\lambda'} \partial_{\lambda'} \frac{\partial x^{\mu}}{\partial x^{\mu'}}Y^{\mu'} - Y^{\lambda'} \partial_{\lambda'} \frac{\partial x^{\mu}}{\partial x^{\mu'}}X^{\mu'} \\
& = & X^{\lambda'} \left( \frac{\partial^2 x^{\mu}}{\partial x^{\lambda'} \partial x^{\mu'}}Y^{\mu'} + \frac{\partial x^{\mu}}{\partial x^{\mu'}} \partial_{\lambda'} Y^{\mu'}\right)  - Y^{\lambda'} \left( \frac{\partial^2 x^{\mu}}{\partial x^{\lambda'} \partial x^{\mu'}}X^{\mu'} + \frac{\partial x^{\mu}}{\partial x^{\mu'}} \partial_{\lambda'} X^{\mu'}\right) \\
& = & \frac{\partial x^{\mu}}{\partial x^{\mu'}} \left(  X^{\lambda'} \partial_{\lambda'} Y^{\mu'}  - Y^{\lambda'} \partial_{\lambda'} X^{\mu'}\right) \\
& = & {\Lambda^\mu}_{\mu'} [X, Y](x^{\mu'})
\end{array}$$