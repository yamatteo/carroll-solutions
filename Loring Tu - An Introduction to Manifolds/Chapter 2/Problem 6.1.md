> Let $\mathbb R$ be the real line with the differentiable structure given by the maximal atlas of the chart $(\mathbb R,\phi = \mathbb 1 : \mathbb R \to \mathbb R)$, and let $\mathbb R'$ be the real line with the differentiable structure given by the maximal atlas of the chart $(\mathbb R,\psi : \mathbb R \to \mathbb R)$, where $\psi(x) = x^{1/3}$.
> 
> (a) Show that these two differentiable structures are distinct.
> 
> (b) Show that there is a diffeomorphism between $\mathbb R$ and $\mathbb R'$. (Hint: The identity map $\mathbb R \to \mathbb R$ is not the desired diffeomorphism; in fact, this map is not smooth.)

We should prove that two charts in the atlases are not compatible. Let's take the given $\phi(x) = x$ and $\psi(x) = x^{1/3}$. Indeed, $\phi \circ \psi^{-1}$ is smooth, but $\psi \circ \phi^{-1} = \psi$ is not: its first derivative is undefined and divergent at $x = 0$. 
![](<Drawing 2023-11-29 15.03.45.excalidraw>)
If we take the function $F: (\mathbb R, \phi) \to (\mathbb R, \psi)$ defined by $F(x) = x^3$, we can see that $\psi \circ F \circ \phi^{-1}$ is the identity (so it's smooth) and that its inverse is smooth as well: $\phi \circ F^{-1} \circ \psi^{-1}$ is also the identity.