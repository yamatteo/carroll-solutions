> Show that the two-dimensional torus T2 is a manifold, by explicitly constructing an appropriate atlas: (Not a maximal one, obviously.)

The torus is built from the $[0, 1]^2$ square with boundaries adequately identified. One easy chart is from the subset $\left]0, 1\right[^2$ by the identity into itself. Think of this one as a chart around point $\left(\frac12, \frac12\right)$.

To make a chart around point $\left(0, \frac12\right)$ we map

$$\left(x, y\right) \mapsto \begin{array}{l}
\left(x+\frac12, y\right) & \text{ if } x < \frac12 \\
\left(x-\frac12, y\right) & \text{ if } x > \frac12 
\end{array}$$

from the domain $\left({\left[0, \frac12\right[} \cup {\left]\frac12, 1\right]}\right) \times {]0, 1[}$ onto $\left]0, 1\right[^2$. Points $(0, y)$ and $(1, y)$ are correctly mapped to the same points, incidentally $\left(\frac12, y\right)$; everything else is just a translation.

With the same reasoning, we can make charts around $\left(\frac12, 0\right)$ by switching the role of $x$ and $y$; and around point $\left(0, 0\right)$, mixing the previous two.