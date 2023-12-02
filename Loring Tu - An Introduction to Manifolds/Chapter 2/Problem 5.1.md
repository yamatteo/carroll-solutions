> Let $A$ and $B$ be two points not on the real line $\mathbb{R}$. Consider the set $S = (\mathbb{R} - {0}) \cup {A, B}$ (see Figure 5.9).
> ![](<Excalidraw/Drawing 2023-11-26 11.16.35.excalidraw>)
> For any two positive real numbers $c, d$, define $$I_A(-c, d) = {]{-c}, 0[} \cup {A} \cup {]0, d[}$$ and similarly for $I_B(-c, d)$, with $B$ instead of $A$. Define a topology on $S$ as follows: on $(\mathbb{R} - \{0\})$, use the subspace topology inherited from $\mathbb{R}$, with open intervals as a basis. A basis of neighborhoods at $A$ is the set $\{I_A(-c, d) | c, d > 0\}$; similarly, a basis of neighborhoods at $B$ is $\{I_B(-c, d) | c, d > 0\}$.
> 
> (a) Prove that the map $h: I_A(-c, d) \to ]-c, d[$ defined by $$\begin{eqnarray}
 h(x) = x && \text{ for } x \in {]{-c}, 0[} \cup {]0, d[} \\
 h(A) = 0 \\
 \end{eqnarray}$$ is a homeomorphism.
> 
> (b) Show that $S$ is locally Euclidean and second countable, but not Hausdorff.

Having a basis, it is enough to show that $h$ and $h^{-1}$ send open interval into open interval. For strictly positive or strictly negative integers, $h=h^{-1}$ is the identity. For intervals around zero, $I_A(-c, d) \;{\xrightarrow{\;h\;}}\; {]{-c}, d[} \;{\xrightarrow{\;h^{-1}\;}}\; I_A(-c, d)$.

Since $(I_A(-c, d), h)$ is a chart around $A$, S is locally euclidean at $A$. With a similar map we can show that it's locally euclidean at $B$. For any other point, the identity is a chart.

It is second countable, because intervals $(-c, -d)$, $I_A(-c, d)$, $I_B(-c, d)$ and $(d, c)$ (for every rational $0 < d < c$) are a countable basis.

It is not Hausdorff. Take points $A$ and $B$. Any neighborhood of $A$ includes some $I_A(-c, c)$ and any neighborhood of $B$ includes some $I_B(-d, d)$. These are not disjoint, for there is some real number $x < c$ and $x < d$.