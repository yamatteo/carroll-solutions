> At each point $p \in \mathbb{R}^3$, define a bilinear function $\omega_p$ on $T_p(\mathbb{R}^3)$ by
> $\omega_p(\textbf a, \textbf b) = \omega_p\left(\left[\begin{array}{c}a_1\\a_2\\a_3\end{array}\right], \left[\begin{array}{c}b_1\\b_2\\b_3\end{array}\right]\right) = p_3\,\det\left[\begin{array}{cc}a_1 & b_1\\a_2 & b_2\end{array}\right]$,
> for tangent vectors $\textbf a, \textbf b \in T_p(\mathbb{R}^3)$, where $p = (p_1, p_2, p_3)$. Since $\omega_p$ is an alternating bilinear function on $T_p(\mathbb{R}^3)$, $\omega$ is a 2-form on $\mathbb{R}^3$. Write $\omega$ in terms of the standard basis $dx^i \wedge dx^j$ at each point.

We should think of $\textbf a$ as $(a^1 \frac{\partial}{\partial x^1} + a^2 \frac{\partial}{\partial x^2} + a^3 \frac{\partial}{\partial x^3})$ and for $\textbf b$ as well. We can write
$$\begin{eqnarray}
\omega (\textbf a, \textbf b) =&& x^3 (a^1 b^2 - a^2 b^1) \\
=&& x^3 \cdot \left[ a^1 dx^1\frac{\partial}{\partial x^1} b^2 dx^2\frac{\partial}{\partial x^2} - a^2  dx^2 \frac{\partial}{\partial x^2} b^1 dx^1\frac{\partial}{\partial x^1} \right] \\
=&& x^3 \cdot \left[ (dx^1 \otimes dx^2)(\textbf a, \textbf b) - (dx^2 \otimes dx^1)(\textbf a, \textbf b)\right] \\
=&& \left(x^3 (dx^1 \wedge dx^2)\right)(\textbf a, \textbf b)
\end{eqnarray}$$