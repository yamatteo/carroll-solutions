> Let $U \subset \mathbb{R}^n$ and $V \subset \mathbb{R}^n$ be open subsets. A $C^\infty$ map $F: U \rightarrow V$ is called a diffeomorphism if it is bijective and has a $C^\infty$ inverse $F^{-1}: V \rightarrow U$.
>
> (a) Show that the function $f: \left]-\frac{\pi}{2},\frac{\pi}{2}\right[ \rightarrow \mathbb{R}$, $f(x) = \tan x$, is a diffeomorphism.
>
> (b) Let $a, b$ be real numbers with $a < b$. Find a linear function $h: \left]a, b\right[ \rightarrow \left]-1, 1\right[$, thus proving that any two finite open intervals are diffeomorphic. The composite $f\circ h: \left]a, b\right[ \rightarrow \mathbb{R}$ is then a diffeomorphism of an open interval with $\mathbb{R}$.
> 
> (c) The exponential function $\exp: \mathbb{R} \rightarrow \left]0, \infty\right[$ is a diffeomorphism. Use it to show that for any real numbers $a$ and $b$, the intervals $\mathbb{R}$, $\left]a, \infty\right[$, and $\left]-\infty, b\right[$ are diffeomorphic.

Function $\tan(x)$ is $C^\infty$ because it is analytic and can be expressed as power series. Its inverse is $\arctan(x)$ whose first derivative is $\frac{1}{1+x^2}$ which is a rational function, and following derivatives have form $\frac{P(x)}{(1+x^2)^n}$ for some polynomial $P$ ans some integer $n$. So $\arctan(x)$ is also $C^\infty$.

Let $h(x) = -\frac{\pi}{2} + \pi\cdot\frac{x-a}{b-a}$. It is a linear function (so a diffeomorphism) from $]a, b[$ to $\left]-\frac{\pi}{2},\frac{\pi}{2}\right[$ and $f \circ h$ is a diffeomorphism from $]a, b[$ to $\mathbb R$.

We can say that both $]a, \infty[$ and $]-\infty, b[$ are diffeomorphic to $\mathbb R$. But we could use directly $x \mapsto b + a - x$
![](<Excalidraw/Drawing 2023-11-16 12.33.22.excalidraw>)