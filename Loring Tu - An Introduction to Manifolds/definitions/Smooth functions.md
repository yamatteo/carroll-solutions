## Real-valued functions
Let $M$ be a smooth manifold of dimension $n$. A function $f: M \to \mathbb{R}$ is said to be $C^\infty$ or smooth at a point $p$ in $M$ if there is a chart $(U,\phi)$ about $p$ in $M$ such that $f \circ \phi^{-1}$, a function defined on the open subset $\phi(U)$ of $\mathbb{R}^n$, is $C^\infty$ at $\phi(p)$ (see Figure 6.1). The function $f$ is said to be $C^\infty$ on $M$ if it is $C^\infty$ at every point of $M$.

## Inter-manifold functions
Let $N$ and $M$ be manifolds of dimension $n$ and $m$ respectively. A continuous map $F: N \to M$ is $C^\infty$ at a point $p$ in $N$ if there are charts $(V,\psi)$ about $F(p)$ in $M$ and $(U,\phi)$ about $p$ in $N$ such that the composition $\psi \circ F \circ \phi^{-1}$, a map from the open subset $\phi(F^{-1}(V) \cap U)$ of $\mathbb{R}^n$ to $\mathbb{R}^m$, is $C^\infty$ at $\phi(p)$ (see Figure 6.3). The continuous map $F: N \to M$ is said to be $C^\infty$ if it is $C^\infty$ at every point of $N.$

> **Proposition 6.8.** Let $N$ and $M$ be smooth manifolds, and $F: N \to M$ a continuous map. The following are equivalent:
> (i) The map $F: N \to M$ is smooth.
> (ii) For every chart $(U, \phi)$ on $N$ and $(V, \psi)$ on $M$, the map $\psi \circ F \circ \phi^{-1}$ is smooth.
## Diffeomorphism
A diffeomorphism is a smooth function with a smooth inverse.

> **Propositions 6.10 and 6.11.** Let $U$ be an open subset of a manifold $M$ of dimension $n$. A map $\phi: U \to \phi(U) \subset \mathbb{R}^n$ is a diffeomorphism onto an open subset of $\mathbb{R}^n$ if and only if $(U, \phi)$ is a chart on $M$.

