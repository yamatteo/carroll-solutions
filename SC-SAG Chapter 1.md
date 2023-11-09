# Special Relativity and Flat Spacetime

### Prelude

General relativity (GR) is Einstein’s theory of space, time, and gravitation. At heart it is a very simple subject (compared, for example, to anything involving quantum mechanics). The essential idea is perfectly straightforward: while most forces of nature are represented by fields defined on spacetime (such as the electromagnetic field, or the short-range fields characteristic of subnuclear forces), gravity is inherent in spacetime itself. In particular, what we experience as "gravity" is a manifestation of the curvature of spacetime.

Our task, then, is clear. We need to understand spacetime, we need to understand curvature, and we need to understand how curvature becomes gravity. Roughly, the first two chapters of this book are devoted to an exploration of spacetime, the third is about curvature, and the fourth explains the relationship between curvature and gravity, before we get into applications of the theory. However, let’s indulge ourselves with a short preview of what is to come, which will perhaps motivate the initial steps of our journey.

GR is a theory of gravity, so we can begin by remembering our previous theory of gravity, that of Newton. There are two basic elements: an equation for the gravitational field as influenced by matter, and an equation for the response of matter to this field. The conventional Newtonian statement of these rules is in terms of forces between particles; the force between two objects of masses $M$ and $m$ separated by a vector $\mathbf r = r\mathbf e_{r}$ is the famous inverse-square law, $$
\begin{equation}
F = \frac{G M m}{r^2} \mathbf e_r
\tag{1.1}\end{equation}
$$
and this force acts on a particle of mass $m$ to give it an acceleration according to Newton’s second law, $$
\mathbf F= m \mathbf a \tag{1.2}
$$
Equivalently, we could use the language of the gravitational potential $\Phi$; the potential is related to the mass density $\rho$ by Poisson’s equation, $$
\nabla^2 \Phi = 4 \pi G \rho \tag{1.3}
$$
and the acceleration is given by the gradient of the potential, $$
\mathbf a = \nabla \Phi \tag{1.4}
$$
Either (1.1) and (1.2), or (1.3) and (1.4), serve to define Newtonian gravity. To define GR, we need to replace each of them by statements about the curvature of spacetime.
The hard part is the equation governing the response of spacetime curvature to the presence of matter and energy. We will eventually find what we want in the form of Einstein’s equation, $$
R_{\mu\nu} — \frac12 R g_{\mu\nu} = 8 \pi G T_{\mu\nu} \tag{1.5}
$$
This looks more forbidding than it should, largely because of those Greek subscripts. In fact this is simply an equation between 4x4 matrices, and the subscripts label elements of each matrix. The expression on the left-hand side is a measure of the curvature of spacetime, while the right-hand side measures the energy and momentum of matter, so this equation relates energy to curvature, as promised. But we will defer until later a detailed understanding of the inner workings of Einstein’s equation.

The response of matter to spacetime curvature is somewhat easier to grasp: free particles move along paths of "shortest possible distance", or geodesics. In other words, particles try their best to move on straight lines, but in a curved spacetime there might not be any straight lines (in the sense we are familiar with from Euclidean geometry), so they do the next best thing. Their parameterized paths $x^\mu(\lambda)$ obey the geodesic equation:$$
\frac{d^2 x^\mu}{d\lambda^2} + \Gamma^\mu_{\rho\sigma}\frac{dx^\rho}{d\lambda}\frac{dx^\sigma}{d\lambda} = 0 \tag{1.6}
$$
At this point you aren’t expected to understand (1.6) any more than (1.5); but soon enough it will all make sense.

As we will discuss later, the universal nature of geodesic motion is an extremely profound feature of GR. This universality is the origin of our claim that gravity is not actually a "force", but a feature of spacetime. A charged particle in an electric field feels an acceleration, which deflects it from straight-line motion; in contrast, a particle in a gravitational field moves along a path that is the closest thing there is to a straight line. Such particles do not feel acceleration; they are freely falling. Once we become more familiar with the spirit of GR, it will make perfect sense to think of a ball flying through the air as being more truly "unaccelerated" than one sitting on a table; the one sitting on a table is being deflected away from the geodesic it would like to be on (which is why we feel a force on our feet as we stand on Earth).

