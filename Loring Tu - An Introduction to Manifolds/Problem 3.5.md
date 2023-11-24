> Let $f$ be a $k$-tensor on a vector space $V$. Prove that $f$ is alternating if and only if $f(v_1, \ldots, v_k) = 0$ whenever two of the vectors $v_1, \ldots, v_k$ are equal.

If $f$ is alternating and $v_i = v_j$, then
$$f(\dots, v_i, \dots, v_j, \dots) = f(\dots, v_j, \dots, v_i, \dots) = -f(\dots, v_i, \dots, v_j, \dots)$$
so $f(\dots, v_i, \dots, v_j, \dots) = 0$.

On the other hand, suppose the characterization is true. Then
$$\begin{eqnarray}
0 &=& f(\dots, v_i + v_j, \dots, v_i + v_j, \dots) \\
&=& \cancel{f(\dots, v_i, \dots, v_i, \dots)} \\
&&+ f(\dots, v_i, \dots, v_j, \dots) \\
&&+ f(\dots, v_j, \dots, v_i, \dots) \\
&&+ \cancel{f(\dots, v_j, \dots, v_j, \dots)} \\
\end{eqnarray}$$
So any transposition flip the sign and (decomposing any permutation into transpositions) $f$ is alternating.