>Using the tensor transformation law applied to $F_{\mu\nu}$, show how the electric and magnetic field 3-vector $\mathbf E$ and $\mathbf B$ transform under
> **(a)** a rotation about the $y$-axis,
> **(b)** a boost along the $z$-axis.

A rotation of an angle $\theta$ about the $y$ axis is represented by the matrix $${\Lambda^{\mu'}}_\mu = {\Lambda_{\mu'}}^\mu = \begin{pmatrix}1 & 0 & 0 & 0 \\ 0 & \cos\theta & 0 & \sin\theta \\ 0 & 0 & 1 & 0 \\ 0 & -\sin\theta & 0 & \cos\theta\end{pmatrix}$$
Therefore, $$F_{\mu'\nu'} = {\Lambda_{\mu'}}^\mu {\Lambda_{\nu'}}^\nu F_{\mu\nu} = {\Lambda_{\mu'}}^\mu F_{\mu\nu} {\Lambda^\nu}_{\nu'} = $$
$$= \begin{pmatrix}1 & 0 & 0 & 0 \\ 0 & \cos\theta & 0 & \sin\theta \\ 0 & 0 & 1 & 0 \\ 0 & -\sin\theta & 0 & \cos\theta\end{pmatrix}\begin{pmatrix}
0 & -E_1 & -E_2 & -E_3 \\
E_1 & 0 & B_3 & -B_2 \\
E_2 & -B_3 & 0 & B_1 \\
E_3 & B_2 & -B_1 & 0
\end{pmatrix} \begin{pmatrix}1 & 0 & 0 & 0 \\ 0 & \cos\theta & 0 & -\sin\theta \\ 0 & 0 & 1 & 0 \\ 0 & \sin\theta & 0 & \cos\theta\end{pmatrix}$$
$$=
\left(\begin{matrix}
0 & - E_{1} C - E_{3} S  & - E_{2} & E_{1} S - E_{3} C \\
E_{1} C + E_{3} S & 0 & - B_{1} S + B_{3} C & - B_{2} \\
E_{2} & B_{1} S - B_{3} C & 0 & B_{1} C + B_{3} S \\
E_{1} S + E_{3} C & B_{2} & - B_{1} C - B_{3} S & 0
\end{matrix}\right)
$$
Where $C = \cos\theta$ and $S = \sin\theta$. For example, let's check $$\begin{eqnarray}
 & F_{0'1'} & =  {\Lambda_{0'}}^\mu {\Lambda_{1'}}^\nu F_{\mu\nu} = \\ 
 & & = {\Lambda_{0'}}^0 {\Lambda_{1'}}^\nu F_{0\nu} + {\Lambda_{0'}}^1 {\Lambda_{1'}}^\nu F_{1\nu} + {\Lambda_{0'}}^2 {\Lambda_{1'}}^\nu F_{2\nu} + {\Lambda_{0'}}^3 {\Lambda_{1'}}^\nu F_{3\nu} = \\
 & & = 1\cdot {\Lambda_{1'}}^\nu F_{0\nu} + 0\cdot {\Lambda_{1'}}^\nu F_{1\nu} + 0\cdot{\Lambda_{1'}}^\nu F_{2\nu} + 0\cdot {\Lambda_{1'}}^\nu F_{3\nu} = \\
 & & = {\Lambda_{1'}}^\nu  F_{0\nu}= \\
 & & = {\Lambda_{1'}}^0  F_{00} +  {\Lambda_{1'}}^1  F_{01}+  {\Lambda_{1'}}^2  F_{02}+  {\Lambda_{1'}}^3 F_{03} = \\ 
 & & = 0 \cdot  F_{00} +  \cos\theta\cdot  F_{01}+  0\cdot  F_{02}+  \sin\theta\cdot F_{03} = \\
 & & = -\cos\theta\cdot E_1 - \sin\theta\cdot E_3
 \end{eqnarray}$$
For a boost along the $z$-axis we have $${\Lambda^{\mu'}}_\mu = {\Lambda_{\mu'}}^\mu = \begin{pmatrix}
\gamma & 0 & 0 & -v\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ -v\gamma & 0 & 0 & \gamma
\end{pmatrix}$$
$$F_{\mu'\nu'} = {\Lambda_{\mu'}}^\mu {\Lambda_{\nu'}}^\nu F_{\mu\nu} = $$
$$ = \left(\begin{matrix}0 & \gamma \left(- B_{2} v - E_{1}\right) & \gamma \left(B_{1} v - E_{2}\right) & E_{3}\\\gamma \left(B_{2} v + E_{1}\right) & 0 & B_{3} & \gamma \left(- B_{2} - E_{1} v\right)\\\gamma \left(- B_{1} v + E_{2}\right) & - B_{3} & 0 & \gamma \left(B_{1} - E_{2} v\right)\\- E_{3} & \gamma \left(B_{2} + E_{1} v\right) & \gamma \left(- B_{1} + E_{2} v\right) & 0\end{matrix}\right)$$


 
```python
import micropip
await micropip.install('sympy')
from sympy import *

E1, E2, E3, B1, B2, B3, theta, v, gamma = symbols("E1, E2, E3, B1, B2, B3, theta, v, gamma", real=True)
F = Matrix([
	[0, -E1, -E2, -E3],
	[E1, 0, B3, -B2],
	[E2, -B3, 0, B1],
	[E3, B2, -B1, 0]			
])
L = Matrix([
	[1, 0, 0, 0],
	[0, cos(theta), 0, sin(theta)],
	[0, 0, 1, 0],
	[0, -sin(theta), 0, cos(theta)]
])

print("Rotation")
print(latex(simplify(L * F * L.T)))


L = Matrix([
	[gamma, 0, 0, -v*gamma],
	[0, 1, 0, 0],
	[0, 0, 1, 0],
	[-v*gamma, 0, 0, gamma]
])

print("Boost")
print(latex(simplify((L * F * L.T).subs(v**2, 1/gamma**2 + 1))))
```