The basic concept underlying our description of spacetime curvature will be that of the metric tensor, typically denoted by $g_{\mu\nu}$. The metric encodes the geometry of a space by expressing deviations from Pythagoras’s theorem, $(\Delta l)^2 = (\Delta x)^2 + (\Delta y)^2$ (where $\Delta l$ is the distance between two points defined on a Cartesian grid with coordinate separations $\Delta x$ and $\Delta y$. This familiar formula is valid only in conventional Euclidean geometry, where it is implicitly assumed that space is flat. In the presence of curvature our deeply ingrained notions of geometry will begin to fail, and we can characterize the amount of curvature by keeping track of how Pythagoras’s relation is altered. This information is contained in the metric tensor. From the metric we will derive the Riemann curvature tensor, used to define Einstein’s equation, and also the geodesic equation. Setting up this mathematical apparatus is the subject of the next several chapters.

Despite the need to introduce a certain amount of formalism to discuss curvature in a quantitative way, the essential notion of GR ("gravity is the curvature of spacetime") is quite simple. So why does GR have, at least in some benighted circles, a reputation for difficulty or even abstruseness? Because the elegant truths of Einstein’s theory are obscured by the accumulation of certain pre-relativity notions which, although very useful, must first be discarded in order to appreciate the world according to GR. Specifically, we live in a world in which spacetime curvature is very small, and particles are for the most part moving quite slowly compared to the speed of light. Consequently, the mechanics of Galileo and New-
ton comes very naturally to us, even though it is only an approximation to the deeper story.

So we will set about learning the deeper story by gradually stripping away the layers of useful but misleading Newtonian intuition. The first step, which is the subject of this chapter, will be to explore special relativity (SR), the theory of spacetime in the absence of gravity (curvature). Hopefully this is mostly review, as it will proceed somewhat rapidly. The point will be both to recall what SR is all about, and to introduce tensors and related concepts that will be crucial later on, without the extra complications of curvature on top of everything else. Therefore, for this chapter we will always be working in flat spacetime, and furthermore we will only use inertial (Cartesian-like) coordinates. Needless to say it is possible to do SR in any coordinate system you like, but it turns out that introducing the necessary tools for doing so would take us halfway to curved spaces anyway, so we will put that off for a while.

### Space and time, separately and together

A purely cold-blooded approach to GR would reverse the order of Chapter 2 (Manifolds) and Chapter 1 (Special Relativity and Flat Spacetime). A manifold is the kind of mathematical structure used to describe spacetime, while special relativity is a model that invokes a particular kind of spacetime (one with no curvature, and hence no gravity). However, if you are reading this book you presumably have at least some familiarity with special relativity (SR), while you may not know anything about manifolds. So our first step will be to explore the relatively familiar territory of SR, taking advantage of this opportunity to introduce
concepts and notation that will be crucial to later developments.

Special relativity is a theory of the structure of spacetime, the background on which particles and fields evolve. SR serves as a replacement for Newtonian mechanics, which also is a theory of the structure of spacetime. In either case, we can distinguish between this basic structure and the various dynamical laws governing specific systems: Newtonian gravity is an example of a dynamical system set
within the context of Newtonian mechanics, while Maxwell’s electromagnetism is a dynamical system operating within the context of special relativity.

Spacetime is a four-dimensional set, with elements labeled by three dimensions of space and one of time. (We’ll do a more rigorous job with the definitions in the next chapter.) An individual point in spacetime is called an event. The path of a particle is a curve through spacetime, a parameterized one-dimensional set of events, called the worldline. Such a description applies equally to SR and Newtonian mechanics. In either case, it seems clear that “time” is treated somewhat differently than “space”; in particular, particles always travel forward in time, whereas they are free to move back and forth in space.

There is an important difference, however, between the set of allowed paths that particles can take in SR and those in Newton’s theory. In Newtonian mechanics, there is a basic division of spacetime into well-defined slices of “all of space at a fixed moment in time.” The notion of simultaneity, when two events occur at the same time, is unambiguously defined. Trajectories of particles will move ever forward in time, but are otherwise unconstrained; in particular, there is no limit on the relative velocity of two such particles.

In SR the situation is dramatically altered: in particular, there is no well-defined notion of two separated events occurring “at the same time.” That is not to say that spacetime is completely structureless. Rather, at any event we can define a light cone, which is the locus of paths through spacetime that could conceivably be taken by light rays passing through this event. The absolute division, in Newtonian mechanics, of spacetime into unique slices of space parameterized by time, is replaced by a rule that says that physical particles cannot travel faster than light, and consequently move along paths that always remain inside these light cones.

The absence of a preferred time-slicing in SR is at the heart of why the notion of spacetime is more fundamental in this context than in Newtonian mechanics. Of course we can choose specific coordinate systems in spacetime, and once we do, it makes sense to speak of separated events occurring at the same value of the time coordinate in this particular system; but there will also be other possible coordinates, related to the first by “rotating” space and time into each other. This
phenomenon is a natural generalization of rotations in Euclidean geometry, to which we now turn.

Consider a garden-variety two-dimensional plane. It is typically convenient to label the points on such a plane by introducing coordinates, for example by defining orthogonal x and y axes and projecting each point onto these axes in the usual way. However, it is clear that most of the interesting geometrical facts about the plane are independent of our choice of coordinates; there aren’t any preferred
directions. As a simple example, we can consider the distance between two points, given by $$
(\Delta s)^2 = (\Delta x)^2 + (\Delta y )^2 \tag{1.7}
$$

In a different Cartesian coordinate system, defined by x’ and y’ axes that are rotated with respect to the originals, the formula for the distance is unaltered: $$
(\Delta s)^2 = (\Delta x')^2 + (\Delta y')^2 \tag{1.8}
$$
We therefore say that the distance is invariant under such changes of coordinates.

This is why it is useful to think of the plane as an intrinsically two-dimensional space, rather than as two fundamentally distinct one-dimensional spaces brought arbitrarily together: although we use two distinct numbers to label each point, the numbers are not the essence of the geometry, since we can rotate axes into each other while leaving distances unchanged. In Newtonian physics this is not the case with space and time; there is no useful notion of rotating space and time
into each other. Rather, the notion of “all of space at a single moment in time” has a meaning independent of coordinates.

SR is a different story. Let us consider coordinates $(t, x, y, z)$ on spacetime, set up in the following way. The spatial coordinates $(x, y, z)$ comprise a standard Cartesian system, constructed for example by welding together rigid rods that meet at right angles. The rods must be moving freely, unaccelerated. The time coordinate is defined by a set of clocks, which are not moving with respect to the spatial coordinates. (Since this is a thought experiment, we can imagine that the rods are infinitely long and there is one clock at every point in space.) The clocks are synchronized in the following sense. Imagine that we send a beam of
light from point 1 in space to point 2, in a straight line at a constant velocity c, and then immediately back to 1 (at velocity —c). Then the time on the coordinate clock when the light beam reaches point 2, which we label $t_2$, should be halfway between the time on the coordinate clock when the beam left point 1 ($t_1$) and the time on that same clock when it returned ($t_1'$): $$
t_2 = \frac12 (t_1' + t_1) \tag{1.9}
$$The coordinate system thus constructed is an inertial frame, or simply “inertial coordinates.” These coordinates are the natural generalization to spacetime of Cartesian (orthonormal) coordinates in space. (The reason behind the careful construction is so that we only make comparisons locally; never, for example, comparing two far-away clocks to each other at the same time. This kind of care will be even more necessary once we go to general relativity, where there will not be any way to construct inertial coordinates throughout spacetime.)

We can construct any number of inertial frames via this procedure, differing from the first one by an offset in initial position and time, angle, and (constant) velocity. In a Newtonian world, the new coordinates $(t’, x’, y’, z’)$ would have the feature that $t’ = t + \mathrm{constant}$, independent of spatial coordinates. That is, there is an absolute notion of “two events occurring simultaneously, that is, at the same time.” But in SR this isn’t true; in general the three-dimensional “spaces” defined by $t = \text{constant}$ will differ from those defined by $t' = \text{constant}$.

However, we have not descended completely into chaos. Consider, without any motivation for the moment, what we will call the spacetime interval between two events:$$
(\Delta s)^2 = -(c\Delta t)^2 + (\Delta x)^2 + (\Delta y)^2 + (\Delta z)^2 \tag{1.10}
$$
(Notice that it can be positive, negative, or zero even for two nonidentical points.) Here, c is some fixed conversion factor between space and time, that is, a fixed velocity. As an empirical matter, it turns out that electromagnetic waves propagate in vacuum at this velocity c, which we therefore refer to as “the speed of light.” The important thing, however, is not that photons happen to travel at that speed, but that there exists a c such that the spacetime interval is invariant under changes of inertial coordinates. In other words, if we set up a new inertial frame $(t’, x’, y’, z’)$, the interval will be of the same form:$$
(\Delta s)^2 = -(c\Delta t')^2 + (\Delta x')^2 + (\Delta y')^2 + (\Delta z')^2 \tag{1.11}
$$
This is why it makes sense to think of SR as a theory of four-dimensional spacetime, known as Minkowski space. (This is a special case of a four-dimensional manifold, which we will deal with in detail later.) As we shall see, the coordinate transformations that we have implicitly defined do, in a sense, rotate space and time into each other. There is no absolute notion of “simultaneous events”; whether two things occur at the same time depends on the coordinates used. Therefore, the division of Minkowski space into space and time is a choice we make for our own purposes, not something intrinsic to the situation.

Almost all of the “paradoxes” associated with SR result from a stubborn persistence of the Newtonian notions of a unique time coordinate and the existence of “space at a single moment in time.” By thinking in terms of spacetime rather than space and time together, these paradoxes tend to disappear.

Let’s introduce some convenient notation. Coordinates on spacetime will be denoted by letters with Greek superscript indices running from 0 to 3, with 0 generally denoting the time coordinate. Thus,$$
x^\mu \quad : \quad \begin{matrix}
x^0 = ct \\
x^1 = x \\
x^2 = y \\
x^3 = z
\end{matrix}\tag{1.12}
$$
(Don’t start thinking of the superscripts as exponents.) Furthermore, for the sake of simplicity we will choose units in which $$
c=1 \tag{1.13}
$$ we will therefore leave out factors of c in all subsequent formulae. Empirically we know that c is $3 \times 10^8$ meters per second; thus, we are working in units where 1 second equals $3 \times 10^8$ meters. Sometimes it will be useful to refer to the space and time components of $x^\mu$ separately, so we will use Latin superscripts to stand for the space components alone:$$
x^i \quad : \quad \begin{matrix}
x^1 = x \\
x^2 = y \\
x^3 = z
\end{matrix}\tag{1.14}
$$

It is also convenient to write the spacetime interval in a more compact form. We therefore introduce a 4 x 4 matrix, the metric, which we write using two lower indices:$$
\eta_{\mu\nu} = \begin{pmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}\tag{1.15}
$$
(Some references, especially field theory books, define the metric with the opposite sign, so be careful.) We then have the nice formula $$
(\Delta s)^2 = \eta_{\mu\nu} \Delta x^\mu \Delta x ^\nu \tag{1.16}
$$

This formula introduces the summation convention, in which indices appearing both as superscripts and subscripts are summed over. We call such labels dummy indices; it is important to remember that they are summed over all possible values, rather than taking any specific one. (It will always turn out to be the case that dummy indices occur strictly in pairs, with one “upstairs” and one “downstairs.” More on this later.) The content of (1.16) is therefore exactly the same as (1.10).

An extremely useful tool is the spacetime diagram, so let’s consider Minkowski space from this point of view. We can begin by portraying the initial t and x axes at right angles, and suppressing the y and z axes. (“Right angles” as drawn on a spacetime diagram don’t necessarily imply “orthogonal in spacetime,” although that turns out to be true for the $t$ and $x$ axes in this case.) It is enlightening to consider the paths corresponding to travel at the speed c = 1, given by $x = \pm t$. A set of points that are all connected to a single event by straight lines moving
at the speed of light is the light cone, since if we imagine including one more spatial coordinate, the two diagonal lines get completed into a cone. Light cones are naturally divided into future and past; the set of all points inside the future and past light cones of a point p are called timelike separated from p, while those outside the light cones are spacelike separated and those on the cones are lightlike or null separated from p. Referring back to (1.10), we see that the interval
between timelike separated points is negative, between spacelike separated points is positive, and between null separated points is zero. (The interval is defined to be $(\Delta s)^2$, not the square root of this quantity.)

The fact that the interval is negative for a timelike line (on which a slower-
than-light particle will actually move) is annoying, so we define the proper time $\tau$ to satisfy $$
(\Delta \tau)^2 = -(\Delta s)^2 = - \eta_{\mu\nu} \Delta x^\mu \Delta x^\nu \tag{1.17}
$$
A crucial feature of the spacetime interval is that _the proper time between two events measures the time elapsed as seen by an observer moving on a straight path between the events_. This is easily seen in the very special case that the two events have the same spatial coordinates, and are only separated in time; this corresponds to the observer traveling between the events being at rest in the coordinate system used. Then $(\Delta \tau)^2 = -\eta_{\mu\nu} \Delta x^\mu \Delta x^\nu = (\Delta t)^2$, so $\Delta \tau = \Delta t$, and of course we defined $t$ as the time measured by a clock located at a fixed spatial position. But the spacetime interval is invariant under changes of inertial frame; the proper time (1.17) between two fixed events will be the same when evaluated in an inertial frame where the observer is moving as it is in the frame where the observer is at rest.

A crucial fact is that, for more general trajectories, the proper time and coordinate time are different (although the proper time is always that measured by the clock carried by an observer along the trajectory). Consider two trajectories between events A and C, one a straight line passing through a halfway point marked B, and another traveled by an observer moving away from A at a constant velocity $v = dx/dt$ to a point B’ and then back at a constant velocity $-v$ to intersect at the event C. Choose inertial coordinates such that the straight trajectory describes a motionless particle, with event A located at coordinates (t, x) = (0, 0) and C located at ($\Delta t$, 0). The two paths then describe an isosceles triangle in spacetime; B has coordinates ($\frac12 \Delta t$, 0) and B’ has coordinates ($\frac12 \Delta t$, $\Delta x$), with $\Delta x = \frac12 v \Delta t$. Clearly, $\Delta \tau_{AB} = \frac12 \Delta t$, but $$\begin{eqnarray}
\Delta \tau_{AB'} & = & \sqrt{\left(\frac12 \Delta t\right)^2 - (\Delta x)^2} \\
& = & \frac12\sqrt{1 - v^2}\Delta t \tag{1.18}
\end{eqnarray} $$
It should be obvious that $\Delta \tau_{BC} = \Delta \tau_{AB}$ and $\Delta \tau_{B'C} = \Delta \tau_{AB'}$. Thus, the observer on the straight-line trip from event A to C experiences an elapsed time of $\Delta \tau_{ABC} = \Delta t$, whereas the one who traveled out and returned experiences $$
\Delta \tau_{AB'C} = \sqrt{1 - v^2} \Delta t < \Delta t \tag{1.19}
$$
Even though the two observers begin and end at the same points in spacetime, they have aged different amounts. This is the famous “twin paradox,” the unfortunate scene of all sorts of misunderstandings and tortured explanations. The truth is straightforward: a nonstraight path in spacetime has a different interval than a straight path, just as a nonstraight path in space has a different length than a straight one. This isn’t as trivial as it sounds, of course; the profound insight is the way in which “elapsed time along a worldline” is related to the interval traversed
through spacetime. In a Newtonian world, the coordinate t represents a universal flow of time throughout all of spacetime; in relativity, t is just a convenient coordinate, and the elapsed time depends on the path along which you travel. An important distinction is that the nonstraight path has a shorter proper time. In space, the shortest distance between two points is a straight line; in spacetime, the longest proper time between two events is a straight trajectory.

Not all trajectories are nice enough to be constructed from pieces of straight lines. In more general circumstances it is useful to introduce the infinitesimal interval, or **line element**: $$
ds^2 = \eta_{\mu\nu}dx^\mu dx^\nu \tag{1.20}
$$for infinitesimal coordinate displacements $dx^\mu$. (We are being quite informal here, but we’ll make amends later on.) From this definition it is tempting to take the square root and integrate along a path to obtain a finite interval, but it is somewhat unclear what $\int \sqrt{\eta_{\mu\nu} dx^\mu dx^\nu}$ is supposed to mean. Instead we consider a path through spacetime as a parameterized curve, $x^\mu(\lambda)$. Note that, unlike conventional practice in Newtonian mechanics, the parameter $\lambda$ is not necessarily identified with the time coordinate. We can then calculate the derivatives $dx^\mu / d\lambda$, and write the path length along a spacelike curve (one whose infinitesimal intervals are spacelike) as $$
\Delta s = \int \sqrt{\eta_{\mu\nu}\frac{d x^\mu}{d\lambda} \frac{d x^\nu}{d\lambda}} d\lambda \tag{1.21}
$$where the integral is taken over the path. For timelike paths we use the proper time$$
\Delta \tau = \int \sqrt{-\eta_{\mu\nu}\frac{d x^\mu}{d\lambda} \frac{d x^\nu}{d\lambda}} d\lambda \tag{1.22}
$$which will be positive. (For null paths the interval is simply zero.) Of course we may consider paths that are timelike in some places and spacelike in others, but fortunately it is seldom necessary since the paths of physical particles never change their character (massive particles move on timelike paths, massless particles move on null paths). Once again, $\Delta \tau$ really is the time measured by an observer moving along the trajectory.

The notion of acceleration in special relativity has a bad reputation, for no good reason. Of course we were careful, in setting up inertial coordinates, to make sure that particles at rest in such coordinates are unaccelerated. However, once we've set up such coordinates, we are free to consider any sort of trajectories for physical particles, whether accelerated or not. In particular, there is no truth to the rumor that SR is unable to deal with accelerated trajectories, and general relativity must be invoked. General relativity becomes relevant in the presence of gravity, when spacetime becomes curved. Any processes in flat spacetime are described within the context of special relativity; in particular, expressions such as (1.22) are perfectly general.

### Lorentz transformations

We can now consider coordinate transformations in spacetime at a somewhat more abstract level than before. We are interested in a formal description of how to relate the various inertial frames constructed via the procedure outlined above; that is, coordinate systems that leave the interval (1.16) invariant. One simple variety are the **translations**, which merely shift the coordinates (in space or time):$$
x^\mu \to x^{\mu'} = \delta^{\mu'}_\mu(x^\mu + a^\mu)
\tag{1.23}$$ where $a^\mu$ is a set of four fixed numbers and $\delta_\mu^{\mu'}$ is the four-dimensional version of the traditional Kronecker delta symbol:$$
\delta_\mu^{\mu'} = \left\lbrace \begin{matrix}1 \quad \text{ when }\mu' = \mu \\ 0 \quad \text{ when }\mu' \neq \mu\end{matrix}\right.
	\tag{1.24}$$Notice that we put the prime on the index, not on the x. The reason for this should become more clear once we start dealing with vectors and tensors; the notation serves to remind us that the geometrical object is the same, but its components are resolved with respect to a different coordinate system. Translations leave the differences $\Delta x^\mu$ unchanged, so it is not remarkable that the interval is unchanged. The other relevant transformations include spatial **rotations** and offsets by a constant velocity vector, or **boosts**; these are linear transformations, described by multiplying $x^\mu$ by a (spacetime-independent) matrix:$$
x^{\mu'} = {\Lambda^{\mu'}}_\nu x^\nu
\tag{1.25}$$or, in more conventional matrix notation,$$
x' = \Lambda x
\tag{1.26}$$(We will generally use indices, rather than matrix notation, but right now we have an interest in relating our discussion to certain other familiar notions usually described by matrices.) These transformations do not leave the differences $\Delta x^\mu$ unchanged, but multiply them also by the matrix $\Lambda$. What kind of matrices will leave the interval invariant? Sticking with the matrix notation, what we would like is $$
\begin{eqnarray}
(\Delta s)^2 = (\Delta x)^T \eta (\Delta x) & = & (\Delta x')^T \eta (\Delta x') \\
& = & (\Delta x)^T \Lambda^T \eta \Lambda (\Delta x) \tag{1.27}
\end{eqnarray}$$and therefore$$
\eta = \Lambda^T \eta \Lambda \tag{1.28}
$$or $$
\eta_{\rho\sigma} = {\Lambda^{\mu'}}_\rho \eta_{\mu'\nu'}{\Lambda^{\nu'}}_\sigma = {\Lambda^{\mu'}}_\rho {\Lambda^{\nu'}}_\sigma \eta_{\mu'\nu'}
\tag{1.29}$$
(In matrix notation the order matters, while in index notation it is irrelevant.) We want to find the matrices ${\Lambda^{\mu'}}_\nu$ such that the components of the matrix $\eta_{\mu'\nu'}$ are the same as those of $\eta_{\rho\sigma}$; that is what it means for the interval to be invariant under these transformations.

The matrices that satisfy (1.28) are known as the Lorentz transformations;
the set of them forms a group under matrix multiplication, known as the Lorentz
group. There is a close analogy between this group and SO(3), the rotation group
in three-dimensional space. The rotation group can be thought of as 3 x 3 matrices
R that satisfy R'R = 1, where 1 is the 3 x 3 identity matrix. Such matrices are
called orthogonal, and the 3 x 3 ones form the group O(3). This includes not only
rotations but also reversals of orientation of the spatial axes (parity transforma-
tions). Sometimes we choose to exclude parity transformations by also demanding
that the matrices have unit determinant, |R| = 1; such matrices are called special,
and the resulting group is SO(3). The orthogonality condition can be made to look
more like (1.28) if we write it as

```
1 = R™1R. (1.30)
```
So the difference between the rotation group O(3) and the Lorentz group is the
replacement of 1, a 3 x 3 diagonal matrix with all entries equal to +1, by n,
a4 x 4 diagonal matrix with one entry equal to —1 and the rest equal to +1.
The Lorentz group is therefore often referred to as O(3,1). It includes not only
boosts and rotations, but discrete reversals of the time direction as well as parity
transformations. As before we can demand that |A| = 1, leaving the “proper
Lorentz group” SO(3,1). However, this does not leave us with what we really
want, which is the set of continuous Lorentz transformations (those connected
smoothly to the identity), since a combination of a time reversal and a parity
reversal would have unit determinant. From the (9,0) = (0,0) component of
(1.29) we can easily show that |A%'o| > 1, with negative values corresponding to
time reversals. We can therefore demand at last that A” > 1 (inaddition to |A| =
1), leaving the “proper orthochronous” or “restricted” Lorentz group. Sometimes
this is denoted by something like SO(3, 1)*, but usually we will not bother to
make this distinction explicitly. Note that the 3 x 3 identity matrix is simply the
metric for ordinary flat space. Such a metric, in which all of the eigenvalues are
positive, is called Euclidean, while those such as (1.15), which feature a single
minus sign, are called Lorentzian.
It is straightforward to write down explicit expressions for simple Lorentz
transformations. A familiar rotation in the x-y plane is:
1 0 0 O
0 cos@ sind O
0 —sin@ cosd 0
0 0 0 oi

```
,
AM = (1.31)
```

14 Chapter 1 Special Relativity and Flat Spacetime

```
The rotation angle @ is a periodic variable with period 27. The boosts may be
thought of as “rotations between space and time directions.” An example is given
by a boost in the x-direction:
```
```
cosh@ —sinh@ 0 0
/ —sinh@ cosh@ 0 O
1 0
1
```
```
AW = 0 0 (1.32)
0 0 0
```
```
The boost parameter ¢, unlike the rotation angle, is defined from —oo to oo. A
general transformation can be obtained by multiplying the individual transfor-
mations; the explicit expression for this six-parameter matrix (three boosts, three
rotations) is not pretty, or sufficiently useful to bother writing down. In general
Lorentz transformations will not commute, so the Lorentz group is nonabelian.
The set of both translations and Lorentz transformations is a ten-parameter non-
abelian group, the Poincaré group.
You should not be surprised to learn that the boosts correspond to changing
coordinates by moving to a frame that travels at a constant velocity, but let’s see
it more explicitly. Don’t confuse “boosting” with “accelerating.” The difference
between boosting to a different reference frame and accelerating an object is the
same as the difference between rotating to a different coordinate system and set-
ting an object spinning.) For the transformation given by (1.32), the transformed
coordinates t’ and x’ will be given by
```
```
t' =tcosh¢ —xsinh¢
x’ = —tsinh¢@+.xcosh@. (1.33)
```
```
From this we see that the point defined by x’ = 0 is moving; it has a velocity
```
```
x sinhd _
t coshd
```
(^) tanh ¢. (1.34)
To translate into more pedestrian notation, we can replace @ = tanh! v to obtain
t! = y(t — vx)
x’ =y(x — vt), (1.35)
where y = 1/1 — v2. So indeed, our abstract approach has recovered the con-
ventional expressions for Lorentz transformations. Applying these formulae leads
to time dilation, length contraction, and so forth.
It’s illuminating to consider Lorentz transformations in the context of space-
time diagrams. According to (1.33), under a boost in the x-t plane the x’ axis
(t’ = 0) is given by t = x tanh@, while the t’ axis (x’ = 0) is given by tf =
x/tanh @. We therefore see that the space and time axes are rotated into each
other, although they scissor together instead of remaining orthogonal in the tradi-
tional Euclidean sense. (As we shall see, the axes do in fact remain orthogonal in


1.4 &

```
1.4 Vectors 15
```
```
Af
```
```
FIGURE 1.7 A Lorentz transformation relates the {t’, x’} coordinates to the {t, x} coor-
dinates. Note that light cones are unchanged.
```
```
the Lorentzian sense; that’s the implication of the metric remaining invariant un-
der boosts.) This should come as no surprise, since if spacetime behaved just like
a four-dimensional version of space the world would be a very different place. We
see quite vividly the distinction between this situation and the Newtonian world;
in SR, it is impossible to say (in a coordinate-independent way) whether a point
that is spacelike separated from p is in the future of p, the past of p, or “at the
same time.”.
Note also that the paths defined by x’ = -k#’ are precisely the same as those
defined by x = +; these trajectories are left invariant under boosts along the x-
axis. Of course we know that light travels at this speed; we have therefore found
that the speed of light is the same in any inertial frame.
```
```
VECTORS
```
```
To probe the structure of Minkowski space in more detail, it is necessary to intro-
duce the concepts of vectors and tensors. We will start with vectors, which should
be familiar. Of course, in spacetime vectors are four-dimensional, and are often
referred to as four-vectors. This turns out to make quite a bit of difference—for
example, there is no such thing as a cross product between two four-vectors.
Beyond the simple fact of dimensionality, the most important thing to empha-
size is that each vector is located at a given point in spacetime. You may be used
to thinking of vectors as stretching from one point to another in space, and even
of “free” vectors that you can slide carelessly from point to point. These are not
useful concepts outside the context of flat spaces; once we introduce curvature,
we lose the ability to draw preferred curves from one point to another, or to move
vectors uniquely around a manifold. Rather, to each point p in spacetime we as-
sociate the set of all possible vectors located at that point; this set is known as
the tangent space at p, or T,. The name is inspired by thinking of the set of
```

16 Chapter 1 Special Relativity and Flat Spacetime

```
vectors attached to a point on a simple curved two-dimensional space as com-
prising a plane tangent to the point. (This picture relies on an embedding of the
manifold and the tangent space in a higher-dimensional external space, which we
won’t generally have or need.) Inspiration aside, it is important to think of these
vectors as being located at a single point, rather than stretching from one point to
another (although this won’t stop us from drawing them as arrows on spacetime
diagrams).
In Chapter 2 we will relate the tangent space at each point to things we can
construct from the spacetime itself. For right now, just think of T, as an abstract
vector space for each point in spacetime. A (real) vector space is a collection of
objects (vectors) that can be added together and multiplied by real numbers in a
linear way. Thus, for any two vectors V and W and real numbers a and b, we have
```
(a+b)\(V+W) =aV +b6V +aW +bW. (1.36)

```
Every vector space has an origin, that is, a zero vector that functions as an identity
element under vector addition. In many vector spaces there are additional oper-
ations such as taking an inner (dot) product, but this is extra structure over and
above the elementary concept of a vector space.
A vector is a perfectly well-defined geometric object, as is a vector field, de-
fined as a set of vectors with exactly one at each point in spacetime. [The set of all
the tangent spaces of an n-dimensional manifold M can be assembled into a 2n-
dimensional manifold called the tangent bundle, 7 (M). It is a specific example
of a “fiber bundle,” which is endowed with some extra mathematical structure; we
won’t need the details for our present purposes.] Nevertheless it is often useful to
decompose vectors into components with respect to some set of basis vectors. A
basis is any set of vectors which both spans the vector space (any vector is a linear
combination of basis vectors) and is linearly independent (no vector in the basis
```
```
FIGURE 1.8 A suggestive drawing of the tangent space Tp, the space of all vectors at
the point p.
```

```
1.4 Vectors 17
```
```
is a linear combination of other basis vectors). For any given vector space, there
will be an infinite number of possible bases we could choose, but each basis will
consist of the same number of vectors, known as the dimension of the space. (For
a tangent space associated with a point in Minkowski space, the dimension is, of
course, four.)
Let us imagine that at each tangent space we set up a basis of four vectors é(,,),
with w € {0, 1, 2, 3} as usual. In fact let us say that each basis is “adapted to the
coordinates x”’—that is, the basis vector €(,) is what we would normally think
of pointing along the x-axis. It is by no means necessary that we choose a basis
adapted to any coordinate system at all, although it is often convenient. (As before,
we really could be more precise here, but later on we will repeat the discussion
at an excruciating level of precision, so some sloppiness now is forgivable.) Then
any abstract vector A can be written as a linear combination of basis vectors:
```
A= AMéeyy. (1.37)

The coefficients A“ are the components of the vector A. More often than not
we will forget the basis entirely and refer somewhat loosely to “the vector A“,”
but keep in mind that this is shorthand. The real vector is an abstract geometrical
entity, while the components are just the coefficients of the basis vectors in some
convenient basis. (Since we will usually suppress the explicit basis vectors, the
indices usually will label components of vectors and tensors. This is why there
are parentheses around the indices on the basis vectors, to remind us that this is a
collection of vectors, not components of a single vector.)
A standard example of a vector in spacetime is the tangent vector to a curve.
A parameterized curve or path through spacetime is specified by the coordinates
as a function of the parameter, for example, x“ (1). The tangent vector V (A) has
components

```
we dx
v di
```
```
(1.38)
```
The entire vector is V = V“é;,,). Under a Lorentz transformation the coordinates
x change according to (1.25), while the parameterization 1 is unaltered; we can
therefore deduce that the components of the tangent vector must change as

VE > VE = AK vy”. (1.39)

However, the vector V itself (as opposed to its components in some coordinate
system) is invariant under Lorentz transformations. We can use this fact to derive
the transformation properties of the basis vectors. Let us refer to the set of basis
vectors in the transformed coordinate system as ew ): Since the vector is invariant,
we have

V = Vey = VY ew = A” Veen. (1.40)


18 Chapter 1 Special Relativity and Flat Spacetime

```
But this relation must hold no matter what the numerical values of the components
V" are. We can therefore say
```
ey) = A” pew. (1.41)

```
To get the new basis é(,) in terms of the old one é,,,), we should multiply by the
inverse of the Lorentz transformation A” y- But the inverse of a Lorentz transfor-
mation from the unprimed to the primed coordinates is also a Lorentz transforma-
_ tion, this time from the primed to the unprimed systems. We will therefore intro-
```
```
1.
```
```
duce a somewhat subtle notation, by using the same symbol for both matrices, just
with primed and unprimed indices switched. That is, the Lorentz transformation
specified by A“’, has an inverse transformation written as A?,/. Operationally
this implies
```
AMy AY) = dH, AT AA = 8%), (1.42)

```
From (1.41) we then obtain the transformation rule for basis vectors:
```
bw = AM eq. (1.43)

```
Therefore the set of basis vectors transforms via the inverse Lorentz transforma-
tion of the coordinates or vector components.
Let’s pause a moment to take all this in. We introduced coordinates labeled
by upper indices, which transformed in a certain way under Lorentz transforma-
tions. We then considered vector components that also were written with upper
indices, which made sense since they transformed in the same way as the coordi-
nate functions. (In a fixed coordinate system, each of the four coordinates x“ can
be thought of as a function on spacetime, as can each of the four components of a
vector field.) The basis vectors associated with the coordinate system transformed
via the inverse matrix, and were labeled by a lower index. This notation ensured
that the invariant object constructed by summing over the components and ba-
sis vectors was left unchanged by the transformation, just as we would wish. It’s
probably not giving too much away to say that this will continue to be the case
for tensors, which may have multiple indices.
```
```
DUAL VECTORS (ONE-FORMS)
```
```
Once we have set up a vector space, we can define another associated vector space
(of equal dimension) known as the dual vector space. The dual space is usually
denoted by an asterisk, so that the dual space to the tangent space T,, called the
cotangent space, is denoted T>. The dual space is the space of all linear maps
from the original vector space to the real numbers; in math lingo, if w € T; isa
dual vector, then it acts as a map such that
```
```
o(aV +bW) = aw(V)+ ba(W) ER, (1.44)
```

```
1.5 Dual Vectors (One-Forms) 19
```
```
where V, W are vectors and a, b are real numbers. The nice thing about these
maps is that they form a vector space themselves; thus, if w and n are dual vectors,
we have
```
```
(aw + bn)(V) = aw(V) + bn(V). (1.45)
```
```
To make this construction somewhat more concrete, we can introduce a set of
basis dual vectors 6) by demanding
```
6 yy) = 8. (1.46)

```
Then every dual vector can be written in terms of its components, which we label
with lower indices:
```
o= 0,6, (1.47)

Usually, we will simply write w,,, in perfect analogy with vectors, to stand for the
entire dual vector. In fact, you will sometimes see elements of T, (what we have
called vectors) referred to as contravariant vectors, and elements of T; (what we
have called dual vectors) referred to as covariant vectors, although in this day and
age these terms sound a little dated. If you just refer to ordinary vectors as vectors
with upper indices and dual vectors as vectors with lower indices, nobody should
be offended. Another name for dual vectors is one-forms, a somewhat mysterious
designation that will become clearer in Chapter 2.
The component notation leads to a simple way of writing the action of a dual
vector on a vector:

o(V) = 0,0 (Vey)

```
= 0, V’d™ (é))
= 0,V" dt
=o,V" ER. (1.48)
```
This is why it is rarely necessary to write the basis vectors and dual vectors ex-
plicitly; the components do all of the work. The form of (1.48) also suggests that
we can think of vectors as linear maps on dual vectors, by defining

```
V(@) = @(V) =a, V". (1.49)
```
```
Therefore, the dual space to the dual vector space is the original vector space
itself.
Of course in spacetime we will be interested not in a single vector space, but
in fields of vectors and dual vectors. [The set of all cotangent spaces over M can
be combined into the cotangent bundle, 7*(M).] In that case the action of a
dual vector field on a vector field is not a single number, but a scalar (function)
on spacetime. A scalar is a quantity without indices, which is unchanged under
```

20 Chapter 1 Special Relativity and Flat Spacetime

```
Lorentz transformations; it is a coordinate-independent map from spacetime to
the real numbers.
We can use the same arguments that we earlier used for vectors (that geomet-
rical objects are independent of coordinates, even if their components are not)
to derive the transformation properties of dual vectors. The answers are, for the
components,
```
```
On = AY yy, (1.50)
```
```
and for basis dual vectors,
pe’) = Af .6®), (1.51)
```
```
This is just what we would expect from index placement; the components of a
dual vector transform under the inverse transformation of those of a vector. Note
that this ensures that the scalar (1.48) is invariant under Lorentz transformations,
just as it should be.
In spacetime the simplest example of a dual vector is the gradient of a scalar
function, the set of partial derivatives with respect to the spacetime coordinates,
which we denote by a lowercase d:
ad «
dd = d axe —— 6), (1.52) 52
```
```
The conventional chain rule used to transform partial derivatives amounts in this
case to the transformation rule of components of dual vectors:
dd ax" dg
axl! ax! axl
```
— Au Ay", ,2e dg (1.53)

```
where we have used (1.25) to relate the Lorentz transformation to the coordinates. —
The fact that the gradient is a dual vector leads to the following shorthand nota-
tions for partial derivatives:
```
axe ag In? = Ps). (1.54)

```
So, x“ has an upper index, but when it is in the denominator of a derivative it
implies a lower index on the resulting object. In this book we will generally use
0, rather than the comma notation. Note that the gradient does in fact act in a*
natural way on the example we gave above of a vector, the tangent vector to a
curve. The result is an ordinary derivative of the function along the curve:
```
```
ax — do
a,¢— uP an = dh. (1.55)1.
```

1.6

```
1.6 Tensors 21
```
```
TENSORS
```
```
A straightforward generalization of vectors and dual vectors is the notion of a
tensor. Just as a dual vector is a linear map from vectors to R, a tensor T of type
(or rank) (k, /) is a multilinear map from a collection of dual vectors and vectors
to R:
```
```
T: T)x---xXT)xTpx---xTp>R (1.56)
(k times) (J times)
```
```
Here, “x” denotes the Cartesian product, so that for example T,, x T, is the space
of ordered pairs of vectors. Multilinearity means that the tensor acts linearly in
each of its arguments; for instance, for a tensor of type (1, 1), we have
```
```
T (aw + bn, cV + dW) = acT (a, V)
+ adT(w, W) + bcT(n, V) + bdT(n, W). (1.57)
```
```
From this point of view, a scalar is a type (0, 0) tensor, a vector is a type (1, 0)
tensor, and a dual vector is a type (0, 1) tensor.
The space of all tensors of a fixed type (k, 1) forms a vector space; they can
be added together and multiplied by real numbers. To construct a basis for this
space, we need to define a new operation known as the tensor product, denoted
by @. If T is a (k, J) tensor and S is an (m, n) tensor, we define a (k + m,1 +n)
tensor T ® S by
```
```
T @S@™,...,0,...,0™, VO, VO, VM)
=T(o,...,0,V,..., Vv)
x S(oO™FTD wt yD yr), (1.58)
```
```
Note that the o and V are distinct dual vectors and vectors, not components
thereof. In other words, first act T on the appropriate set of dual vectors and
vectors, and then act § on the remainder, and then multiply the answers. Note
that, in general, tensor products do not commute: T @S #S QT.
It is now straightforward to construct a basis for the space of all (k, /) tensors,
by taking tensor products of basis vectors and dual vectors; this basis will consist
of all tensors of the form
```
```
b (11) B+ @ lug) QOD @...Q OM, (1.59)
```
```
In a four-dimensional spacetime there will be 4*+” basis tensors in all. In compo-
nent notation we then write our arbitrary tensor as
```
T TH uy) B+ @ luz) @ ACY @--- BO. (1.60)


