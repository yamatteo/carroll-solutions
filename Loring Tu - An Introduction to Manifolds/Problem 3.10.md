> Let $\alpha^1, \ldots, \alpha^k$ be $1$-covectors on a vector space $V$. Show that $\alpha^1 \wedge \cdots \wedge \alpha^k \neq 0$ if and only if $\alpha^1, \ldots, \alpha^k$ are linearly independent in the dual space $V^\vee$.

If these covectors are linearly dependent, there is a combination of them that's equal to $0$. Without loss of generality we can assume that $\alpha^k = \sum_{i=1}^{k-1} a_i \alpha^i$. Then
$$\alpha^1 \wedge \cdots \wedge \alpha^k = \sum_{i=1}^{k-1} a_i (\alpha^1\wedge\dots\wedge \alpha^{k-1} \wedge \alpha^i) = 0$$
On the other hand, suppose $\alpha^1 \wedge \cdots \wedge \alpha^k = 0$ but $\alpha^2 \wedge \cdots \wedge \alpha^{k} \neq 0$. There are vectors $w_2, \dots, w_k$ such that $(\alpha^2 \wedge \cdots \wedge \alpha^{k})(w_2, \dots, w_k) \neq 0$. We therefore have 
$$\begin{eqnarray}
0 &&= (\alpha^1 \wedge \cdots \wedge \alpha^k)(w_1, \dots, w_k) \\
&&= \sum_{\sigma \in S_k} \text{sgn}(\sigma) \alpha^1(w_{\sigma(1)}) \cdots \alpha^k(w_{\sigma(k)}) \\
&&= \sum_{\sigma \in S_k} \text{sgn}(\sigma) \alpha^{\sigma(1)}(w_1) \cdots \alpha^{\sigma(k)}(w_k) \\
&&= \sum_{j=1}^k \left( \sum_{\sigma\in S_k | \sigma(1)=j} \text{sgn}(\sigma) \alpha^{\sigma(2)}(w_2) \cdots \alpha^{\sigma(k)}(w_k)\right) \alpha^j(w_1)
\end{eqnarray}$$
which is a linear combination of $\alpha^1, \dots, \alpha^k$ applied on the generic vector $w_1$, whose coefficient are independent of $w_1$ and not all, because at least for $j=1$ we have the coefficient $(\alpha^2 \wedge \cdots \wedge \alpha^{k})(w_2, \dots, w_k) \neq 0$