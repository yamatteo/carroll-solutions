> Define carefully addition, multiplication, and scalar multiplication in $C_p^\infty$ (see [[Smooth germs]]). Prove that addition in $C_p^\infty$ is commutative.

Let $[f]_p$ and $[g]_p$ be germs in $C_p^\infty$; then there are $f  \in C^\infty(U)$ and $g \in C^\infty(V)$ with $p \in U \cap V \subseteq \mathbb R^n$. With $W = U \cap V$, let's define
$$[f]_p + [g]_p = [f_{|W}+g_{|W}]_p$$
$$[f]_p \cdot [g]_p = [f_{|W} \cdot g_{|W}]_p$$
$$k \cdot [f]_p = [k \cdot f]_p$$
Many proofs are due to make these definitions sound: for any $f, U$ and $f', U'$ in the same equivalence class, we need to show that, for example, $f + g \sim f' + g$. Then, the commutativity of addition comes from the commutativity of addition of regular functions $f_{|W}+g_{|W} = g_{|W}+f_{|W}$.