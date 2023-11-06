>Imagine we have a tensor $X^{\mu\nu}$ and a vector $V^\mu$, with components $$X^{\mu\nu} = \begin{pmatrix}2 & 0 & 1 & -1 \\ -1 & 0 & 3 & 2 \\ -1 & 1 & 0 & 0 \\ -2 & 1 & 1 & -2\end{pmatrix} \qquad V^\mu = (-1, 2, 0, -2)$$
>Find the components of:
>- ${X^\mu}_\nu$
>- ${X_\mu}^\nu$
>- $X^{(\mu \nu)}$
>- $X_{[\mu\nu]}$
>- ${X^\lambda}_\lambda$
>- $V^\mu V_\mu$
>- $V_\mu X^{\mu\nu}$

To lower an index we use the metric $${X^\mu}_\nu = X^{\mu\alpha} g_{\alpha \nu} = \begin{pmatrix}-2 & 0 & 1 & -1 \\ 1 & 0 & 3 & 2 \\ 1 & 1 & 0 & 0 \\ 2 & 1 & 1 & -2\end{pmatrix}$$
$${X_\mu}^\nu = g_{\mu \alpha} X^{\alpha\nu} = \begin{pmatrix}-2 & 0 & -1 & 1 \\ -1 & 0 & 3 & 2 \\ -1 & 1 & 0 & 0 \\ -2 & 1 & 1 & -2\end{pmatrix}$$

To symmetrize the tensor we average with the transpose:
$$X^{(\mu \nu)} = \frac12 (X^{\mu\nu} + X^{\nu\mu}) = \begin{pmatrix}2 & - \frac{1}{2} & 0 & - \frac{3}{2}\\- \frac{1}{2} & 0 & 2 & \frac{3}{2}\\0 & 2 & 0 & \frac{1}{2}\\- \frac{3}{2} & \frac{3}{2} & \frac{1}{2} & -2\end{pmatrix}$$

The anysymmetric part is similar:
$$X_{[\mu \nu]} = \frac12 (X_{\mu\nu} - X_{\nu\mu}) = \begin{pmatrix}0 & - \frac{1}{2} & -1 & - \frac{1}{2}\\\frac{1}{2} & 0 & 1 & \frac{1}{2}\\1 & -1 & 0 & - \frac{1}{2}\\\frac{1}{2} & - \frac{1}{2} & \frac{1}{2} & 0\end{pmatrix}$$

The trace of ${X^\mu}_\nu$ is ${X^\lambda}_\lambda = -4$. The norm (squared) of $V_\mu$ is $V^\mu V_\mu = -1 + 4 +4 = 7$.

The _whatever_ product $V_\mu X^{\mu\nu} = g_{\mu\alpha}V^\alpha X^{\mu\nu} = \begin{pmatrix}4 & -2 & 5 & 7\end{pmatrix}$
```python
import micropip
await micropip.install('sympy')  
from sympy import *

X = Matrix([[2, 0, 1, -1], [-1, 0, 3, 2], [-1, 1, 0, 0], [-2, 1, 1, -2]])
V = Matrix([-1, 2, 0, -2])
g = Matrix([[-1, 0, 0, 0], [0, 1, 0, 0], [0, 0, 1, 0], [0, 0, 0, 1]])
print(latex((g*V).T*X))
```
$$\begin{pmatrix}-1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{pmatrix}\begin{pmatrix}2 & 0 & 1 & -1 \\ -1 & 0 & 3 & 2 \\ -1 & 1 & 0 & 0 \\ -2 & 1 & 1 & -2\end{pmatrix}$$