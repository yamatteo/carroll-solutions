> (a) Let $V$ be a vector space of dimension $n$ and $f: V \to \mathbb{R}$ a nonzero linear functional. Show that $\dim \ker f = n - 1$. A linear subspace of $V$ of dimension $n-1$ is called a hyperplane in $V$.
> 
> (b) Show that a nonzero linear functional on a vector space $V$ is determined up to a multiplicative constant by its kernel, a hyperplane in $V$. In other words, if $f$ and $g: V \to \mathbb{R}$ are nonzero linear functionals and $\ker f = \ker g$, then $g = cf$ for some constant $c \in \mathbb{R}$.

Since $f$ is nonzero its image as positive dimension. But it can't be greater than $1$, so it is $1$. Since $\dim V = \dim \text{img } f + \dim \ker f$ , the kernel has dimension $n-1$.

Let $v \in V$ be a vector that's not in the kernel shared by $f$ and $g$, so that $f(v) \neq 0$. Then $V$ can be decomposed in the kernel and the span of $v$; that is, for any vector $w \in V$ we can write $w = k \cdot v + u$ with $k \in \mathbb R$ and $u$ in the kernel. So
$$g(w) = k\cdot g(v) + g(u) = k \frac{g(v)}{f(v)}f(v) = \frac{g(v)}{f(v)} f(w)$$ 