22 Chapter 1 Special Relativity and Flat Spacetime

```
Alternatively, we could define the components by acting the tensor on basis vec-
tors and dual vectors:
```
TH Hy = TOY, ..., 8, Buy), Bu). (1.61)

```
You can check for yourself, using (1.46) and so forth, that these equations all hang
together properly.
As with vectors, we will usually take the shortcut of denoting the tensor T by
its components T“1'#*,,...),. The action of the tensors on a set of vectors and
dual vectors follows the pattern established in (1.48):
```
```
T(o™, bees o), vo, — v) _ TH Hey yo) Lo. of) yOu... yOu,
```
```
(1.62)
```
```
A (k,1) tensor thus has k upper indices and / lower indices. The order of the
indices is obviously important, since the tensor need not act in the same way on
its various arguments.
Finally, the transformation of tensor components under Lorentz transforma-
tions can be derived by applying what we already know about the transformation
of basis vectors and dual vectors. The answer is just what you would expect from
index placement,
, _ , = AM, / .-.- A , Mee AY 1k
TH Hy oy = AM AM AM AMY TH ay, (1.63)
```
```
Thus, each upper index gets transformed like a vector, and each lower index gets
transformed like a dual vector.
Although we have defined tensors as linear maps from sets of vectors and tan-
gent vectors to R, there is nothing that forces us to act on a full collection of
arguments. Thus, a (1, 1) tensor also acts as a map from vectors to vectors:
```
TH, Vi > TA”. (1.64)

