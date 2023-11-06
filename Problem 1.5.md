> Particle physicists are so used to setting $c = 1$ that they measure mass in units of energy. In particular, they tend to use electron volts ($1 \mathrm{eV} = 1.6 \times 10^{-12} \mathrm{erg} = 1.8 \times 10^{-33} \mathrm{g}$), or, more commoly, keV, MeV, and GeV ($10^3$ eV, $10^6$ eV, and $10^9$ eV, respectively). The muon has been measured to have a mass of $0.106$ GeV and a rest frame lifetime of $2.19 \times 10^{-6}$ seconds. Imagine that such a muon is moving in the circular storage ring of a particle accelerator, 1 kilometer in diameter, such that the muon's total energy is 1000 GeV. How long would it appear to live from the experimenter's point of view? How many radians would it travel around the ring?

If, following the definition, $$-m^2 = p_\mu p^\mu = - E^2 + m^2 \gamma^2 v^2$$
Then $$v = \sqrt{1 - \frac{m^2}{E^2}} = 1 - 5.62\times10^{-9}$$
and the lifetime is dilated to $$\Delta t = \gamma \, \Delta t' = 2.07\times10^{-2}\mathrm{s}$$
In this period it travels $$c \, v \, \Delta t = 6.20 \times 10^6 \mathrm m$$
which corresponds to $$\frac{c\,v\,\Delta t}{(\mathrm{radius})} = 1.24 \times 10^4 \mathrm{rad}$$
```python
import micropip
await micropip.install('sympy')  
from sympy import *

c = 3e8
Dtprime = 2.19e-6
m = 0.106
E = 1000
v = sqrt(1 - (m / E)**2)
print("v - 1 =", N(v - 1))

gamma = 1/sqrt(1 - v**2)
Dt = Dtprime * gamma
print("Lifetime =", Dt)

Dl = v*Dt*c
print("Meters =", Dl)
print("Radians =", Dl / 500)
```