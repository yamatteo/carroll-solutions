> Consider an inertial frame $S$ with coordinates $x^\mu = (t, x, y, z)$, and a frame $S'$ with coordinates $x^{\mu'}$ related to $S$ by a boost with velocity parameter $v$ along the y-axis.
> Imagine we have a wall at rest in $S'$, lying along the line $x' = -y'$. From the point of view of $S$, what is the relationship between the incident angle of a ball hitting the wall (traveling in the $x$-$y$ plane) and the reflected angle? What about the velocity before and after?

Let's start with the wall: consider a rod of length $1$ from point $(1, 0)$ to $(0, 0)$ in $S'$. Being orthogonal to the motion of $S'$ _wrt_ to $S$, it is not affected by contraction and has length $1$ in $S$ as well. On the other hand, a rod of length $1$ between $(1, 0)$ and $(1, -1)$ in $S'$ is parallel to the motion and is contracted in $S$ by a factor $\gamma = (1 - v^2)^{-\frac 12}$. Therefore, in $S$, the wall is not alligned with $y = -x$ but with $y = - (1 / \gamma)\, x$ and it is orthogonal to the vector $\vec n = \langle 1, \gamma \rangle$. 

![](carroll/drawings/slanted_wall3.excalidraw.png)

Suppose that the ball is moving, seen by $S$, with velocity $\vec u = \langle u_x, u_y\rangle$ and it hits the wall at $t = 0$ in the origin $(0, 0)$. By $S$ measures, the angle on incidence $\theta_{\mathrm{in}}$ is such that $$\cos{\theta_\mathrm{in}} = \frac{- \vec u \cdot \vec n}{\Vert \vec u \Vert \; \Vert \vec n \Vert}$$

![](carroll/drawings/angle_of_incidence.excalidraw.png)

The ball has a four-velocity $u^\mu = \langle 1/\sqrt{1 - u^2}, u_x / \sqrt{1 - u^2}, u_y / \sqrt{1 - u^2}, 0 \rangle$ (with $u = \Vert \vec u \Vert$ for brevity) and therefore has four-velocity in $S'$ equal to $$u^{\mu '} = {\Lambda ^{\mu'}} _\alpha u ^\alpha = \left( \begin{matrix}\gamma (1 - v \, u_y) / \sqrt{1 - u^2} \\ u_x / \sqrt{1 - u^2} \\ \gamma (-v + u_y) / \sqrt{1 - u^2} \\ 0 \end{matrix}\right)$$
So from the point of view of $S'$, the ball has a velocity $$ \vec u ' = \begin{pmatrix} \frac{u_x}{\gamma (1 - v u_y)} \\ \frac{-v +u_y}{1 - v u_y}\end{pmatrix} $$ which after the hit gets reflected into $$ \vec w ' = \begin{pmatrix}\frac{v - u_y}{1 - v u_y} \\  \frac{- u_x}{\gamma (1 - v u_y)}\end{pmatrix} $$ corresponding to a four-velocity $$w^{\mu '} = \left( \begin{matrix}\gamma (1 - v \, u_y) / \sqrt{1 - u^2} \\ \gamma (v - u_y) / \sqrt{1 - u^2} \\ -u_x / \sqrt{1 - u^2} \\ 0 \end{matrix}\right)$$. That four-velocity, seem by $S$ is $$ w^{\mu} = {\Lambda ^{\mu}} _{\alpha'} w ^{\alpha'} = \begin{pmatrix} \gamma^2 (1 - v u_y) / \sqrt{1 - u^2} - \gamma v u_x / \sqrt{1 - u^2} \\ \gamma (v - u_y) / \sqrt{1 - u^2} \\ \gamma^2 (1 - v u_y) / \sqrt{1 - u^2} - \gamma u_x  / \sqrt{1 - u^2} \\ 0\end{pmatrix}$$ and it correspond to a velocity $$ \vec{w} = \begin{pmatrix} \frac{v - u_y}{\gamma - \gamma v u_y - v u_x} \\ \frac{\gamma v - \gamma v^2 u_y - u_x}{\gamma - \gamma v u_y - v u_x} \end{pmatrix} $$
![](carroll/drawings/angle_of_reflection.excalidraw.png)
And finally to the ration between the tangents of $\theta_{out}$ and $\theta_{in}$ that is
$$
\frac{\tan(\theta_{out})}{\tan(\theta_{in})} = \frac{\gamma u_{y} + u_{x}}{\gamma \left(- \gamma^{2} u_{y} + \gamma^{2} v - \gamma u_{x} + v\right)}
$$


> To check the calculations, take a look at the [notebook](carroll/notebooks/problem_1_1.ipynb)