```
You can check for yourself that T“,,V” is a vector (that is, obeys the vector trans-
formation law). Similarly, we can act one tensor on (all or part of) another tensor
to obtain a third tensor. For example,
```
UM, = TH S oy (1.65)

```
is a perfectly good (1, 1) tensor.
You may be concerned that this introduction to tensors has been somewhat too
brief, given the esoteric nature of the material. In fact, the notion of tensors does
not require a great deal of effort to master; it’s just a matter of keeping the indices
straight, and the rules for manipulating them are very natural. Indeed, a number of
books like to define tensors as collections of numbers transforming according to
(1.63). While this is operationally useful, it tends to obscure the deeper meaning
of tensors as geometrical entities with a life independent of any chosen coordinate
```

```
1.6 Tensors. 23
```
```
system. There is, however, one subtlety that we have glossed over. The notions of
dual vectors and tensors and bases and linear maps belong to the realm of linear
algebra, and are appropriate whenever we have an abstract vector space at hand. In
the case of interest to us we have not just a vector space, but a vector space at each
point in spacetime. More often than not we are interested in tensor fields, which
can be thought of as tensor-valued functions on spacetime. Fortunately, none of
the manipulations we defined above really care whether we are dealing with a
single vector space or a collection of vector spaces, one for each event. We will
be able to get away with simply calling things functions of x“ when appropriate.
However, you should keep straight the logical independence of the notions we
have introduced and their specific application to spacetime and relativity.
In spacetime, we have already seen some examples of tensors without calling
them that. The most familiar example of a (0, 2) tensor is the metric, ny. The
action of the metric on two vectors is so useful that it gets its own name, the inner
product (or scalar product, or dot product):
```
n(V, W) = nuvV“W" = V-W. (1.66)

```
Just as with the conventional Euclidean dot product, we will refer to two vectors
whose inner product vanishes as orthogonal. Since the inner product is a scalar,
it is left invariant under Lorentz transformations; therefore, the basis vectors of
any Cartesian inertial frame, which are chosen to be orthogonal by definition, are
still orthogonal after a Lorentz transformation (despite the “scissoring together”
we noticed earlier). The norm of a vector is defined to be inner product of the
vector with itself; unlike in Euclidean space, this number is not positive definite:
<0, Vis timelike
if nuvV"V” is | =0, Vis lightlike or null
> 0, Vis spacelike.
```
(A vector can have zero norm without being the zero vector.) You will notice
that the terminology is the same as that which we used earlier to classify the
_ relationship between two points in spacetime; it’s no accident, of course, and we
will go into more detail later.
Another tensor is the Kronecker delta 6 5 , of type (1, 1). Thought of as a map
from vectors to vectors (or one-forms to one-forms), the Kronecker delta is simply
“the identity map. We follow the example of many other references in placing the
upper and lower indices in the same column for this unique tensor; purists might
write 6“, or 5), but these would be numerically identical, and we shouldn’t get
in trouble being careless in this one instance.
Related to the Kronecker delta and the metric is the inverse metric 7”, a type
(2, 0) tensor defined (unsurprisingly) as the “inverse” of the metric:

