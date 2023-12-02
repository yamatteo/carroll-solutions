> Let $f(x)$ be the function on $\mathbb{R}$ defined in Example 1.3 (that is $f(x) = e^{-1/x}$ for $x>0$ and $0$ otherwise). 
> **(a)** Show by induction that for $x>0$ and $k\geq 0$, the $k$-th derivative $f^{(k)}(x)$ is of the form $p_{2k}(1/x) e^{-1/x}$ for some polynomial $p_{2k}(y)$ of degree $2k$ in $y$.
> **(b)** Prove that $f$ is $C^\infty$ on $\mathbb{R}$ and that $f^{(k)}(0) = 0$ for all $k\geq 0$.

The property (a) is true for $k=0$ with polynomial $p_0(y) = 1$. Suppose it is true for $k-1$, then $f^{(k-1)}(x) = p_{2k-2}(1/x) e^{-1/x}$ and so
$$\begin{eqnarray}
f^{(k)}(x) &&= \frac{\mathrm d}{\mathrm d x}\left(p_{2k-2}(1/x) e^{-1/x}\right) \\
&&= \frac{\mathrm d}{\mathrm d x}\left(p_{2k-2}(1/x)\right) e^{-1/x} + p_{2k-2}(1/x) \frac{\mathrm d}{\mathrm d x}\left(e^{-1/x}\right)\\
&&= p'_{2k-2}(1/x)(-1/x^2)e^{-1/x} + p_{2k-2}(1/x)e^{-1/x}(1/x^2) \\
&&= \left(-p'_{2k-2}(1/x)(1/x^2) + p_{2k-2}(1/x)(1/x^2)\right)e^{-1/x}
\end{eqnarray}$$
So the required polynomial is $p_{2k}(y) = y^2 \cdot (p_{2k-2}(y) - p'_{2k-2}(y))$ which have, in fact, degree $2k$. These $f^{(k)}$ are thus defined  for $x>0$, but each one respect the limit $f^{(k)}(x) \to 0$ when $x \to 0^+$, so we can rightfully extend them with $f^{(k)}(x) = 0$ for $x \leq 0$ and have continuous function for every $k \geq 0$. 