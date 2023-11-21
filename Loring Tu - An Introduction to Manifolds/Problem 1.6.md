> Prove that if $f: \mathbb R^2 \to \mathbb R$ is $C^\infty$, then there exist $C^\infty$ functions $g_{11}, g_{12}, g_{22}$ on $\mathbb R^2$ such that
> $$\begin{eqnarray}
f(x, y) = f(0, 0) && + \frac{\partial f}{\partial x}(0, 0)x + \frac{\partial f}{\partial y}(0, 0)y \\
&&+ x^2 g_{11}(x ,y) + xyg_{12}(x, y) + y^2 g_{22}(x, y)
\end{eqnarray}$$

We are going to use the "Taylor's theorem with reminder" lemma with $U = \mathbb R^2$ as open subset (obviously star-shaped) and $P = (0, 0)$ as point. Using the lemma once we get two $C^\infty$ function, $g_1$ and $g_2$ such that
$$f(x, y) = f(0, 0) + x g_1(x, y) + y g_2(x, y)$$
We need to prove that $g_1(0, 0) = \partial f / \partial x(0, 0)$. By definition of partial derivative and using the continuity of $g_1$,
$$\begin{eqnarray}
\frac{\partial f}{\partial x}(0, 0) = \lim_{t \to 0} \frac{f(t, 0) - f(0, 0)}{t} = \lim_{t \to 0} g_1(t, 0) = g_1(0, 0)
\end{eqnarray}$$
The same goes for $g_2$.

Using the lemma again, both on $g_1$ and $g_2$ we get four $C^\infty$ function, temporarily named $h_{11}, h_{12}, h_{21}, h_{22}$, such that
$$\begin{eqnarray}
f(x, y) &= f(0, 0) & + x\left(g_1(0, 0) + x h_{11}(x ,y) + y h_{12}(x, y)\right)\\
&&+ y\left(g_2(0, 0) + x h_{21}(x ,y) + y h_{22}(x, y)\right) \\
&= f(0, 0) &+ \frac{\partial f}{\partial x}(0, 0)x + \frac{\partial f}{\partial y}(0, 0)y\\
&&+x^2 h_{11}(x, y) + xy(h_{12}+h_{21})(x, y) + y^2h_{22}(x, y)
\end{eqnarray}$$