```
1’ tp = Nov = 8). (1.67)
(It’s the inverse metric since, when multiplied by the metric, it yields the identity
map.) In fact, as you can check, the inverse metric has exactly the same compo-
```

24 Chapter 1 Special Relativity and Flat Spacetime

```
nents as the metric itself. This is only true in flat space in Cartesian coordinates,
and will fail to hold in more general situations. There is also the Levi—Civita
symbol, a (0, 4) tensor:
```
```
—1 if wvpo is an odd permutation of 0123 (1.68)
```
```
+1 if wvpo is an even permutation of 0123
Ewvpo =
0 otherwise.
Here, a “permutation of 0123” is an ordering of the numbers 0, 1, 2, 3, which
can be obtained by starting with 0123 and exchanging two of the digits; an even
permutation is obtained by an even number of such exchanges, and an odd per-
mutation is obtained by an odd number. Thus, for example, 932; = —1. (The
tilde on E,.,9., and referring to it as a symbol rather than simply a tensor, derive
from the fact that this object is actually not a tensor in more general geometries or
coordinates; instead, it is something called a “tensor density.” It is straightforward
enough to define a related object that is a tensor, which we will denote by €,y 50
and call the “Levi—Civita tensor.” See Chapter 2 for a discussion.)
A remarkable property of the above tensors—the metric, the inverse metric,
the Kronecker delta, and the Levi-Civita symbol—is that, even though they all
transform according to the tensor transformation law (1.63), their components re-
main unchanged in any inertial coordinate system in flat spacetime. In some sense
this makes them nongeneric examples of tensors, since most tensors do not have
this property. In fact, these are the only tensors with this property, although we
won’t prove it. The Kronecker delta is even more unusual, in that it has exactly
the same components in any coordinate system in any spacetime. This makes
sense from the definition of a tensor as a linear map; the Kronecker tensor can
be thought of as the identity map from vectors to vectors (or from dual vectors
to dual vectors), which clearly must have the same components regardless of co-
ordinate system. Meanwhile, the metric and its inverse characterize the structure
of spacetime, while the Levi—Civita symbol is secretly not a true tensor at all.
We shall therefore have to treat these objects more carefully when we drop our
assumption of flat spacetime.
A more typical example of a tensor is the electromagnetic field strength ten-
sor. We all know that the electromagnetic fields are made up of the electric field
vector E; and the magnetic field vector B;. (Remember that we use Latin indices
for spacelike components 1, 2, 3.) Actually these are only “vectors” under rota-
tions in space, not under the full Lorentz group. In fact they are components of a
(0, 2) tensor F,,, defined by
```
```
0 -E, —-E, —£3
Fy 0 B; —Bo
Ey —B3 0 By
E3; Bo -—B, 0
```
Fyy = =—Fy,. (1.69)

```
From this point of view it is easy to transform the electromagnetic fields in one
reference frame to those in another, by application of (1.63). The unifying power
of the tensor formalism is evident: rather than a collection of two vectors whose
```

1.7 i

1.7 Manipulating Tensors 25

```
relationship and transformation properties are rather mysterious, we have a single
tensor field to describe all of electromagnetism. (On the other hand, don’t get car-
ried away; sometimes it’s more convenient to work in a single coordinate system
using the electric and magnetic field vectors.)
```
```
MANIPULATING TENSORS
```
```
With these examples in hand we can now be a little more systematic about some
properties of tensors. First consider the operation of contraction, which tums a
(k, 1) tensor into a (k — 1,1 — 1) tensor. Contraction proceeds by summing over
one upper and one lower index:
```
SHO, = TH Sy. (1.70)

```
You can check that the result is a well-defined tensor. It is only permissible to
contract an upper index with a lower index (as opposed to two indices of the same
type); otherwise the result would not be a well-defined tensor. (By well-defined
tensor we mean either “transforming according to the tensor transformation law,’
or “defining a unique multilinear map from a set of vectors and dual vectors to the
real numbers”; take your pick.) Note also that the order of the indices matters, so
that you can get different tensors by contracting in different ways; thus,
```
```
THe oy FTP cy (1.71)
in general.
The metric and inverse metric can be used to raise and lower indices on ten-
sors. That is, given a tensor T# 5, we can use the metric to define new tensors,
which we choose to denote by the same letter T:
TBH, _ nh¥ TH 5,
```
```
Ty ys = nual? ys,
Ty? = nuanoen’’ nT 5, (1.72)
```
```
and so forth. Notice that raising and lowering does not change the position of an
index relative to other indices, and also that free indices (which are not summed
over) must be the same on both sides of an equation, while dummy indices (which
are summed over) only appear on one side. As an example, we can turn vectors
and dual vectors into each other by raising and lowering indices:
```
```
Vi =NuvV”
ao =n” aw, (1.73)
```
```
Because the metric and inverse metric are truly inverses of each other, we are free
to raise and lower simultaneously a pair of indices being contracted over:
```
A* By, = 1? Apna BY = 58 A,B? = Ag BY. (1.74)


26 Chapter 1 Special Relativity and Flat Spacetime

```
The ability to raise and lower indices with a metric explains why the gradient
in three-dimensional flat Euclidean space is usually thought of as an ordinary
vector, even though we have seen that it arises as a dual vector; in Euclidean
space (where the metric is diagonal with all entries +1) a dual vector is turned
into a vector with precisely the same components when we raise its index. You
may then wonder why we have belabored the distinction at all. One simple reason,
of course, is that in a Lorentzian spacetime the components are not equal:
```
wo = (—ap, @1, @2, @3). (1.75)

```
In a curved spacetime, where the form of the metric is generally more compli-
cated, the difference is rather more dramatic. But there is a deeper reason, namely
that tensors generally have a “natural” definition independent of the metric. Even
though we will always have a metric available, it is helpful to be aware of the
logical status of each mathematical object we introduce. The gradient, with its
action on vectors, is perfectly well-defined regardless of any metric, whereas the
“gradient with upper indices” is not. (As an example, we will eventually want to
take variations of functionals with respect to the metric, and will therefore have to
know exactly how the functional depends on the metric, something that is easily
obscured by the index notation.)
Continuing our compilation of tensor jargon, we refer to a tensor as symmetric
in any of its indices if it is unchanged under exchange of those indices. Thus, if
```
Suvp = Svyp> (1.76)

```
we say that S,,y) is symmetric in its first two indices, while if
```
```
Suvp = Supv = Spyv = Svup = Srp = Spvps (1.77)
we say that S,.yo is symmetric in all three of its indices. Similarly, a tensor is
antisymmetric (or skew-symmetric) in any of its indices if it changes sign when
those indices are exchanged; thus,
```
Ayvp = —Apvyp (1.78)

```
means that A,,yp) is antisymmetric in its first and third indices (or just “antisym-
metric in yz and p”). If a tensor is (anti-) symmetric in all of its indices, we refer -
to it as simply (anti-) symmetric (sometimes with the redundant modifier “com-
pletely”). As examples, the metric y,,, and the inverse metric n“” are symmetric,
while the Levi—Civita symbol €,,y 9. and the electromagnetic field strength ten-
sor F,» are antisymmetric. (Check for yourself that if you raise or lower a set of
indices that are symmetric or antisymmetric, they remain that way.) Notice that
it makes no sense to exchange upper and lower indices with each other, so don’t
succumb to the temptation to think of the Kronecker delta 4% as symmetric. On
the other hand, the fact that lowering an index on 53 gives a symmetric tensor (in
fact, the metric) means that the order of indices doesn’t really matter, which is
why we don’t keep track of index placement for this one tensor.
```

1.7. Manipulating Tensors 27

Given any tensor, we can symmetrize (or antisymmetrize) any number of its
upper or lower indices. To symmetrize, we take the sum of all permutations of the
relevant indices and divide by the number of terms:

Tp.) 09"+[1n)p° = al (Tyjp9+-pn” + Sum Over permutations of indices j11 --- Ln),

```
(1.79)
```
while antisymmetrization comes from the alternating sum:

```
1.
Thyjp2pnlo = av (Tyjpo-pnp° + alternating sum over (1.80)
* permutations of indices [41 --- [n).
```
By “alternating sum” we mean that permutations that are the result of an odd
number of exchanges are given a minus sign, thus:

```
Tiyvplo = : (Tuvpe — Tupve + Ture — Toupe + Trpps — Tove). (1-81)
```
Notice that round/square brackets denote symmetrization/antisymmetrization.
Furthermore, we may sometimes want to (anti-) symmetrize indices that are
not next to each other, in which case we use vertical bars to denote indices not
included in the sum:

Tlie) = 3 (Tuo + Tovu) - (1.82)

If we are contracting over a pair of upper indices that are symmetric on one tensor,
only the symmetric part of the lower indices will contribute; thus,

XHYY yy = XM Yor, (1.83)

regardless of the symmetry properties of Y,,,. (Analogous statements hold for an-
tisymmetric indices, or if it’s the lower indices that are symmetric to start with.)
For any two indices, we can decompose a tensor into symmetric and antisymmet-
ric parts,

```
Tuvpo = Tip) + Thuvipo (1.84)
```
but this will not in general hold for three or more indices,

```
Tyvpo F Twvp)o + Thuvple» (1.85)
```
because there are parts with mixed symmetry that are not specified by either
the symmetric or antisymmetric pieces. Finally, some people use a convention
in which the factor of 1/n! is omitted. The one used here is a good one, since, for
example, a symmetric tensor satisfies


28 Chapter 1 Special Relativity and Flat Spacetime

Syiy-tin = Styugepin)> (1.86)

```
and likewise for antisymmetric tensors.
For a (1, 1) tensor X“,, the trace is a scalar, often denoted by leaving off the
indices, which is simply the contraction:
```
X=X,. (1.87)

```
If we think of X“, as a matrix, this is just the sum of the diagonal components,
so it makes sense. However, we will also use trace in the context of a (0, 2) tensor
Y,,v, in which case it means that we should first raise an index (Y" = g’*Y,y)
and then contract:
```
Y=¥*, = 7"'¥ yy. (1.88)

```
(It must be this way, since we cannot sum over two lower indices.) Although
this is the sum of the diagonal components of Y“,, it is certainly not the sum of
the diagonal components of Y,,,,; we had to raise an index, which in general will
change the numerical value of the components. For example, you might guess that
the trace of the metric is -1 + 1+1-+1 = 2, but it’s not:
```
nu» = 6 = 4. (1.89)

```
(In n dimensions, Si = n.) There is no reason to denote this trace by g (or 4),
since it will always be the same number, even after we make the transition to
curved spaces where the metric components are more complicated. Note that an-
tisymmetric (0, 2) tensors are always traceless.
We have been careful so far to distinguish clearly between things that are al-
ways true (on a manifold with arbitrary metric) and things that are only true in |
Minkowski space in inertial coordinates. One of the most important distinctions
arises with partial derivatives. If we are working in flat spacetime with inertial
coordinates, then the partial derivative of a (k, 1) tensor is a (k,1 + 1) tensor;.
that is,
```
```
Ty = Og RM y (1.90)
```
```
transforms properly under Lorentz transformations. However, this will no longer
be true in more general spacetimes, and we will have to define a covariant deriva-
tive to take the place of the partial derivative. Nevertheless, we can still use the
fact that partial derivatives give us tensor in this special case, as long as we keep
our wits about us. [The one exception to this warning is the partial derivative
of a scalar, dv¢, which is a perfectly good tensor (the gradient) in any space-
time.] Of course, if we fix a particular coordinate system, the partial derivative is
a perfectly good operator, which we will use all the time; its failure is only that
it doesn’t transform in the same way as the tensors we will be using (or equiv-
alently, that the map it defines is not coordinate-independent). One of the most
```

