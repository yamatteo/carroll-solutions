> Verify (2.78): for the exterior derivative of a product of a $p$-form $\omega$ and a $q$-form $\eta$, we have $$\mathrm d(\omega \wedge \eta) = (\mathrm d \omega) \wedge \eta + (-1)^p\omega \wedge (\mathrm d\eta)$$

Being that $\mathrm d(\omega \wedge \eta)$ is a $(p+q+1)$-form and thus linear, as well as the right side of the equation, we just need to prove the equation for its components in some basis $\{\partial_\mu\}$ derived from the coordinates $\{x^\mu\}$. By the definition of exterior derivative as given by Carroll:
$$\mathrm d (\omega \wedge \eta)_{\mu_0 \dots \mu_{p+q}} = (p+q+1) \cdot \partial_{[\mu_0} (\omega \wedge \eta)_{{\mu_1} \dots {\mu_{p+q}]}}$$
We can split the permutations of the indices in groups, depending on what index goes in the partial derivatives
$$ = (p+q+1) \cdot \sum_{i=0}^{p+q} (-1)^p \partial_{\mu_i} (\omega\wedge\eta)_{[\mu_0 \dots \mu_{i-1} \mu_{i+1} \dots \mu_{p+q}]} $$
but $(\omega\wedge\eta)$ is completely anti-symmetric so we can squash all permutations into a single one, provided we don't change the order. The indices $\mu_0 \dots \mu_{i-1} \mu_{i+1} \dots \mu_{p+q}$ means every index from $\mu_0$ to $\mu_{p+q}$ except $\mu_i$, so $p+q$ in total. By definition of wedge product (as given by Carroll), we can replace $(\omega\wedge\eta)$ with
$$ = (p+q+1) \cdot \sum_{i=0}^{p+q} (-1)^p \partial_{\mu_i} \left(\frac{(p+q)!}{p!q!}\omega_{[\nu_{i,1} \dots \nu_{i,p}}\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}]}\right) $$
where
$$ \nu_{i, j} = \left\{\begin{array}{l}
\mu_{j-1} & \text{ if }j \leq i \\
\mu_j & \text{ if }j > i
\end{array}\right.$$
Then we can factor out the constants and apply Liebniz rule to the partial derivatives. For a single case in all the permutations of indices $\nu$ it does
$$\begin{array}{rcl}
\partial_{\mu_i}(\omega_{\nu_{i,1} \dots \nu_{i,p}}\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}}) &=& (\partial_{\mu_i}\omega_{\nu_{i,1} \dots \nu_{i,p}})\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}} + \omega_{\nu_{i,1} \dots \nu_{i,p}}(\partial_{\mu_i}\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}}) \\
&=& (\partial_{\mu_i}\omega_{\nu_{i,1} \dots \nu_{i,p}})\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}} + (\partial_{\mu_i}\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}})\omega_{\nu_{i,1} \dots \nu_{i,p}}
\end{array}$$
But the same goes for all permutation, so we can put the brackets back as 
$$ = \frac{(p+q+1)!}{p!q!} \cdot \sum_{i=0}^{p+q} (-1)^p \left((\partial_{\mu_i}\omega_{[\nu_{i,1} \dots \nu_{i,p}})\eta_{\nu_{i,p+1} \dots \nu_{i,p+q}]} + (\partial_{\mu_i}\eta_{[\nu_{i,p+1} \dots \nu_{i,p+q}})\omega_{\nu_{i,1} \dots \nu_{i,p}]}\right)  $$
Where both side of the sum can be seen as break down of a more general antisymmetrization as
$$ = \frac{(p+q+1)!}{p!q!} \cdot \left( (\partial_{[\mu_0}\omega_{\nu_{0,1} \dots \nu_{0,p}})\eta_{\nu_{0,p+1} \dots \nu_{0,p+q}]} + (\partial_{[\mu_0}\eta_{\nu_{0,p+1} \dots \nu_{0,p+q}})\omega_{\nu_{0,1} \dots \nu_{0,p}]}\right) $$
$$ = \frac{(p+q+1)!}{p!q!} \cdot \left( (\partial_{[\mu_0}\omega_{\mu_1 \dots \mu_p})\eta_{\mu_{p+1} \dots \mu_{p+q}]} + \omega_{[\mu_1 \dots \mu_p}(\partial_{\mu_0}\eta_{\mu_{p+1} \dots \mu_{p+q}]})\right) $$
but than we can use the definition of exterior derivative to write
$$ = \frac{(p+q+1)!}{p!q!} \cdot \left(\frac{1}{p+1} (\mathrm d \omega)_{[\mu_0 \dots \mu_p}\eta_{\mu_{p+1} \dots \mu_{p+q}]} + \frac{1}{q+1}\omega_{[\mu_1 \dots \mu_p}(\mathrm d \eta)_{\mu_0 \mu_{p+1} \dots \mu_{p+q}]})\right) $$
then we can split the two pieces and bring $\mu_0$ as first index in the second piece
$$ = \frac{(p+q+1)!}{(p+1)!q!} (\mathrm d \omega)_{[\mu_0 \dots \mu_p}\eta_{\mu_{p+1} \dots \mu_{p+q}]} + (-1)^p \frac{(p+q+1)!}{p!(q+1)!}\omega_{[\mu_0 \dots \mu_{p-1}}(\mathrm d \eta)_{\mu_p \dots \mu_{p+q}]} $$
and finally use the definition of wedge product to obtain the final result.