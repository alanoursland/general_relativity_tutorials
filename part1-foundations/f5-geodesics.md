# Geodesics: How Things Move

> **Tutorial `F5`** · Part 1 · **Goal:** the geodesic equation, conserved quantities from symmetry, and the effective-potential picture for orbits — the machinery [`PPN4`](../part6-ppn-observation/ppn4-classical-tests.md)/[`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md) need for perihelion precession. · **Prereqs:** [F1](./f1-metric.md), [F2](./f2-tensors.md), [F3](./f3-special-relativity.md), [F4](./f4-curvilinear-coordinates.md).

**Where this sits in the arc.** Perihelion precession is the observational selector that actually works ([`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md)) — it is what distinguishes members of the $A_\lambda$ family once redshift and light-bending have failed to. Everything that calculation needs — a conserved energy, a conserved angular momentum, and an effective potential in $r$ — is built here, in full generality, before any specific metric is chosen.

## Geodesics: the "straightest possible" worldline

A **geodesic** is the worldline a freely falling particle follows — no rockets, no non-gravitational forces. Among all timelike worldlines connecting two fixed events, the geodesic is the one that *extremizes* (in fact, locally maximizes) the accumulated proper time $\int d\tau$ — the direct generalization of "straight line" to curved spacetime, and exactly what [`F3`](./f3-special-relativity.md) noted about inertial worldlines in flat spacetime. Extremizing that integral via the calculus of variations produces the **geodesic equation**,

$$\frac{d^2x^\mu}{d\tau^2} + \Gamma^\mu_{\alpha\beta}\,\frac{dx^\alpha}{d\tau}\frac{dx^\beta}{d\tau} = 0,$$

where the **Christoffel symbols** $\Gamma^\mu_{\alpha\beta}$ are built from derivatives of the metric $g_{\mu\nu}$. You will not need to compute a Christoffel symbol by hand anywhere in this book; the only thing worth knowing about them conceptually is that they encode how the coordinate grid itself twists and stretches from point to point (they vanish in special locally-flat coordinates at any single point, which is why they are not themselves tensors) — the actual, coordinate-independent curvature is captured only by the object built from their derivatives, the Riemann tensor ([`F7`](./f7-curvature.md)).

## The practical shortcut: symmetry gives conservation laws

Rather than grinding through Christoffel symbols directly, this book uses a shortcut available whenever the metric has a symmetry — a shortcut that is the geodesic-equation analogue of Noether's theorem: **every direction the metric does not depend on gives a conserved quantity along geodesics.** Concretely, geodesics extremize the Lagrangian-like quantity

$$\mathcal{L} = g_{\mu\nu}\dot x^\mu \dot x^\nu, \qquad \dot{} \equiv \frac{d}{d\tau},$$

and if $g_{\mu\nu}$ does not depend on some coordinate $x^\sigma$, then $x^\sigma$ is a **cyclic coordinate** in the ordinary Lagrangian-mechanics sense, and its conjugate momentum $\partial\mathcal{L}/\partial\dot x^\sigma$ is conserved along the geodesic. This is precisely "invariance under shifting $x^\sigma$ implies a conserved quantity," transplanted from ordinary mechanics — no new machinery beyond what a CS-trained reader will recognize from any first course touching Lagrangian dynamics or symmetry arguments in general.

## Applying this to a static, spherically symmetric metric

Take the general ansatz from [`SYM1`](./sym1-static-spherical.md), restricted (by spherical symmetry, without loss of generality) to the equatorial plane $\theta=\pi/2$:

$$ds^2 = -A(r)c^2dt^2 + B(r)dr^2 + r^2 d\phi^2.$$

This metric does not depend on $t$ (**static**) or on $\phi$ (**spherically symmetric**, so nothing distinguishes one azimuthal direction from another) — only on $r$. By the shortcut above, this hands us two conserved quantities along any geodesic, conventionally normalized per unit mass as an energy $E$ and an angular momentum $\ell$:

$$E \equiv A(r)c^2\,\dot t, \qquad \ell \equiv r^2\,\dot\phi.$$

$E$ is conserved because the metric is time-independent (time-translation symmetry); $\ell$ is conserved because the metric is $\phi$-independent (rotational symmetry about the polar axis) — the exact geodesic-equation analogue of energy and angular-momentum conservation in ordinary orbital mechanics.

## The orbit equation and effective potential

For a timelike worldline parameterized by proper time, the line element itself supplies a third relation — the **normalization condition** $ds^2 = -c^2 d\tau^2$, i.e. $g_{\mu\nu}\dot x^\mu\dot x^\nu = -c^2$:

$$-A(r)c^2\dot t^2 + B(r)\dot r^2 + r^2\dot\phi^2 = -c^2.$$

Substitute $\dot t = E/(A c^2)$ and $\dot\phi = \ell/r^2$ from above:

$$-A c^2 \cdot \frac{E^2}{A^2c^4} + B\dot r^2 + r^2\cdot\frac{\ell^2}{r^4} = -c^2 \quad\Longrightarrow\quad -\frac{E^2}{Ac^2} + B\dot r^2 + \frac{\ell^2}{r^2} = -c^2.$$