1.8 0

1.8 Maxwell’s Equations 29

```
useful properties of partial derivatives is that they commute,
```
Ody ++) = IyInC +) (1.91)

```
no matter what kind of object is being differentiated.
```
```
MAXWELL'S EQUATIONS
```
```
We have now accumulated enough tensor know-how to illustrate some of these
concepts using actual physics. Specifically, we will examine Maxwell’s equa-
tions of electrodynamics. In 19th-century notation, these are
```
```
VxB-daE=J
V-E=op
VxE+0,B=0
V-B=0. (1.92)
```
```
Here, E and B are the electric and magnetic field 3-vectors, J is the current, p
is the charge density, and Vx and V- are the conventional curl and divergence.
These equations are invariant under Lorentz transformations, of course; that’s how
the whole business got started. But they don’t look obviously invariant; our ten-
sor notation can fix that. Let’s begin by writing these equations in component
notation,
```
eka B, — aE! = J'

```
aE! = J°
éJk9, Ey, + Ip B' =0
```
4; Bi = 0. (1.93)

```
In these expressions, spatial indices have been raised and lowered with aban-
don, without any attempt to keep straight where the metric appears, because 6;;
is the metric on flat 3-space, with 6'/ its inverse (they are equal as matrices).
We can therefore raise and lower indices at will, since the components don’t
change. Meanwhile, the three-dimensional Levi-Civita symbol é‘/* is defined
just as the four-dimensional one, although with one fewer index (normalized
so that €123 = €3 = 1). We have replaced the charge density by J°; this is
legitimate because the density and current together form the current 4-vector,
JH =(p,J*, J, J).
From (1.93), and the definition (1.69) of the field strength tensor Fy, it is easy
to get a completely tensorial 20th-century version of Maxwell’s equations. Begin
by noting that we can express the field strength with upper indices as
```

30

```
1.9
```
```
Chapter 1 Special Relativity and Flat Spacetime
```
FU = ek, (1.94)

```
To check this, note for example that F°! = 49n1! Fo, and F!? = €!3B3. Then
the first two equations in (1.93) become
```
0;F —aF% = J!

ajF% = 9. (1.95)

```
Using the antisymmetry of F“’, we see that these may be combined into the
single tensor equation
```
OF = J”. (1.96)

```
A similar line of reasoning, which is left as an exercise, reveals that the third and
fourth equations in (1.93) can be written
```
OtuF yy = 0. (1.97)

```
It’s simple to verify that the antisymmetry of F,,, implies that (1.97) can be equiv-
alently expressed as
```
```
On Fun + Oy Fi + 0. Fav = 0. (1.98)
```
```
The four traditional Maxwell equations are thus replaced by two, vividly
demonstrating the economy of tensor notation. More importantly, however, both
sides of equations (1.96) and (1.97) manifestly transform as tensors; therefore, if
they are true in one inertial frame, they must be true in any Lorentz-transformed
frame. This is why tensors are so useful in relativity—-we often want to express
relationships without recourse to any reference frame, and the quantities on each
side of an equation must transform in the same way under changes of coordinates.
As a matter of jargon, we will sometimes refer to quantities written in terms of
tensors as covariant (which has nothing to do with “covariant” as opposed to
“contravariant’”). Thus, we say that (1.96) and (1.97) together serve as the covari-
ant form of Maxwell’s equations, while (1.92) or (1.93) are noncovariant.
```
```
ENERGY AND MOMENTUM
```
```
We’ve now gone over essentially everything there is to know about the care and
feeding of tensors. In the next chapter we will look more carefully at the rigorous
definitions of manifolds and tensors, but the basic mechanics have been pretty
well covered. Before jumping to more abstract mathematics, let’s review how
physics works in Minkowski spacetime.
Start with the worldline of a single particle. This is specified by amap R > M,
where M is the manifold representing spacetime; we usually think of the path as
```

```
1.9 Energy and Momentum 31
```
a parameterized curve x"(A). As mentioned earlier, the tangent vector to this path
is dx“ /dd (note that it depends on the parameterization). An object of primary
interest is the norm of the tangent vector, which serves to characterize the path;
if the tangent vector is timelike/null/spacelike at some parameter value 4, we say
that the path is timelike/null/spacelike at that point. This explains why the same
words are used to classify vectors in the tangent space and intervals between two
points—because a straight line connecting, say, two timelike separated points will
itself be timelike at every point along the path.
Nevertheless, be aware of the sleight of hand being pulled here. The metric,
as a (0, 2) tensor, is a machine that acts on two vectors (or two copies of the
same vector) to produce a number. It is therefore very natural to classify tan-
gent vectors according to the sign of their norm. But the interval between two
points isn’t something quite so natural; it depends on a specific choice of path (a
“straight line’) that connects the points, and this choice in turn depends on the
fact that spacetime is flat (which allows a unique choice of straight line between
the points).
Let’s move from the consideration of paths in general to the paths of massive
particles (which will always be timelike). Since the proper time is measured by a
clock traveling on a timelike worldline, it is convenient to use t as the parameter
along the path. That is, we use (1.22) to compute t(A), which (if A is a good
parameter in the first place) we can invert to obtain A(t), after which we can think
of the path as x(t). The tangent vector in this parameterization is known as the
four-velocity, U“:

```
dxl#
ye (1.99)
dt
```
```
Since dt” = —n,,y»dxdx”, the four-velocity is automatically normalized:
```
NuyUMUY = —1, (1.100)

This absolute normalization is a reflection of the fact that the four-velocity is not
a velocity through space, which can of course take on different magnitudes, but a
“velocity through spacetime,” through which one always travels at the same rate.
The norm of the four-velocity will always be negative, since we are only defining
it for timelike trajectories. You could define an analogous vector for spacelike
paths as well; for null paths the proper time vanishes, so t can’t be used as a
parameter, and you have to be more careful. In the rest frame of a particle, its
four-velocity has components U“ = (1, 0, 0, 0).
A related vector is the momentum four-vector, defined by

```
pY =muU?, (1.101)
```

(^32) Chapter 1 Special Relativity and Flat Spacetime
where m is the mass of the particle. The mass is a fixed quantity independent of
inertial frame, what you may be used to thinking of as the “rest mass.” It turns
out to be much more convenient to take this as the mass once and for all, rather
than thinking of mass as depending on velocity. The energy of a particle is sim-
ply E = p®, the timelike component of its momentum vector. Since it’s only
one component of a four-vector, it is not invariant under Lorentz transformations;
that’s to be expected, however, since the energy of a particle at rest is not the
same as that of the same particle in motion. In the particle’s rest frame we have
p° =m; recalling that we have set c = 1, we see that we have found the equation
that made Einstein a celebrity, E = mc?. (The field equation of general relativity
is actually more fundamental than this one, but Ryy — 5Rg uv = 8%GT,y doesn’t
elicit the visceral reaction that you get from E = mc?.) In a moving frame we can
find the components of p“ by performing a Lorentz transformation; for a particle
moving with three-velocity v = dx/dt along the x axis we have
p” = (ym, vym, 0,0), (1.102)
where y = 1/1 — v2. For small v, this gives p? = m + smu? (what we usually
think of as rest energy plus kinetic energy) and p! = mv (what we usually think
of as Newtonian momentum). Outside this approximation, we can simply write
Pup" = —m’, (1.103)
or
E=,/m? +p’, (1.104)
where p? = 6;; p! p/.
The centerpiece of pre-relativity physics is Newton’s Second Law, or f =
ma = dp/dt. An analogous equation should hold in SR, and the requirement
that it be tensorial leads us directly to introduce a force four-vector f“ satisfying
we me x(r) _4 “(r) (1.105)
dr? ~ ar?
The simplest example of a force in Newtonian physics is the force due to gravity.
In relativity, however, gravity is not described by a force, but rather by the cur-
vature of spacetime itself. Instead, let us consider electromagnetism. The three-
dimensional Lorentz force is given by f = g(E + v x B), where q is the charge on
the particle. We would like a tensorial generalization of this equation. There turns
out to be a unique answer:
fl =qu' Fy". (1.106)
You can check for yourself that this reduces to the Newtonian version in the limit
of small velocities. Notice how the requirement that the equation be tensorial,


```
1.9 Energy and Momentum 33
```
which is one way of guaranteeing Lorentz invariance, severely restricts the pos-
sible expressions we can get. This is an example of a very general phenomenon, in
which a small number of an apparently endless variety of possible physical laws
are picked out by the demands of symmetry.
Although p“ provides a complete description of the energy and momentum of
an individual particle, we often need to deal with extended systems comprised of
huge numbers of particles. Rather than specify the individual momentum vectors
of each, particle, we instead describe the system as a fluid—a continuum char-
acterized by macroscopic quantities such as density, pressure, entropy, viscosity,
and so on. Although such a fluid may be composed of many individual particles
with different four-velocities, the fiuid itself has an overall four-velocity field. Just
think of everyday fluids like air or water, where it makes sense to define a velocity
for each individual fiuid element even though nearby molecules may have appre-
ciable relative velocities.
A single momentum four-vector field is insufficient to describe the energy and
momentum of a fluid; we must go further and define the energy-momentum ten-
sor (sometimes called the stress-energy tensor), T“”. This symmetric (2, 0) tensor
tells us all we need to know about the energy-like aspects of a system: energy den-
sity, pressure, stress, and so forth. A general definition of T“” is “the flux of four-
momentum p“ across a surface of constant x”.” In fact, this definition is not going
to be incredibly useful; in Chapter 4 we will define the energy-momentum tensor
in terms of a functional derivative of the action with respect to the metric, which
will be a more algorithmic procedure for finding an explicit expression for T“”.
But the definition here does afford some physical insight. Consider an infinitesi-
mal element of the fluid in its rest frame, where there are no bulk motions. Then
T°, the “flux of p® (energy) in the x9 (time) direction,” is simply the rest-frame
energy density p. Similarly, in this frame, T° = T’° is the momentum density.
The spatial components 7’ are the momentum flux, or the stress; they represent
the forces between neighboring infinitesimal elements of the fluid. Off-diagonal
terms in T‘/ represent shearing terms, such as those due to viscosity. A diagonal
term such as T!! gives the x-component of the force being exerted (per unit area)
by a fluid element in the x-direction; this is what we think of as the x-component
of the pressure, p, (don’t confuse it with the momentum). The pressure has three
components, given in the fluid rest frame (in inertial coordinates) by

p=T". (1.107)

There is no sum over i.
To make this more concrete, let’s start with the simple example of dust. (Cos-
mologists tend to use “matter” as a synonym for dust.) Dust may be defined in
flat spacetime as a collection of particles at rest with respect to each other. The
four-velocity field U“(x) is clearly going to be the constant four-velocity of the
individual particles. Indeed, its components will be the same at each point. Define
the number-flux four-vector to be

NY =nu", (1.108)


34 Chapter 1 Special Relativity and Flat Spacetime

```
where n is the number density of the particles as measured in their rest frame.
(This doesn’t sound coordinate-invariant, but it is; in any frame, the number den-
sity that would be measured if you were in the rest frame is a fixed quantity.)
Then N° is the number density of particles as measured in any other frame, while
N’ is the flux of particles in the x’ direction. Let’s now imagine that each of the
particles has the same mass m. Then in the rest frame the energy density of the
dust is given by
```
```
p=mn. (1.109)
```
```
By definition, the energy density completely specifies the dust. But ¢ only mea-
sures the energy density in the rest frame; what about other frames? We notice
that both n and m are 0-components of four-vectors in their rest frame; specifi-
cally, N“ = (n, 0,0, 0) and p” = (m, 0, 0, 0). Therefore p is the » = 0, v = 0
component of the tensor p ® N as measured in its rest frame. We are therefore
led to define the energy-momentum tensor for dust:
```
Tha = PUN” =mnU"U” = puHU”, (1.110)

