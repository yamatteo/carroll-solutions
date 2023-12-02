> Let $\textbf{0} = (0,0)$ be the origin and $B(\mathbf{0},1)$ the open unit disk in $\mathbb{R}^2$. To find a diffeomorphism between $B(\mathbf{0},1)$ and $\mathbb{R}^2$, we identify $\mathbb{R}^2$ with the xy-plane in $\mathbb{R}^3$ and introduce the lower open hemisphere
> $$S: x^2 + y^2 + (z-1)^2 = 1, \quad z < 1,$$
> in $\mathbb{R}^3$ as an intermediate space (Figure 1.4). First note that the map
>$$f: B(\mathbf{0},1) \rightarrow S, \quad (a,b) \mapsto (a,b,1-\sqrt{1-a^2-b^2}),$$
> is a bijection.
> 
> (a) The stereographic projection $g: S \rightarrow \mathbb{R}^2$ from $(0,0,1)$ is the map that sends a point $(a,b,c) \in S$ to the intersection of the line through $(0,0,1)$ and $(a,b,c)$ with the xy-plane. Show that it is given by
> $$(a,b,c) \mapsto (u,v) = \left(\frac{a}{1-c}, \frac{b}{1-c}\right), \quad c = 1 - \sqrt{1-a^2-b^2},$$
> with inverse
> $$(u,v) \mapsto \left(\frac{u}{\sqrt{1+u^2+v^2}}, \frac{v}{\sqrt{1+u^2+v^2}}, 1-\frac{1}{\sqrt{1+u^2+v^2}}\right).$$
> (b) Composing the two maps $f$ and $g$ gives the map
> 
> $$h = g\circ f: B(\mathbf{0},1) \rightarrow \mathbb{R}^2, \quad h(a,b) = \left(\frac{a}{\sqrt{1-a^2-b^2}}, \frac{b}{\sqrt{1-a^2-b^2}}\right).$$
> 
> Find a formula for $h^{-1}(u,v) = (f^{-1} \circ g^{-1})(u,v)$ and conclude that $h$ is a diffeomorphism of the open disk $B(\mathbf{0},1)$ with $\mathbb{R}^2$.
> 
> (c) Generalize part (b) to $\mathbb{R}^n$.
![[Drawing 2023-11-16 14.22.16.excalidraw]]

Looking from the side, we see two similar right triangles. The smaller has sides $c$ and $\sqrt{u^2 + v^2} - \sqrt{a^2 + b^2}$; the larger has respective sides $1$ and $\sqrt{u^2 + v^2}$. So we can deduce that

$$\begin{eqnarray}
& \frac{c}{1} = \frac{\sqrt{u^2 + v^2} - \sqrt{a^2 + b^2}}{\sqrt{u^2 + v^2}} \\
\\
\Rightarrow & 1-c = \frac{\sqrt{a^2+b^2}}{\sqrt{u^2 + v^2}} \\
\\
\Rightarrow & u^2 + v^2 = \frac{a^2 + b^2}{(1-c)^2} = \left(\frac{a}{1-c}\right)^2 + \left(\frac{b}{1-c}\right)^2
\end{eqnarray}$$
Looking from above we see that $a/b = u/v$ or, more generally, $a \cdot v = b \cdot u$. So with little more effort we prove that $u = \frac{a}{1-c}$ and $v = \frac{b}{1-c}$. To invert the relation, start by considering that
$$1 + u^2 + v^2 = \frac{(1-c)^2 + a^2 + b^2}{(1-c)^2} = \frac{1}{(1-c)^2}$$
so 
$$a = u \cdot (1-c) = \frac{u}{\sqrt{1 + u^2 + v^2}}$$
The inverse of $h$ is 
$$h^{-1}(u, v) = \left( \frac{u}{\sqrt{1+u^2+v^2}}, \frac{v}{\sqrt{1+u^2+v^2}}\right)$$
that is $C^\infty$ for any point in $\mathbb R^2$.

---
To generalize to $\mathbb R^n$, let's consider the ball $B(\mathbf 0, 1)$ including all points with coordinates $(x^1, \dots, x^n)$ such that
$$\left(x^1\right)^2 + \cdots + \left(x^n\right)^2 = k^2 < 1$$
Then we can map
$$(x^1, \dots, x^n) \mapsto \left(\frac{x^1}{\sqrt{1 - k^2}}, \dots, \frac{x^n}{\sqrt{1 - k^2}}\right)$$
As before, with little effort we can show that this map is a diffeomophism.