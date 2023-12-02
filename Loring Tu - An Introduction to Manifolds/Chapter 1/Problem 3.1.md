> Let $e_1, \ldots, e_n$ be a basis for a vector space $V$ and let $\alpha^1, \ldots, \alpha^n$ be its dual basis in $V^\vee$. Suppose $[g_{ij}] \in \mathbb{R}^{n \times n}$ is an $n \times n$ matrix. Define a bilinear function $f: V \times V \to \mathbb{R}$ by
> $$f(v, w) = \sum_{1\leq i,j \leq n} g_{ij} v^i w^j$$
> for $v = \sum_i v^i e_i$ and $w = \sum_j w^j e_j$ in $V$. Describe $f$ in terms of the tensor products of $\alpha^i$ and $\alpha^j$, $1 \leq i, j \leq n$.

For every vector, $v = \sum_i v^i e_i = \sum_i \alpha^i(v) e_i$, so we can replace $v^i$ with $\alpha^i(v)$ and $w^j$ with $\alpha^j(w)$. Secondly, being that $\alpha^i$ and $\alpha^j$ are $1$-linear function, by definition of tensor product we can replace $\alpha^i(v)\alpha^j(w)$ with $(\alpha^i \otimes \alpha^j)(v, w)$. That's it
$$f(v, w) = \sum_{1 \leq i, j \leq n} g_{ij} (\alpha^i \otimes \alpha^j)(v, w)$$