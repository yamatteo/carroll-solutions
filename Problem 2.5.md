> Give an example of two linearly independent, nowhere-vanishing vector fields in $\mathbb R^2$ whose commutator does not vanish. Notice that these fields provide a basis for the tangent space at each point, but it cannot be a coordinate basis since the commutator doesn’t vanish.

Take vectors 
$$
\begin{array}{rrl}
v = & \cos(x + y)\partial_x & + \sin(x+y)\partial_y \\
u = & -\sin(x+y)\partial_x & + \cos(x+y)\partial_y
\end{array}
$$

They are linearly independent because if $a \cdot \sin(x+y) + b \cdot \cos(x+y) = a \cdot \cos(x+y) - b\cdot \sin(x+y) = 0$, either $\cos(x+y) = 0$ and so $a = b = 0$ or $\cos(x+y) \neq 0$ and $a \cdot \tan(x+y) + b = a - b \cdot \tan(x+y) = 0$, therefore $b \cdot \tan^2(x+y) + b = 0$ and so, again, $a = b= 0$.

Their commutator is (let $C = \cos(x+y)$ and $S = \sin(x+y)$)
$$\begin{array}{rcl}
[v, u]^x \partial_x & = & [(C\partial_x + S\partial_y)(-S) - (-S\partial_x + C\partial_y)C]\partial_x \\
& = & C\partial_x(-S\partial_x) + S\partial_y(-S\partial_x) +S\partial_x(C\partial_x) - C\partial_y(C\partial_x) \\
& = & -C^2\partial_x - SC\partial_x\partial_x - SC\partial_x - S^2 \partial_x\partial_y -S^2 \partial_x + SC \partial_x \partial_x + SC \partial_x - C^2 \partial_x\partial_y \\
& = & -\partial_x - \partial_x\partial_y
\end{array}$$
$$\begin{array}{rcl}
[v, u]^y \partial_y & = & [(C\partial_x + S\partial_y)C - (-S\partial_x  + C\partial_y)S] \partial_y \\
& = & (C\partial_x + S\partial_y)(C\partial_y) - (-S\partial_x  + C\partial_y)(S \partial_y) \\
& = & C\partial_x(C\partial_y) + S\partial_y(C\partial_y) +S\partial_x(S \partial_y)  - C\partial_y(S \partial_y) \\
& = & -SC \partial_y + C^2 \partial_x\partial_y - S^2\partial_y + SC\partial_y\partial_y + SC \partial_y + S^2 \partial_x\partial_y - C^2 \partial_y -SC \partial_y\partial_y \\
& = & +\partial_x\partial_y - \partial_y
\end{array}$$
But these two parts are added together when applied to a function so, as an operator on function, $[v, u]$ correspond to the non vanishing constant vector field $[-1, -1]$