```
where p is defined as the energy density in the rest frame. (Typically you don’t
just guess energy-momentum tensors by such a procedure, you derive them from
equations of motion or an action principle.) Note that the pressure of the dust in
any direction is zero; this should not be surprising, since pressure arises from the
random motions of particles within the fluid, and we have defined dust to be free
of such motions.
Dust is not sufficiently general to describe most of the interesting fluids that
appear in general relativity; we only need a slight generalization, however, to ar-
rive at the concept of a perfect fluid. A perfect fluid is one that can be completely
specified by two quantities, the rest-frame energy density p, and an isotropic rest-
frame pressure p. The single parameter p serves to specify the pressure in every
direction. A consequence of isotropy is that 7”” is diagonal in its rest frame—
there is no net flux of any component of momentum in an orthogonal direction.
Furthermore, the nonzero spacelike components must all be equal, 71! = T? =
T>. The only two independent numbers are therefore the energy density p = T°
and the pressure p = T’’; we don’t need a subscript on p, since the pressure is
equal in every direction. The energy-momentum tensor of a perfect fluid therefore
takes the following form in its rest frame:
```
```
p 9 0 0
re ; P. ; (1.111)
0 0 0 p
```
```
(Remember that we are in flat spacetime; this will change when curvature is in-
troduced.) We would like, of course, a formula that is good in any frame. For dust
we had TH” = pU"U”, so we might begin by guessing (9 + p)U“U”, which
```

```
1.9 Energy and Momentum 35
```
```
gives
```
```
Prp^0   0
0 0
0 0 ooo
```
```
+
0
0 (1.112)
0 000
```
This is not a very clever guess, to be honest. But by subtracting this guess from
our desired answer, we see that what we need to add is

```
—-p 0 0 0
0 pO 0
0 0 p 0 (1.113)
0 0 0 p
```
Fortunately, this has an obvious covariant generalization, namely pn“”Thus, the
general form of the energy-momentum tensor for a perfect fluid is

TY” = (p+ p)U"U" + pn”. (1.114)

It may seem that the procedure used to arrive at this formula was somewhat arbi-
trary, but we can have complete confidence in the result. Given that (1.111) should
be the form of T“” in the rest frame, and that (1.114) is a perfectly tensorial ex-
pression that reduces to (1.111) in the rest frame, we know that (1.114) must be
the right expression in any frame.
The concept of a perfect fluid is general enough to describe a wide variety of
physical forms of matter. To determine the evolution of such a fluid, we specify
an equation of state relating the pressure to the energy density, p = p(p). Dust is
a special case for which p = 0, while an isotropic gas of photons has p = 5p. A
more exotic example is vacuum energy, for which the energy-momentum tensor
is proportional to the metric, T“” = —pyacn””. By comparing to (1.114) we find
that vacuum energy is a kind of perfect fluid for which pyac = —Pyac. The notion
of an energy density in vacuum is completely pointless in special relativity, since
in nongravitational physics the absolute value of the energy doesn’t matter, only
the difference in energy between two states. In general relativity, however, all en-
ergy couples to gravity, so the possibility of a nonzero vacuum energy will become
an important consideration, which we will discuss more fully in Chapter 4.
Besides being symmetric, T” has the even more important property of be-
ing conserved. In this context, conservation is expressed as the vanishing of the
“divergence”:

```
a,7%" =0. (1.115)
```
This expression is a set of four equations, one for each value of v. The equation
with v = 0 corresponds to conservation of energy, while a, TH = 0 expresses


36 Chapter 1 Special Relativity and Flat Spacetime

```
conservation of the kth component of the momentum. Let’s apply this equation to
a perfect fluid, for which we have
```
dn, T = du(e + p)UMU” + (p + p)(U" 9,0" + 0" 9,0") +d" p. (1.116)

```
To analyze what this equation means, it is helpful to consider separately what
happens when we project it into pieces along and orthogonal to the four-velocity
field U". We first note that the normalization U,U” = —1 implies the useful
identity
```
U,8,U” = 44,(UyU”) =0. (1.117)

```
To project (1.116) along the four-velocity, simply contract it into Uy:
```
```
Ua, THY = —8,(pU") — pa,U". (1.118)
```
```
Setting this to zero gives the relativistic equation of energy conservation for a
perfect fluid. It will look more familiar in the nonrelativistic limit, in which
```
Uhk=(1,v'), Jul|«l1, p«p. (1.119)

```
The last condition makes sense, because pressure comes from the random motions
of the individual particles, and in this limit these motions (as well as the bulk
motion described by U”) are taken to be small. So in ordinary nonrelativistic
language, (1.118) becomes
```
d;p + V - (pv) =0, (1.120)

```
the continuity equation for the energy density. We next consider the part of (1.116)
that is orthogonal to the four-velocity. To project a vector orthogonal to U", we
multiply it by the projection tensor
```
P°, = 82 +U°Uy. (1.121)

```
To convince yourself this does the trick, check that if we have a vector vi , parallel
to U“, and another vector W/', perpendicular to U“, the projection tensor will
annihilate the parallel vector and preserve the orthogonal one:
```
```
P?,V) =0
P°,Wi = We. (1.122)
```
```
Applied to a,,7"”, we obtain
```
P°d,T = (p + p)U"d,U* + 0° p+ UP U" dy p. (1.123)

```
In the nonrelativistic limit given by (1.119), setting the spatial components of this
expression equal to zero yields
```
```
plav+(v-V)v]+Vp+vaep+v- Vp) =0. (1.124)
```

1.10

```
1.10 Classical Field Theory 37
```
```
But notice that the last set of terms involve derivatives of p times the three-
velocity v, assumed to be small; these will therefore be negligible compared to
the V p term, and can be neglected. We are left with
```
plav+(v-V)v]=—Vp, (1.125)

```
which is the Euler equation familiar from fluid mechanics.
```
```
CLASSICAL FIELD THEORY
```
```
When we make the transition from special relativity to general relativity, the met-
ric Ny Will be promoted to a dynamical tensor field, g,.y(x). GR is thus a par-
ticular example of a classical field theory; we can build up some feeling for how
such theories work by considering classical fields defined on flat spacetime. (We
say classical field theory in contrast with quantum field theory, which is quite a
different story; we will discuss it briefly in Chapter 9, but it is outside our main
area of interest here.)
Let’s begin with the familiar example of the classical mechanics of a single
particle in one dimension with coordinate q(t). We can derive the equations of
motion for such a particle by using the “principle of least action”: we search for
critical points (as a function of the trajectory) of an action 5S, written as
```
s= fata, (1.126)

```
where the function L(q, q) is the Lagrangian. The Lagrangian in point-particle
mechanics is typically of the form
```
L=K~-YV, (1.127)

```
where K is the kinetic energy and V the potential energy. Following the calculus-
of-variations procedure, which is described in any advanced textbook on classical
mechanics, we show that critical points of the action [trajectories q(t) for which
S remains stationary under small variations] are those that satisfy the Euler—
Lagrange equations,
```
```
aL — —~—{——)=0. od f{ aL
(1.128)
aq dt: \ Aq)
```
```
For example, L = 5q° — V(q) leads to
```
```
dV
g= -—. dq (1.129) 1.1
```
```
Field theory is a similar story, except that we replace the single coordinate q(t)
by a set of spacetime-dependent fields, b‘ (x), and the action S becomes a func-
tional of these fields. A functional is simply a function of an infinite number of
```

38 Chapter 1 Special Relativity and Flat Spacetime

```
variables, such as the values of a field in some region of spacetime. Functionals are
often expressed as integrals. Each! is a function on spacetime (at least in some
coordinate system), and i is an index labeling our individual fields. For example,
in electromagnetism (as we will see below) the fields are the four components of
a one-form called the “vector potential,” A,,:
```
®! = (Ao, A, Ad, A3}. (1.130)

