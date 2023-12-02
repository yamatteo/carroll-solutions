> Let $f : X \to Y$ be a map of sets, and let $B \subseteq Y$. Prove that $f(f^{-1}(B)) = B \cap f(X)$. Therefore, if $f$ is surjective, then $f(f^{-1}(B)) = B$.

Suppose $y \in f(f^{-1}(B))$, so there is $x \in f^{-1}(B)$ such that $f(x) = y$, therefore $y \in f(X)$; but since $x \in f^{-1}(B)$, there is $y' \in B$ such that $f(x) = y'$. We conclude that $y = f(x) = y' \in B$.
On the other hand, suppose $y \in B \cap f(X)$. Then there is $x \in X$ such that $f(x) = y$. Being $y \in B$, we now that $x \in f^{-1}(B)$ and $y \in f(f^{-1}(B))$.