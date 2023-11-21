> Let $f: \mathbb R^2 \to \mathbb R$ be a $C^\infty$ function with $f(0, 0) = \partial f / \partial x (0, 0) = \partial f / \partial y (0, 0) = 0$. Define
> $$g(t, u) = \left\{ \begin{array}{ll} \frac{f(t, tu)}{t} & \text{ for } t \neq 0 \\ 0 & \text{ for } t = 0\end{array}\right.$$
> Prove that $g(t, u)$ is $C^\infty$ for $(t, u) \in \mathbb R^2$.

Let's start applying the result of [[Loring Tu - An Introduction to Manifolds/Problem 1.6|Problem 1.6]] with the given simplifications:
$$f(x, y) = x^2 g_{11}(x,y) + xy\,g_{12}(x,y) + y^2 g_{22}(x,y)$$
and then compose all these function with the $C^\infty$ substitution 
$$\left\{\,\begin{array}{l} x \mapsto t \\ y \mapsto ut\end{array}\right.$$
So that
$$f(t, ut) = t^2 g_{11}(t,ut) + ut^2g_{12}(t,ut) + u^2 t^2 g_{22}(t,ut)$$
Now we can redefine $g$ as
$$g(t, u) = t\cdot\left(g_{11}(t, ut) + u\, g_{12}(t, ut) + u^2 g_{22}(t, ut)\right)$$
which is $C^\infty$ because is a composition of $C^\infty$ functions and coincides with the previous definition for every value of $t$ and $u$.