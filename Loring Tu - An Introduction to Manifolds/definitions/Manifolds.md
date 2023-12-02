### Topological manifolds
A topological space $M$ is **locally Euclidean** of dimension $n$ if every point $p$ in $M$ has a neighborhood $U$ such that there is a homeomorphism
$$\phi: U \to \text{an open subset of } \mathbb{R}^n.$$
We call the pair $(U,\phi: U \to \mathbb{R}^n)$ a **chart**, $U$ a coordinate neighborhood or a coordinate open set, and $\phi$ a coordinate map or a coordinate system on $U$. We say that a chart $(U,\phi)$ is centered at $p \in U$ if $\phi(p) = 0$.

A **topological manifold** is a Hausdorff, second countable, locally Euclidean space. It is said to be of dimension $n$ if it is locally Euclidean of dimension $n$.

### Manifolds
Two charts $(U,\phi: U \to \mathbb{R}^n)$, $(V,\psi: V \to \mathbb{R}^n)$ of a topological manifold are **$C^\infty$-compatible** if the two maps
$$\phi \circ \psi^{-1}: \psi(U \cap V) \to \phi(U \cap V),$$
$$\psi \circ \phi^{-1}: \phi(U \cap V) \to \psi(U \cap V)$$
are $C^\infty$. These two maps are called the transition functions between the charts. If $U \cap V$ is empty, then the two charts are automatically $C^\infty$-compatible.

A $C^\infty$ atlas or simply an **atlas** on a locally Euclidean space $M$ is a collection $\mathfrak U = \{(U_\alpha, \phi_\alpha)\}$ of pairwise $C^\infty$-compatible charts that cover $M$, i.e., such that $M = \bigcup_\alpha U_\alpha$.

> **Lemma.** Let $\{(U_\alpha, \phi_\alpha)\}$ be an atlas on a locally euclidean space. If two charts $(V, \psi)$ and $(W, \sigma)$ are both compatible with the atlas $\{(U_\alpha, \phi_\alpha)\}$, then they are compatible with each other.

A **smooth manifold** is a topological manifold together with a maximal atlas. the maximal atlas is also called a differentiable structure. A manifold is said to have dimension $n$ if all of its connected components have dimension $n$. A 1-dimensional manifold is also called a curve, a 2-dimensional manifold a surface, and an $n$-dimensional manifold an $n$-manifold.