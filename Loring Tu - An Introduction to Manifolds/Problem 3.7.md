> Suppose two sets of covectors on a vector space $V$, $\beta^1, \ldots, \beta^k$ and $\gamma^1, \ldots, \gamma^k$, are related by
> $$\beta^i = \sum_{j=1}^k {a^i}_j \gamma^j, \quad i = 1, \ldots, k,$$
> for a $k \times k$ matrix $A = [{a^i}_j]$. Show that
> $$\beta^1 \wedge \cdots \wedge \beta^k = (\det A)\gamma^1 \wedge \cdots \wedge \gamma^k.$$

Let's start substituting $\beta^i$ with $\sum_{j_i=1}^k {a^1}_{j_i} \gamma^j$. By linearity
$$\beta^1 \wedge \cdots \wedge \beta^k = \sum_{j_1=1}^k \cdots \sum_{j_k = 1}^k {a^1}_{j_1}\cdots{a^k}_{j_k} (\gamma^{j_1} \wedge \cdots \wedge \gamma^{j_k})$$
Since the wedge product is alternating, we can assume that all $j_1, \dots, j_k$ are distinct and write the previous multisum as
$$\begin{eqnarray}
\beta^1 \wedge \cdots \wedge \beta^k =&& \sum_{\sigma \in S_k} {a^1}_{\sigma(1)}\cdots{a^k}_{\sigma(k)} (\gamma^{\sigma(1)} \wedge \cdots \wedge \gamma^{\sigma(k)})\\
=&& \left(\sum_{\sigma \in S_k} \text{sgn}(\sigma) {a^1}_{\sigma(1)}\cdots{a^k}_{\sigma(k)}\right) (\gamma^{1} \wedge \cdots \wedge \gamma^{k})
\end{eqnarray}$$
Which is a proper definition of the determinant of $A$.