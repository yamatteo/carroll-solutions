> Let $V$ be a vector space of dimension $n$ with basis $e_1, \ldots, e_n$. Let $\alpha^1, \ldots, \alpha^n$ be the dual basis for $V^\vee$. Show that a basis for the space $L_k(V)$ of $k$-linear functions on $V$ is ${\alpha^{i_1} \otimes \cdots \otimes \alpha^{i_k}}$ for all multi-indices $(i_1, \ldots, i_k)$ (not just the strictly ascending multi-indices as for $A_k(V)$). In particular, this shows that $\dim L_k(V) = n^k$. (This problem generalizes Problem 3.1.)

Let $f$ be any $k$-linear function on $V$ and let $v_1, \dots, v_k \in V$ be any vectors. Then we can break down each vector in its components and use $f$'s linearity:
$$\begin{eqnarray}
f(v_1, \dots, v_k) &=& \sum_{i_1=1}^n \alpha^{i_1}(v_1) f(e_{i_1}, v_2, \dots, v_k) \\
&=& \sum_{i_1=1}^n \dots \sum_{i_k=1}^n \alpha^{i_1}(v_1) \cdots \alpha^{i_k}(v_k) f(e_{i_1}, \dots, e_{i_k}) \\
&=& \sum_{i_1=1}^n \dots \sum_{i_k=1}^n  f(e_{i_1}, \dots, e_{i_k}) \left(\alpha^{i_1}\otimes \cdots \otimes \alpha^{i_k}\right)(v_1, \dots, v_k)
\end{eqnarray}$$
which shows that the $n^k$ products $\alpha^{i_1}\otimes \cdots \otimes \alpha^{i_k}$ span $L_k(V)$. On the other hand, if there's a null linear combination we can prove that every coefficient is zero testing it again the respective selection of elements in the $\{e_1, \dots, e_n\}$ basis. For example,
$$\begin{eqnarray}
0 &=& \left(\sum \lambda_{i_1, \dots, i_k}(\alpha^{i_1}\otimes \cdots \otimes \alpha^{i_k}) \right)(e_{j_1}, \dots, e_{j_k})\\
&=& \sum \lambda_{i_1, \dots, i_k}\left((\alpha^{i_1}\otimes \cdots \otimes \alpha^{i_k})(e_{j_1}, \dots, e_{j_k} )\right)\\
&=& \lambda_{j_1, \dots, j_k}
\end{eqnarray}$$
So each one of them is independent of the other and, together, they form a basis.