# Glossary

Concise definitions of the recurring terms, each faithful to the source paper
and linked to the tutorial that treats it in full.

**Areal radius.** The radial coordinate $r$ defined so that a sphere at fixed
$r$ has surface area exactly $4\pi r^2$ — it is a definition by *area*, not by
any notion of distance from the center, and the two can diverge once space is
curved. The paper's flux law (I2) is written in this coordinate, which is why it
is a coordinate-dependent postulate rather than a covariant equation. See
[`F4`](../part1-foundations/f4-curvilinear-coordinates.md).

**Isotropic coordinates.** A radial coordinate $\rho$ in which the spatial part
of a static spherical metric is conformally flat, $\Psi^2(\rho)(d\rho^2+\rho^2d\Omega^2)$,
so that space "looks Euclidean up to an overall scale factor." The standard PPN
metric is written in isotropic form, so comparing $A_\lambda$ (given in areal
coordinates) to $\gamma$ and $\beta$ requires the second-order transformation
$r=\rho(1+k_1w+k_2w^2)$. See [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md).

**Painlevé–Gullstrand (PG) coordinates.** A time coordinate $T$, related to
Schwarzschild-family time $t$ by $dt=dT-\frac{\sqrt{1-A}}{cA}dr$, chosen so that
constant-$T$ spatial slices are flat Euclidean space and all the gravitational
content sits in a mixed term $2v\,dr\,dT$, with river velocity $v(r)=c\sqrt{1-A(r)}$.
$v$ is a coordinate shift, not a material flow. See
[`PG1`](../part7-michell-pg/pg1-painleve-gullstrand.md).

**Asymptotic flatness.** The boundary condition $A,B\to1$ as $r\to\infty$: far
from the source, spacetime looks like flat Minkowski space. It fixes the
integration constant $C_0=1$ when solving the family's closure equation. See
[`SYM1`](../part1-foundations/sym1-static-spherical.md) and
[`CORE4`](../part3-building-the-family/core4-classification-theorem.md).

**Horizon.** A boundary beyond which nothing, not even outgoing light, can
escape. The book insists on the invariant PG criterion — outgoing light frozen,
$dr/dT=c-v=0$, i.e. $v=c$ — rather than merely a zero of $g_{tt}$; only
Schwarzschild ($\lambda=-1$) is established to have a genuine horizon at its
zero $r_s$. See [`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md) and
[`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md).

