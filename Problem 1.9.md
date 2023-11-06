>For a system of discrete point particles the energy-momentum tensor takes the form $$T_{\mu\nu} = \sum_a \frac{p_\mu^{(a)} p_\nu^{(a)}}{p^{0(a)}} \delta^{(3)}(\mathbf x - \mathbf x^{(a)})$$ where the index $(a)$ labels the different particles. Show that, for a dense collection of particles with isotropically distributed velocities, we can smooth over the individual particle worldlines to obtain the perfect-fluid energy-momentum tensor.

Let's consider a small portion of spacetime where each particle has mass $m$ and four-velocity $U^{(a)\mu}$. 

$$T_{\mu \nu} = \int_a \frac{p_\mu^{(a)} p_\nu^{(a)}}{p^{0(a)}} = \int_a \frac{ m^2 \, g_{\mu \alpha}U^{(a)\alpha} g_{\nu \beta}U^{(a)\beta}}{m \, \gamma^{(a)}} = m \, g_{\mu \alpha} \, g_{\nu \beta} \int_a \frac{U^{(a)\alpha} U^{(a)\beta}}{\gamma^{(a)}}$$
$$T^{\mu \nu} = m \int_a \frac{U^{(a)\mu} U^{(a)\nu}}{\gamma^{(a)}}$$
$$T^{0 0} = m \int_a \frac{U^{(a)0} U^{(a)0}}{\gamma^{(a)}} = m \int_a \gamma^{(a)} = m \, n \, (\mathrm{mean}\; \gamma) = \rho$$
$$T^{0 j} = m \int_a \frac{U^{(a)0} U^{(a)j}}{\gamma^{(a)}} = m \int_a \gamma^{(a)} v^j = 0$$
$$T^{i j} = m \int_a \frac{U^{(a)i} U^{(a)j}}{\gamma^{(a)}} = m \int_a \gamma^{(a)} v^i v^j = 0$$
$$T^{i i} = m \int_a \frac{U^{(a)i} U^{(a)i}}{\gamma^{(a)}} = m \int_a \gamma^{(a)} (v^i)^2 = m \, n \, (\mathrm{mean}\; \gamma)(\mathrm{mean} \; v)^2 = (\mathrm{pressure})$$
If we call that pressure. It is an energy density, so [energy] / [length]^3 = [force] / [length]^2, so units seem good.