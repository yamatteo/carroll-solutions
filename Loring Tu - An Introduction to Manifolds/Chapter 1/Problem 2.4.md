> Let $A$ be an [[Algebra over field|algebra over a field]] $K$. If $D_1$ and $D_2$ are [[Derivations|derivations]] of $A$, show that $D_1∘D_2$ is not necessarily a derivation (it is if $D_1$ or $D_2=0$), but $D_1∘D_2 - D_2∘D_1$ is always a derivation of $A$.

It can be proved that $D_1 \circ D_2$ is still a linear map from $A$ to $A$, but it does not satisfy the Liebniz rule, in general.
$$\begin{eqnarray}
(D_1 \circ D_2)(fg) &=& D_1((D_2 f)g + f(D_2 g)) \\
&=& (D_1 D_2 f)g + (D_2 f)(D_1 g) + (D_1 f)(D_2 g) + f(D_1 D_2 g)
\end{eqnarray}$$
But if we consider $D_1∘D_2 - D_2∘D_1$, the mixed terms cancel out and the Liebniz rule holds without further assumption on $D_1$ or $D_2$.