Let $K$ be a field. An _algebra over $K$_ is a vector space $A$ over $K$ equipped with a bilinear multiplication operation 
$$A \times A \rightarrow A, \quad (a,b) \mapsto ab$$
such that for all $a,b,c \in A$ and $r \in K$:
$$\begin{align*}
(ab)c &= a(bc) && \text{(associativity)} \\
(a+b)c &= ac + bc && \text{(left distributivity)} \\  
a(b+c) &= ab + ac && \text{(right distributivity)} \\
r(ab) &= (ra)b = a(rb) && \text{(homogeneity)}
\end{align*}$$

In other words, an algebra over $K$ is a ring $A$ that is also a $K$-vector space, such that ring multiplication is bilinear. Equivalently, the scalar multiplication is compatible with the ring multiplication.

Some examples of algebras over fields include polynomial rings $K[x_1,\dotsc, x_n]$, and spaces of functions like $C^\infty(U)$ for $U \subseteq \mathbb{R}^n$ open.