```
We’re being very lowbrow here, in thinking of a one-form field as four different
functions rather than a single tensor object. This point of view makes sense so
long as we stick to a fixed coordinate system, and it will make our calculations
more straightforward.
In field theory, the Lagrangian can be expressed as an integral over space of
a Lagrange density C, which is a function of the fields! and their spacetime
derivatives 4,0:
```
L= [as L(®!, 4, 6), (1.131)

```
So the action is
```
s= far = he L(', 4,04). (1.132)

```
The Lagrange density is a Lorentz scalar. We typically just say “Lagrangian”
when we mean “Lagrange density.” It will most often be convenient to define
a field theory by specifying the Lagrange density, from which all of the equations
of motion can be readily derived.
We will use “natural units,” in which not only c = 1 but also f = k = 1, where
h = h/2z, h is Planck’s constant, and k is Boltzmann’s constant. The objection
might be raised that we shouldn’t involve f in a purely classical discussion; but
all we are doing here is choosing units, not determining physics. (The relevance
of A would appear if we were to quantize our field theory and obtain particles, but
we won’t get that far right now.) In natural units we have
```
[energy] = [mass] = [(length)~!] = [(time)~1]. (1.133)

```
We will most often use energy or mass as our fundamental unit. Since the action
is an integral of L (with units of energy) over time, it is dimensionless:
```
[S] = [E][T] = M°. (1.134)

```
The volume element has units
```
[d*x] = M+, (1.135)

```
so to get a dimensionless action we require that the Lagrange density have units
```
[L] = M+. (1.136)


```
1.10 Classical Field Theory 39
```
The Euler-Lagrange equations come from requiring that the action be un-
changed under small variations of the fields,

```
o > o' + 30!, (1.137)
0,0! > a, 0! + (0, 6') = 4,0! + 0, (5). (1.138)
```
The expression for the variation in 3,0! is simply the derivative of the variation
of ®'. Since 5@' is assumed to be small, we may Taylor-expand the Lagrangian
under this variation:

```
L(®', 0,0) > L(@! + 36!, a,b! + 4,50")
aL sai, 06
= £(0', 3,6!) +^ gi TORS^ 3,,(8®'). (1.139)
```
Correspondingly, the action goes to S > § +65, with

```
al
= fas Fae 30,05 "OP >. oe)
```
We would like to factor out 5! from the integrand, by integrating the second
term by parts:

```
fas of ~3,(8®') = — f as 3. ( of — | so!
3(3,, 8!) 3(8,, 0!)
```
+a^4 x Ou (saan®® aL i ). (1.141)

The final term is a total derivative—the integral of something of the form a,,V“”—
that can be converted to a surface term by Stokes’s theorem (the four-dimensional
version, that is; see Appendix E for a discussion). Since we are considering vari-
ational problems, we can choose to consider variations that vanish at the bound-
ary (along with their derivatives). It is therefore traditional in such contexts to
integrate by parts with complete impunity, always ignoring the boundary contri-
butions. (Sometimes this is not okay, as in instanton calculations in Yang—Mills
theory.)
We are therefore left with

ss= — | fg, | a^24 x E _ Oy (aces o£ 50! (1.142)

The functional derivative 55/5! of a functional S with respect to a function &!
is defined to satisfy

```
5S.
a= f ats 50 (1.143)
```

40 Chapter 1 Special Relativity and Flat Spacetime

```
when such an expression is valid. We can therefore express the notion that S is at a
critical point by saying that the functional derivative vanishes. The final equations
of motion for our field theory are thus:
```
```
iS 2k yg 0k) 9 1.144
soi adi Naa, bI) J (1.144)
```
```
These are known as the Euler-Lagrange equations for a field theory in flat space-
time.
The simplest example of a field is a real scalar field:
```
```
¢(x") : (spacetime) > R. (1.145)
```
```
Slightly more complicated examples would include complex scalar fields, or maps
from spacetime to any vector space or even any manifold (sometimes called “non-
linear sigma models”). Upon quantization, excitations of the field are observable
as particles. Scalar fields give rise to spinless particles, while vector fields and
other tensors give rise to higher-spin particles. If the field were complex instead
of real, it would have two degrees of freedom rather than just one, which would
be interpreted as a particle and a distinct antiparticle. Real fields are their own
antiparticles. An example of a real scalar field would be the neutral 7-meson.
So let’s consider the classical mechanics of a single real scalar field. It will
have an energy density that is a local function of spacetime, and includes various
contributions:
```
```
kinetic energy : 5°
gradient energy : (Vo)? (1.146)
potential energy : V@).
```
```
Actually, although the potential is a Lorentz-invariant function, the kinetic and
gradient energies are not by themselves Lorentz-invariant; but we can combine
them into a manifestly Lorentz-invariant form:
```
—4n” (ub) (Av) = $67 — 4(V9)?. (1.147)

```
[The combination n“” (d,.6) (dy) is often abbreviated as (8@)*.] So a reasonable
choice of Lagrangian for our single real scalar field, analogous to L = K — V in
the point-particle case, would be
```
L= —Zn"(8.6)(8,¢) — VO). (1.148)

```
This generalizes “kinetic minus potential energy” to “kinetic minus gradient mi-
nus potential energy density.’ Note that since [£] = M*, we must have [V] =_
M+‘. Also, since [8,,] = [3/8x“] = M1, we have
```
[¢] = mM’. (1.149)


```
1.10 Classical Field Theory 41
```
```
For the Lagrangian (1.148) we have
```
```
oe aL dV dV aL
= =n a,d. 1.150
```
###### a6 dé’ 30,0” (1.190)

The second of these equations is a little tricky, so let’s go through it slowly. When
differentiating the Lagrangian, the trick is to make sure that the index placement
is “compatible” (so that if you have a lower index on the thing being differen-
tiated with respect to, you should have only lower indices when the same kind
of object appears in the thing being differentiated), and also that the indices are
strictly different. The first of these is already satisfied in our example, since we
are differentiating a function of d,, with respect to 0,,@. Later on, we will need
to be more careful. To fulfill the second, we simply relabel dummy indices:

nt” (8n6)(Ov) = n°? (8o9) Oc). (1.151)

Then we can use the general rule, for any object with one index such as Y,,, that

```
aV.
— = 88 (1.152)
dVg
```
because each component of Vy is treated as a distinct variable. So we have

###### Fag) (1? ob)(0e)] = 0" [8p Bo) + (8o)8E

= nY? (8g 6) + n°" (8pd) = 2n*d,¢. (1.153)

This leads to the second expression in (1.150).
Putting (1.150) into (1.144) leads to the equation of motion

```
dV
O¢-—=0, p dé ( 1.154 )
```
where 0 = n“’0,,0y is known as the d’Alembertian. Note that our metric sign
convention (—+++) comes into this equation; with the alternative (+———) con-
vention the sign would have been switched. In flat spacetime (1.154) is equivalent
to

```
“ dV
```
##### d- V+ —-V’o+—=0. 7 (1.155) 1.155

A popular choice for the potential V is that of a simple harmonic oscillator,
V(@) = 3m*¢?. The parameter m is called the mass of the field, and you should
notice that the units work out correctly. You may be wondering how a field can
have mass. When we quantize the field we find that momentum eigenstates are
collections of particles, each with mass m. At the classical level, we think of
“mass” as simply a convenient characterization of the field dynamics. Then our


(^42) Chapter 1 Special Relativity and Flat Spacetime
equation of motion is
Og —mo =0, (1.156)
the famous Klein—Gordon equation. This is a linear differential equation, so the
sum of two solutions is a solution; a complete set of solutions (in the form of
plane waves) is easy to find, as you can check for yourself.
A slightly more elaborate example of a field theory is provided by electro-
magnetism. We mentioned that the relevant field is the vector potential A,,; the
timelike component Ao can be identified with the electrostatic potential ®, and the
spacelike components with the traditional vector potential A (in terms of which
the magnetic field is given by B = V x A). The field strength tensor, with com-
ponents given by (1.69), is related to the vector potential by
Fuv = OyAy — dy Ap. (1.157)
From this definition we see that the field strength tensor has the important property
of gauge invariance: when we perform a gauge transformation on the vector
potential,
Ap > Ap + 0,A(x), (1.158)
the field strength tensor is left unchanged:
Fuy > Fuv + Oy 0yA — Oy0,% = Fyy. (1.159)
The last equality follows from the fact that partial derivatives commute, 0,0) =
d,0,,. Gauge invariance is a symmetry that is fundamental to our understanding
of electromagnetism, and all observable quantities must be gauge-invariant. Thus,
while the dynamical field of the theory (with respect to which we vary the action to
derive equations of motion) is A,,, physical quantities will generally be expressed
in terms of Fyy.
We already know that the dynamical equations of electromagnetism are
Maxwell’s equations, (1.96) and (1.97). Given the definition of the field stregth
tensor in terms of the vector potential, (1.97) is actually automatic:
Ou ve] = Indy Ac] — Oyo Av] = 0, (1.160)
again because partial derivatives commute. On the other hand, (1.96) is equivalent
to Euler-Lagrange equations of the form
al -~9 al
= 0, 1.161
aA, © (saa) C16)
if we presciently choose the Lagrangian to be
L=—qPw FY + Ay". (1.162)


```
1.10 Classical Field Theory 43
```
```
For this choice, the first term in the Euler-Lagrange equation is straightforward:
```
```
al
dAy
```
(^) =o Jha J’. (1.163)
The second term is tricker. First we write F,,,F“” as
Fyy FY’ = FopF°? = % n°? Fup Foa- (1.164)
We want to work with lower indices on F,,,, since we are differentiating with re-
spect to 0,,Ay, which has lower indices. Likewise we change the dummy indices
on FF”, since we want to have different indices on the thing being differen-
tiated and the thing we are differentiating with respect to. Once you get familiar
with this stuff it will become second nature and you won’t need nearly so many
steps. This lets us write
aFapF?) _ ap, po [^0 Fug )
( OF og )]
0(0, Av) =n) 3(0,,Ay) Foo + Fup 3(0,A,)
(^). (1.165)
Then, since Fyg = dy Ag — 06 Aq, we have
0 Fog
PF = gg? — gg. 1.166
a(a,Ay) * P Bm ( )
Combining (1.166) with (1.165) yields
0 (Fog NGA FP. = nr? Po [(oue53 — 5550) Foo + (6452 _ 455) Fag |
pAav
= (nn ?? _ on?) Fog^4 (q% B® _ ne’ nP") Fup
= FHY— Fee + FRY — BYR
= 4FM (1.167)
SO
aL
A(OpAv)
(^) _ FH. (1.168)
Then sticking (1.163) and (1.168) into (1.161) yields precisely (1.96):
0,F* = J”. (1.169)
Note that we switched the order of the indices on F#” in order to save ourselves
from an unpleasant minus sign.
You may wonder what the purpose of introducing a Lagrangian formulation
is, if we were able to invent the equations of motion before we ever knew the
Lagrangian (as Maxwell did for his equations). There are a number of reasons,


(^44) Chapter 1 Special Relativity and Flat Spacetime
starting with the basic simplicity of positing a single scalar function of spacetime,
the Lagrange density, rather than a number of (perhaps tensor-valued) equations
of motion. Another reason is the ease with which symmetries are implemented;
demanding that the action be invariant under a symmetry ensures that the dynam-
ics respects the symmetry as well. Finally, as we will see in Chapter 4, the action
leads via a direct procedure (involving varying with respect to the metric itself)
to a unique energy-momentum tensor. Applying this procedure to (1.148) leads
straight to the energy-momentum tensor for a scalar field theory,

#### Tatar = 19" 0.9800 — 1!” [dy A.dao6 + V(6)]- 170)

```
Similarly, from (1.162) we can derive the energy-momentum tensor for electro-
magnetism,
```
Toy = FMF’) — gn Fé Fig. (1.17)

```
Using the appropriate equations of motion, you can show that these energy-
momentum tensors are conserved, 0,,T #Y” — Q (and will be asked to do so in the
Exercises).
The two examples we have considered—scalar field theory and electro-
magnetism—are paradigms for much of our current understanding of nature. The
Standard Model of particle physics consists of three types of fields: gauge fields,
Higgs fields, and fermions. The gauge fields describe the “forces” of nature, in-
cluding the strong and weak nuclear forces in addition to electromagnetism. The
gauge fields giving rise to the nuclear forces are described by one-form poten-
tials, just as in electromagnetism; the difference is that they are matrix-valued
rather than ordinary one-forms, and the symmetry groups corresponding to gauge
transformations are therefore noncommutative (nonabelian) symmetries. The
Higgs fields are scalar fields much as we have described, although they are also
matrix-valued. The fermions include leptons (such as electrons and neutrinos)
and quarks, and are not described by any of the tensor fields we have discussed
here, but rather by a different kind of field called a spinor. We won’t get around
to discussing spinors in this book, but they play a crucial role in particle physics
and their coupling to gravity is interesting and subtle. Upon quantization, these
fields give rise to particles of different spins; gauge fields are spin-1, scalar fields
are spin-0, and the Standard Model fermions are spin-5.
Before concluding this chapter, let’s ask an embarassingly simple question:
Why should we consider one classical field theory rather than some other one?
More concretely, let’s say that we have discovered some particle in nature, and
we know what kind of field we want to use to describe it; how should we pick
the Lagrangian for this field? For example, when we wrote down our scalar-field
Lagrangian (1.148), why didn’t we include a term of the form
```
L! =o" n” (8.6) (Ord), (1.172)


```
1.11. Exercises 45
```
```
where A is a coupling constant? Ultimately, of course, we work by trial and error
and try to fit the data given to us by experiment. In classical field theory, there’s
not much more we could do; generally we would start with a simple Lagrangian,
and perhaps make it more complicated if the first try failed to agree with the data.
But quantum field theory actually provides some simple guidelines, and since we
use Classical field theory as an approximation to some underlying quantum the-
ory, it makes sense to take advantage of these principles. To make a long story
short, quantum field theory allows “virtual” processes at arbitrarily high energies
to contribute to what we observe at low energies. Fortunately, the effect of these
processes can be summarized in a low-energy effective field theory. In the effec-
tive theory, which is what we actually observe, the result of high-energy processes
is simply to “renormalize” the coupling constants of our theory. Consider an arbi-
trary coupling constant, which we can express as a parameter jz (with dimensions
of mass) raised to some power, A = y22 (unless A is dimensionless, in which case
the discussion becomes more subtle). Very roughly speaking, the effect of high-
energy processes will be to make tt very large. Slightly more specifically, w will
be pushed up to a scale at which new physics kicks in, whatever that may be.
Therefore, potential higher-order terms we might think of adding to a Lagrangian
are suppressed, because they are multiplied by coupling constants that are very
small. For (1.172), for example, we must have A = 44”, so A will be tiny (be-
cause yz will be big). Only the lowest-order terms we can put in our Lagrangian
will come with dimensionless couplings (or ones with units of mass to a positive
power), so we only need bother with those at low energies. This feature of field
theory allows for a dramatic simplification in considering all of the models we
might want to examine.
As mentioned at the beginning of this section, general relativity itself is a clas-
sical field theory, in which the dynamical field is the metric tensor. It is neverthe-
less fair to think of GR as somehow different; for the most part other classical
field theories rely on the existence of a pre-existing spacetime geometry, whereas
in GR the geometry is determined by the equations of motion. (There are excep-
tions to this idea, called topological field theories, in which the metric makes no
appearance.) Our task in the next few chapters is to explore the nature of curved
geometries as characterized by the spacetime metric, before moving in Chapter 4
to putting these notions to work in constructing a theory of gravitation.
```
1.11 ME EXERCISES

1. Consider an inertial frame S with coordinates x“ = (t,x, y,z), and a frame S’ with
    coordinates x’ related to S by a boost with velocity parameter v along the y-axis.
    Imagine we have a wall at rest in S’, lying along the line x’ = —y’. From the point of
    view of 5, what is the relationship between the incident angle of a ball hitting the mirror
       (traveling in the x-y plane) and the reflected angle? What about the velocity before and
       after?


