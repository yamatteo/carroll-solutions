> Three events, A, B, C, are seen by observer $\mathcal O$ to occur in the order ABC. Another observer, $\bar {\mathcal O}$, sees the events in the order CBA. Is it possible that a third observer sees the events in the order ACB? Support your conclusion by drawing a spacetime diagram.

Let the events A, B and C have in $\mathcal O$ coordinates $$\begin{pmatrix}-1 \\ -4 \\ +4 \\ 0\end{pmatrix}\quad\begin{pmatrix}0 \\ 0 \\ -4 \\ 0\end{pmatrix}\quad\begin{pmatrix}+1 \\ +4 \\ 0 \\ 0\end{pmatrix}$$

```python
import micropip
await micropip.install('sympy')  
from sympy import *

A = Matrix([-1, -4, 4, 0])
B = Matrix([0, 0, -4, 0])
C = Matrix([1, 4, 0, 0])
```

Suppose the observer $\bar{\mathcal O}$ has velocity $1/2$ along the $x$ direction _wrt_ $\mathcal O$. Then the transformation matrix from $\mathcal O$'s coordinates to $\bar{\mathcal O}$'s coordinates is $${\Lambda ^{\bar{\mu}}} _{\mu} = \begin{pmatrix}
2/\sqrt 3 && -1/\sqrt 3 && 0 && 0 \\
-1/\sqrt 3 && 2 / \sqrt3 && 0 && 0 \\
0 && 0 && 1 && 0 \\
0 && 0 && 0 && 1
\end{pmatrix}$$
In $\bar{\mathcal O}$, the events A, B and C have coordinates $$\begin{pmatrix} 2/\sqrt3 \\ -7/\sqrt3 \\ +4 \\ 0 \end{pmatrix} \quad \begin{pmatrix} 0 \\ 0 \\ -4 \\ 0\end{pmatrix}\quad\begin{pmatrix}-2/\sqrt3 \\ 7/\sqrt3 \\ 0 \\ 0\end{pmatrix}$$
showing that the perceived order is CBA.

```python
L = Matrix([
	[2 / sqrt(3), - 1/ sqrt(3), 0, 0],
	[-1/ sqrt(3), 2/ sqrt(3), 0, 0],
	[0, 0, 1, 0],
	[0, 0, 0, 1]
])
print("A ->", L*A)
print("B ->", L*B)
print("C ->", L*C)
```

Now let $\mathcal O'$ be an observer moving at velocity $1/2$ in the $y$ direction _wrt_ $\mathcal O$. Then the transformation matrix from $\mathcal O$'s coordinates to the coordinates of $\mathcal O'$ is $${\Lambda ^{\mu'}} _{\mu} = \begin{pmatrix}\frac{2 \sqrt{3}}{3} & 0 & - \frac{\sqrt{3}}{3} & 0\\0 & 1 & 0 & 0\\- \frac{\sqrt{3}}{3} & 0 & \frac{2 \sqrt{3}}{3} & 0\\0 & 0 & 0 & 1
\end{pmatrix}$$
In $\mathcal O'$, the events A, B and C have coordinates $$
\begin{pmatrix}- 2 \sqrt{3}\\-4\\3 \sqrt{3}\\0\end{pmatrix}\quad
\begin{pmatrix}\frac{4 \sqrt{3}}{3}\\0\\- \frac{8 \sqrt{3}}{3}\\0\end{pmatrix}\quad
\begin{pmatrix}\frac{2 \sqrt{3}}{3}\\4\\- \frac{\sqrt{3}}{3}\\0\end{pmatrix}$$
showing that the perceived order is ACB.

```python
Lprime = Matrix([
	[2 / sqrt(3), 0, - 1/ sqrt(3), 0],
	[0, 1, 0, 0],
	[-1/ sqrt(3), 0, 2/ sqrt(3), 0],
	[0, 0, 0, 1]
])
print("A ->", Lprime*A)
print("B ->", Lprime*B)
print("C ->", Lprime*C)
```

To represent the situation in a spacetime diagram we need a 3D plot with $t$, $x$ and $y$.  That is outside of our reach, and the two 2D projection are not as convincing.

![[Drawing 2023-10-19 10.29.11.excalidraw]]
![[Drawing 2023-10-19 10.34.16.excalidraw]]