**Coordinate singularity vs. curvature singularity.** A coordinate singularity
is a place where a chosen chart misbehaves even though the underlying geometry
is smooth (Schwarzschild's $r=r_s$: curvature invariants stay finite there). A
curvature singularity is a place where an invariant (coordinate-independent)
quantity actually diverges (Schwarzschild's $r=0$). The rule: never call a zero
of $g_{tt}$ a horizon, or a coordinate blow-up a singularity, without checking
an invariant. See [`S4`](../part2-schwarzschild/s4-singularities.md).

**Kretschmann scalar.** The curvature invariant $R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}$,
built entirely from the Riemann tensor and hence coordinate-independent. It is
finite at Schwarzschild's $r_s$ and diverges at $r=0$, which is exactly the
test that separates a coordinate artifact from a real singularity. See
[`F7`](../part1-foundations/f7-curvature.md).

**Newtonian limit.** The weak-field, low-velocity regime in which
$-g_{tt}\approx1+2\Phi/c^2$ with $\Phi=-GM/r$; assumption (I1) of the family's
construction. It fixes the mass scale $r_s=2GM/c^2$ and the metric's leading
term but says nothing about the nonlinear (higher-order) terms — which is
exactly the freedom $\lambda$ parameterizes. See
[`F6`](../part1-foundations/f6-newtonian-limit.md).

**Weak field / post-Newtonian.** An expansion of the metric in powers of
$x=r_s/r$ (equivalently the potential $U=GM/(c^2\rho)$) beyond the leading
Newtonian term. All family members agree through $O(x)$; they first differ at
$O(x^2)$, with coefficient $(1+\lambda)/2$ — vanishing exactly at Schwarzschild.
See [`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md).

**PPN parameters $\gamma$ and $\beta$.** The two numbers of the parametrized
post-Newtonian formalism that summarize a metric's leading departures from flat
space: $\gamma$ is the amount of spatial curvature per unit potential (light
bending, Shapiro delay); $\beta$ is the nonlinearity of the time–time metric
component at $O(U^2)$ (perihelion precession). General relativity predicts
$\gamma=\beta=1$; for the family, $\gamma=1$ for every $\lambda$ while
$\beta=\lambda+2$, so $\beta$ alone carries the information $\gamma$ cannot.
See [`PPN1`](../part6-ppn-observation/ppn1-ppn-formalism.md) and
[`PPN3`](../part6-ppn-observation/ppn3-gamma-beta.md).

**Perihelion precession.** The advance, per orbit, of a planet's point of
closest approach beyond the Newtonian prediction. Its leading anomalous rate is
proportional to $\frac{2+2\gamma-\beta}{3}$; because the family has $\gamma=1$
always, this reduces to $\frac{2-\lambda}{3}$, making precession the one
classical test sensitive to $\lambda$ (redshift and light bending are blind to
it). Mercury's observed 43″/century selects $\lambda=-1$. See
[`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md).

**Gauss's law / flux law.** The statement that the flux of a $1/r^2$ field
through a sphere is constant, equivalently that a suitable potential variable
$V$ obeys $\Delta V=0$ with $\Delta=\frac1{r^2}\frac{d}{dr}\!\left(r^2\frac{d}{dr}\right)$
in *areal* coordinates. Assumption (I2) demands this hold exactly for *some*
monotonic $V(A)$ — but not which one, which is the freedom the family exploits.
This flux law is a postulate, not a consequence of the Einstein equations. See
[`GAUSS1`](../part1-foundations/gauss1-flux-laplacian.md) and
[`CORE1`](../part3-building-the-family/core1-flux-freedom.md).

**Laplace–Beltrami operator.** The genuine, metric-dependent generalization of
the Laplacian to a curved space (or spacetime slice). The book is explicit that
its flux operator $\Delta$ is *not* this object — it is the flat-space radial
operator applied to areal $r$ — and that conflating the two is exactly the kind
of category error the paper's restraint is built to avoid. See
[`GAUSS1`](../part1-foundations/gauss1-flux-laplacian.md).

**Self-energy / binding energy.** The (negative) energy released in quasi-statically
assembling a mass distribution from dispersed pieces at infinity; in the two-shell
calculation, the interaction piece is the convention-independent
$E_{\rm int}=-U=-Gm_1m_2/b$. How that total energy splits between "matter" and
"field" contributions is a localization choice, not a further physical fact.
See [`ENE1`](../part1-foundations/ene1-self-energy.md) and
[`ACC2`](../part5-energy-accounting/acc2-invariant-assembly-energy.md).

**Pseudotensor.** A quantity used in general relativity to try to assign
gravitational field energy a local density, which fails to transform as a true
tensor under general coordinate changes — a symptom of the fact that
gravitational energy has no coordinate-independent local address, only a
well-defined total in suitable circumstances. See
[`ACC6`](../part5-energy-accounting/acc6-energy-localization.md).

**Quasi-local energy.** Constructions (Komar, ADM, Bondi, and others) that
assign an energy to a finite region or its boundary rather than to a point,
partially working around the pseudotensor problem for well-behaved regions and
asymptotic limits; noted here as further reading rather than computed. See
[`ACC6`](../part5-energy-accounting/acc6-energy-localization.md).

**Nordtvedt effect.** A predicted violation of the strong equivalence principle
in which a body's gravitational self-energy might fall differently than its
other mass-energy, tested by lunar laser ranging (Nordtvedt 1968; Williams,
Turyshev & Boggs 2004). It supplies the physical motivation for asking, in
Part V, whether gravitational binding energy "gravitates universally" — the
question that turns out not to fix $\lambda$ by itself. See
[`ACC0`](../part5-energy-accounting/acc0-the-question.md).

**Birkhoff's theorem.** The genuine GR uniqueness result: static, spherically
symmetric, *vacuum-Einstein* ($G_{\mu\nu}=0$) exteriors are Schwarzschild,
uniquely — no family. The paper's family does not contradict this theorem
because it replaces the vacuum Einstein equations with a strictly weaker
postulate (the areal flux law); dropping that one hypothesis is exactly what
reopens the solution set. See
[`BIRK`](../part2-schwarzschild/birkhoff.md).

**The family $A_\lambda$.** The one-parameter family of metric coefficients
$$A_\lambda(r) = \left(1+\lambda\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda=A_\lambda^{-1},$$
that is the complete solution set of assumptions (I1)–(I4), with Schwarzschild
recovered at $\lambda=-1$ and the $\lambda\to0$ limit giving $A_0=e^{-r_s/r}$ by
continuity. See
[`CORE4`](../part3-building-the-family/core4-classification-theorem.md).

**The parameter $\lambda$.** The constant nonlinear-coefficient of assumption
(I4): $-F''(s)/F'(s)=\lambda$, equivalently the coefficient in
$\Delta s=\lambda(s')^2$, where $s=\ln A$. It is mathematically the property of
*which variable was chosen to make the flux law exact* — a closure/representation
choice, not initially a fact about the geometry. It reappears as the PPN
nonlinearity $\beta=\lambda+2$, as the sign controlling whether $A_\lambda$ has
a finite-radius zero, and as the condition ($\lambda=-1$) under which the PG
infall velocity matches the Newtonian profile exactly. See
[`CORE2`](../part3-building-the-family/core2-log-variable-closure.md).