Solving for $\dot r^2$:

$$\boxed{\dot r^2 = \frac{1}{B(r)}\left[\frac{E^2}{A(r)\,c^2} - c^2 - \frac{\ell^2}{r^2}\right].}$$

This is a purely radial "energy equation": once $E$ and $\ell$ are fixed by initial conditions, the whole orbit — including whether $r$ oscillates between a minimum and maximum (a bound orbit) — is governed by this single equation in $r$ alone, exactly as in the ordinary $\tfrac12\dot r^2 + V_{\rm eff}(r) = \text{const}$ picture of central-force orbits, just with $A(r)$ and $B(r)$ dressing the Newtonian terms. The term $-\ell^2/r^2$ is the familiar centrifugal (angular-momentum) barrier; the $E^2/(Ac^2)$ term plays the role of total energy, redistributed by the metric's time coefficient $A(r)$.

This is the general shape every later orbit calculation specializes: in the Newtonian limit ($A\approx1+2\Phi/c^2$, small $\ell$-terms), it reduces to the familiar effective potential $V_{\rm eff}(r) = \Phi(r) + \ell^2/(2r^2)$ that gives closed, non-precessing ellipses. Once $A(r)$ carries genuine relativistic corrections (as every member of the $A_\lambda$ family does beyond leading order — [`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)), the $1/A(r)$ factor introduces extra $r$-dependence beyond the Newtonian terms, an effect that does **not** preserve closed orbits — this is exactly the seed of the perihelion precession calculation carried out in full in [`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md), and why precession, unlike redshift or light bending, is sensitive enough to see the difference between family members.

## Simpler on-ramp

Picture a ball rolling on a hilly track shaped by an effective potential in one variable, $r$ — exactly like a marble in a bowl-shaped valley whose walls are set by gravity plus a "centrifugal" term from spinning around the center. Total energy is fixed at launch; the marble oscillates between two turning points where its radial speed drops to zero, exactly like a planet's orbit oscillating between perihelion and aphelion. In ordinary Newtonian gravity, the valley's shape gives orbits that retrace exactly the same ellipse forever — no drift. Relativistic corrections warp the valley's shape ever so slightly with extra $r$-dependence, so the orbit doesn't quite close after one revolution: the point of closest approach itself slowly rotates. That rotation is precession, and how much it happens depends sensitively on the exact shape of the warp — which is exactly what distinguishes one member of the metric family from another.

## Check your understanding

1. Why does a metric's independence from $t$ produce a conserved "energy," and independence from $\phi$ produce a conserved "angular momentum"?
2. What does the normalization condition $g_{\mu\nu}\dot x^\mu\dot x^\nu=-c^2$ physically encode, and why is it available in addition to the two conserved quantities?
3. In the orbit equation derived above, which term plays the role of the ordinary "centrifugal barrier," and does its form change depending on $A(r)$?
4. Why is perihelion precession a more sensitive probe of the metric's exact shape than, say, gravitational redshift?

<details>
<summary>Answers</summary>

- **1.** This is the geodesic-equation analogue of Noether's theorem: a symmetry (invariance of the metric/Lagrangian under shifting a coordinate) always produces a conserved quantity conjugate to that coordinate — time-translation symmetry gives conserved energy, rotational symmetry about the axis gives conserved angular momentum.
- **2.** It encodes that the worldline is timelike and parameterized by its own proper time (equivalently, $ds^2=-c^2d\tau^2$ along it) — a geometric constraint from the metric itself, independent of and in addition to the two conservation laws from symmetry, giving exactly enough equations to solve for the orbit.
- **3.** The $-\ell^2/r^2$ term (multiplied by $1/B$). Its basic $1/r^2$ shape doesn't change, but it is dressed by the metric functions $A(r)$, $B(r)$, and the way $E^2$ enters through $1/A(r)$ introduces $r$-dependence beyond the Newtonian centrifugal term, which is exactly what breaks orbit closure.
- **4.** Redshift only sees the metric's leading, Newtonian-order behavior (shared by every family member, [`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)), while precession accumulates a small effect from the metric's exact nonlinear shape over many orbits, making it sensitive to exactly the higher-order terms that distinguish one family member from another.

</details>

## What the paper claims here

This tutorial is prerequisite machinery, not a direct claim of the source paper — the paper itself invokes the standard PPN perihelion-precession result (§5.3, factor $\tfrac{2+2\gamma-\beta}{3}$) without re-deriving geodesics from scratch. This tutorial supplies exactly the background needed to understand where that formula comes from and why precession, specifically, is the classical test sensitive to $\beta$ (and hence to $\lambda$) rather than to $\gamma$ alone.

---
**Path navigation:** ← [prev in default path](./f4-curvilinear-coordinates.md) · [next: F6 — The Newtonian limit](./f6-newtonian-limit.md) →
**See also:** [PPN4](../part6-ppn-observation/ppn4-classical-tests.md), [PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md), [S3](../part2-schwarzschild/s3-properties.md)
