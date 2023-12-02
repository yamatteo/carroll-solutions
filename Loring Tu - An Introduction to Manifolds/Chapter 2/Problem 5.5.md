> Prove that if $\{(U_\alpha, \phi_\alpha)\}$ and $\{(V_i, \psi_i)\}$ are $C^\infty$ atlases for the manifolds $M$ and $N$ of dimensions $m$ and $n$, respectively, then the collection $$\left\{(U_\alpha \times V_i, \phi_\alpha \times \psi_i: U_\alpha \times V_i \to \mathbb{R}^m \times \mathbb{R}^n)\right\}$$of charts is a $C^\infty$ atlas on $M \times N$. Therefore, $M \times N$ is a $C^\infty$ manifold of dimension $m+n$.

Fundamental lemmas of topology and basic definitions of set theory assure us that
-  for every element $(p, q) \in M \times N$, there are $U_\alpha$ and $V_i$ such that $(p, q) \in U_\alpha \times V_i$;
-  $U_\alpha \times V_i$ is open since $U_\alpha$ and $V_i$ are open;
-  $\phi_\alpha \times \psi_i: U_\alpha \times V_i \to \mathbb{R}^m \times \mathbb{R}^n$ is a homeomorphism to some open subset of $\mathbb R^{n+m}$;
-  different $\phi_\alpha \times \psi_i$ are compatible.
So the set $\left\{(U_\alpha \times V_i, \phi_\alpha \times \psi_i: U_\alpha \times V_i \to \mathbb{R}^m \times \mathbb{R}^n)\right\}$ is an atlas and can be extended to a maximal atlas, making $M \times N$ a smooth manifold.