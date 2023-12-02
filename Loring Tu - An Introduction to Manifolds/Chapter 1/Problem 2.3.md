> Let $D$ and $D'$ be [[Derivations|derivations]] at $p$ in $\mathbb{R}^n$, and $c \in \mathbb{R}$. Prove that
> (a) the sum $D + D'$ is a derivation at $p$.
> (b) the scalar multiple $cD$ is a derivation at $p$.

We should prove first that $D+D'$ and $cD$ are still linear map from $C_p^\infty$ to $\mathbb R$. It is straightforward:
$$\begin{eqnarray}
(D + D')(af + bg) &=& D(af + bg) + D'(af + bg) \\
&=& aDf + bDg + aD'f + bD'g \\
&=& a(D+D')f + b(D+D')g
\end{eqnarray}$$
Then we should prove that this linear map satisfy the Liebniz rule, so
$$\begin{eqnarray}
(D+D')(fg) &=& D(fg) + D'(fg) \\
&=& (Df)g + f(Dg) + (D'f)g + f(D'g) \\
&=& ((D+D')f)g + f((D+D')g)
\end{eqnarray}$$
The same goes for scalar multiplication.