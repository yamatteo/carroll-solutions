> Let $\alpha$ be a nonzero $1$-covector and $\gamma$ a $k$-covector on a finite-dimensional vector space $V$. Show that $\alpha \wedge \gamma = 0$ if and only if $\gamma = \alpha \wedge \beta$ for some $(k-1)$-covector $\beta$ on $V$.

If $\gamma = (\alpha \wedge \beta)$ then directly $\alpha \wedge \gamma = \alpha \wedge (\alpha \wedge \beta) = (\alpha \wedge \alpha) \wedge \beta = 0 \wedge \beta = 0$.
So, suppose $\alpha \wedge \gamma = 0$. And let $v_0$ be fixed such that $\alpha(v_0) = 1$. Then
$$\begin{eqnarray}
0 &&= (\alpha\wedge\gamma)(v_0, \dots, v_k) \\
&&= \sum_{j=0}^k \left( \sum_{\sigma \in S_{0..k} \atop \sigma(0)=j} \frac{\text{sgn}(\sigma)}{k!} \alpha(v_{\sigma(0)})\gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)}) \right) \\

&&= \sum_{\sigma \in S_{k}} \frac{\text{sgn}(\sigma)}{k!} \gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)}) + \sum_{j=1}^k \left( \sum_{\sigma \in S_{0..k} \atop \sigma(0)=j} \frac{\text{sgn}(\sigma)}{k!} \alpha(v_{\sigma(0)})\gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)}) \right) \\

&&= \gamma(v_1, \dots, v_k) + \sum_{j=1}^k \left( \sum_{\sigma \in S_{0..k} \atop \sigma(j)=0} \frac{\text{sgn}(\sigma)}{k!} \alpha(v_{\sigma(0)})\gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)}) \right) \\

&&= \gamma(v_1, \dots, v_k) + \sum_{j=1}^k \left( \sum_{\sigma \in S_{0..k} \atop \sigma(1)=0} \frac{\text{sgn}(\sigma)}{k!} \alpha(v_{\sigma(0)})\gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)}) \right) \\

&&= \gamma(v_1, \dots, v_k) + \sum_{\sigma \in S_{0..k} \atop \sigma(1)=0} \frac{\text{sgn}(\sigma)}{(k-1)!} \alpha(v_{\sigma(0)})\gamma(v_{\sigma(1)}, \dots, v_{\sigma(k)})  \\
\end{eqnarray}$$
If we now define $\beta(w_2, \dots, w_k) = \gamma(v_0, w_2, \dots, w_k)$ and
$$\sigma^*(n) = \left\{\begin{array}{lr}\sigma(1) &\text{ if }n=0 \\ 0 & \text{ if } n = 1 \\ \sigma(n) & \text{ if }n > 1
\end{array}\right.$$ with the property that $\text{sgn}(\sigma) = -\text{sgn}(\sigma^*)$, we can conclude that
$$\begin{eqnarray}
0 &&= \gamma(v_1, \dots, v_k) + \sum_{\sigma \in S_k} \frac{\text{sgn}(\sigma^*)}{(k-1)!} \alpha(v_{\sigma^*(0)})\gamma(v_{\sigma^*(1)}, \dots, v_{\sigma^*(k)})  \\
&&= \gamma(v_1, \dots, v_k) - \sum_{\sigma \in S_k} \frac{\text{sgn}(\sigma)}{(k-1)!} \alpha(v_{\sigma(1)})\gamma(v_0, v_{\sigma(2)}, \dots, v_{\sigma(k)})  \\  
&&= \gamma(v_1, \dots, v_k) - (\alpha \wedge \beta)(v_1, \dots, v_k)  \\
\end{eqnarray}$$