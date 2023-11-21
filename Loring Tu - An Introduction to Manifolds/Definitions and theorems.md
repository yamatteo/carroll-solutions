## Definiton 1.1 - Smooth functions
Let $k$ be a nonnegative integer. A real-valued function $f: U \rightarrow \mathbb{R}$ is said to be $C^k$ at $p \in U$ if its partial derivatives
$$\frac{\partial^{j}f}{\partial x_{i_1} \cdots \partial x_{i_j}}(p)$$
of all orders $j \leq k$ exist and are continuous at $p$. The function $f: U \rightarrow \mathbb{R}$ is $C^{\infty}$ at $p$ if it is $C^k$ for all $k \geq 0$; in other words, its partial derivatives $\frac{\partial^{j}f}{\partial x_{i_1} \cdots \partial x_{i_j}}(p)$ of all orders exist and are continuous at $p$. A vector-valued function $f: U \rightarrow \mathbb{R}^m$ is said to be $C^k$ at $p$ if all of its component functions $f_1, \ldots, f_m$ are $C^k$ at $p$. We say that $f: U \rightarrow \mathbb{R}^m$ is $C^k$ on $U$ if it is $C^k$ at every point in $U$. A similar definition holds for a $C^{\infty}$ function on an open set $U$. We treat the terms “$C^{\infty}$” and “smooth” as synonymous.
## Lemma 1.4 - Taylor's theorem with remainders
Let $f$ be a $C^{\infty}$ function on an open subset $U$ of $\mathbb{R}^n$ star-shaped with respect to a point $\mathbf{p} = (p_1, \ldots, p_n)$ in $U$. Then there exist functions $g_1(x), \ldots, g_n(x) \in C^{\infty}(U)$ such that
$$f(x) = f(\mathbf{p}) + \sum_{i=1}^n (x_i - p_i) g_i(x), \quad g_i(\mathbf{p}) = \frac{\partial f}{\partial x_i}(\mathbf{p})$$