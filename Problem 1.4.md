> Projection effects can trick you into thinking that an asrtrophysical object is moving "superluminally". Consider a quasar that ejects gas with speed $v$ at an angle $\theta$ with respect to the line-of-sight of the observer. Projected onto the sky, the gas appears to travel perpendicula to the line of sight with angular speed $v_{\mathrm{app}} / D$, where $D$ is the distance to the quasar and $v_{\mathrm{app}}$ is the apparent speed. Derive an expression for $v_{\mathrm{app}}$ in terms of $v$ and $\theta$. Show that, for appropriate values of $v$ and $\theta$, $v_{\mathrm{app}}$ can be greater than $1$.

If we thick of $\vec{v}$ as the displacement of the ejected gas in one unit of time, we get a triangle with one side of length $v$ opposed to an angle, say $\alpha$, and another side of length $D$ opposed to an angle $\theta - \alpha$. 

![[Drawing 2023-10-19 14.28.50.excalidraw]]

By trigonometry, $$ v_{\mathrm{app}} = D \, \tan \alpha = D \, \frac{v \, \sin \theta}{D + v \,\cos\theta}$$


```python
import micropip
await micropip.install('sympy')  
from sympy import *

v, D, theta = symbols("v, D, theta", real=True, positive=True)
v = 1 - 10**-9
D = 1000
theta = pi/2 + asin(v / D)/2
w = D * (v * sin(theta)) / (D + v * cos(theta))
print(f"With v = {v}, D = {D} and theta = {theta}, v_app is {w.evalf()}")
```

The maximum effect is achieved when $\theta = \pi - \frac{\pi - \alpha}{2}$. For example with $v = 1 - 10^{-9}$ and $D = 1000$ we get $v_{\mathrm{app}} = 1 + 3.74 \times 10^{-7}$