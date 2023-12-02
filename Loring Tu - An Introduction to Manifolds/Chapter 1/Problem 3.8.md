> Let $f$ be a $k$-covector on a vector space $V$. Suppose two sets of vectors $u_1, \ldots, u_k$ and $v_1, \ldots, v_k$ in $V$ are related by
> $$u_j = \sum_{i=1}^k {a^i}_j v_i, \quad j = 1, \ldots, k,$$
> for a $k \times k$ matrix $A = [{a^i}_j]$. Show that
> $$f(u_1, \ldots, u_k) = (\det A) f(v_1, \ldots, v_k).$$

Let's start substituting $u_i$ with $\sum_{j_i=1}^k {a^{j_i}}_k v_{j_i}$. By linearity
$$f(u_1, \ldots, u_k) = \sum_{j_1=1}^k \cdots \sum_{j_k = 1}^k {a^{j_1}}_1\cdots{a^{j_k}}_k f(v_{j_1}, \dots, v_{j_k})$$
Since multicovectors are alternating, we can assume that all $j_1, \dots, j_k$ are distinct and write the previous multisum as
$$\begin{eqnarray}
f(u_1, \ldots, u_k) =&& \sum_{\sigma \in S_k} {a^{\sigma(1)}}_1\cdots{a^{\sigma(k)}}_k f(v_{\sigma(1)}, \dots, v_{\sigma(k)})\\
=&& \left(\sum_{\sigma \in S_k} \text{sgn}(\sigma){a^{\sigma(1)}}_1\cdots{a^{\sigma(k)}}_k\right) f(v_1, \dots, v_k)
\end{eqnarray}$$
Which is a proper definition of the determinant of $A$.