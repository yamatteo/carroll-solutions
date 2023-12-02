> Let $V$ be a vector space. For $a, b \in \mathbb{R}$, $f \in A_k(V)$, and $g \in A_l(V)$, show that $a f \wedge b g = (ab) f \wedge g$.

By definition,
$$\begin{eqnarray}
af \wedge bg &=& \frac{1}{k!l!}\sum_{\sigma \in S_{k+l}} \text{sgn}(\sigma)\sigma(af \otimes bg) \\
&=& a b \frac{1}{k!l!}\sum_{\sigma \in S_{k+l}} \text{sgn}(\sigma)\sigma(f \otimes g) \\ \\
&=& a b (f \wedge g)
\end{eqnarray}$$