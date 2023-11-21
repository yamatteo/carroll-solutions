> By clever choice of coordinate charts, can we make $\mathbb R^2$ look like a
> one-dimensional manifold? Can we make $\mathbb R$ look like a two-dimensional
> manifold? If so, explicitly construct an appropriate atlas, and if not,
> explain why not. The point of this problem is to provoke you to think deeply
> about what a manifold is; it can’t be answered rigorously without going into
> more details about topological spaces. In particular, you might have to
> forget that you already know a definition of “open set” in the original
> $\mathbb R^2$ or $\mathbb R$, and define them as being appropriately
> inherited from the $\mathbb R$ or $\mathbb R^2$ to which they are being
> mapped.

If the definition of $n$-manifold involves a plain set $M$ and an atlas to $\mathbb R^n$ so that the topology on $M$ is defined by the inverse images of the open sets in $\mathbb R^n$, then every set with the same cardinality of $\mathbb R$ can be used to form an $n$-manifold, whatever the $n > 0$.

On the other hand, if we want that the manifold starts with its own topology $(M, \tau)$ so that the charts can be required to be _continuous_ maps from $M$ to $\mathbb R^n$, then we have to specify what is the topology before asking the question.

If we think of $\mathbb R^2$ with its standard topology, then it can't be forced to be a one-dimensional manifold. Suppose there is such atlas, and a chart $\varphi: U \to I$ with $U$ open in $\mathbb R^2$ and $I$ open in $\mathbb R$. Then there is an interval $J \subsetneq (\text{the closure of }J) \subsetneq I$ and $V \subset U$ with $\varphi[V] = J$. Since $J$ is an interval in $\mathbb R$, its closure has just two points more than $J$. But since $\varphi$ is continuous and one-to-one, also the closure of $V$, which is mapped to the closure of $J$, has just two more points. And that's not possible.

In the other direction, suppose there is a chart $\varphi: I \to U$. Then we have open interval $J \subset I$ and open set $V \subset U$ with $\varphi[J] = V$. And there is a value $p$ inside $J$ that split the interval in two open interval. So by the image with $\varphi$ we have $V$ made of two disjoint open set, plus a single point in the closure of both; again, not possible.