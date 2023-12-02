> Let $A = \oplus_{k=-\infty}^\infty A^k$ be a graded algebra over a field $K$ with $A^k = 0$ for $k < 0$. Let $m$ be an integer. A superderivation of $A$ of degree $m$ is a $K$-linear map $D: A \to A$ such that for all $k$, $D(A^k) \subseteq A^{k+m}$ and for all $a \in A^k$ and $b \in A^l$ $$D(ab) = (Da)b + (-1)^{km}a(Db)$$If $D_1$ and $D_2$ are two superderivations of $A$ of respective degrees $m_1$ and $m_2$, define their commutator to be $$[D_1, D_2] = D_1 \circ D_2 - (-1)^{m_1m_2}D_2 \circ D_1$$Show that $[D_1, D_2]$ is a superderivation of degree $m_1 + m_2$. (A superderivation is said to be even or odd depending on the parity of its degree. An even superderivation is a derivation; an odd superderivation is an antiderivation.)

Let $a \in A^k$ and  $b \in A^l$, let's use $D, H$ instead of $D_1, D_2$ and use $m, n$ instead of $m_1, m_2$. 
$$\begin{eqnarray}
[D, H](ab) &=& D H (ab) - (-1)^{m n} H D (ab)\\
&=&D\left[(Ha)b + (-1)^{kn}a(Hb)\right] - (-1)^{m n} H\left[ (Da)b + (-1)^{km}a(Db) \right]\\

&=& D((Ha)b) + (-1)^{kn}D(a(Hb)) + \\
&&- (-1)^{mn} H((Da)b) - (-1)^{mn+km} H(a(Db)) \\

&=& (DHa)b + (-1)^{(k+n)m}(Ha)(Db) \\
&&+ (-1)^{kn}(Da)(Hb) + (-1)^{km+kn}a(DHb) \\
&&- (-1)^{mn}(HDa)b - (-1)^{mn + (k+m)n}(Da)(Hb) \\
&&-(-1)^{mn + km}(Ha)(Db) - (-1)^{mn + km + kn}a(HDb)\\

&=& (DHa)b - (-1)^{mn}(HDa)b  \\
&&+ (-1)^{km+kn}a(DHb) - (-1)^{mn + km + kn}a(HDb)\\
&=& ([D, H]a)b + (-1)^{k(m+n)}a([D,H]b)
\end{eqnarray}$$
and $[D, H]$ is a superderivation. A tricky point was, for me, the fact that $(Ha)$ is no longer in $A^k$ but in $A^{k+n}$, so the (anti)Liebniz rule change the exponent of $(-1)$.
