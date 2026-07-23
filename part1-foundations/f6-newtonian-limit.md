# The Newtonian Limit

> **Tutorial `F6`** · Part 1 · **Goal:** derive how $-g_{tt}\approx1+2\Phi/c^2$ emerges from matching geodesic motion to Newton's law, why $\Phi=-GM/r$ fixes the leading term of $A(r)$, and the mass scale $r_s=2GM/c^2$. · **Prereqs:** [F1](./f1-metric.md), [F3](./f3-special-relativity.md), [F5](./f5-geodesics.md).

**Where this sits in the arc.** This tutorial *is* assumption (I1) from [`CORE0`](../part3-building-the-family/core0-four-assumptions.md) — the first of the four ingredients that build the whole $A_\lambda$ family. It fixes the mass scale $r_s$ and the leading behavior of $A(r)$ shared by *every* member of the family, and it is exactly the reason the family's members cannot be told apart by their weakest-field behavior alone ([`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)).

## The question

For a metric to describe gravity around an ordinary mass $M$ — the Sun, say — it had better reduce, far away and for slowly moving test particles, to plain Newtonian gravity: $F=-\nabla\Phi$ per unit mass, with $\Phi=-GM/r$. What does that requirement force onto the metric function $A(r)$ in $ds^2=-A(r)c^2dt^2+B(r)dr^2+r^2d\Omega^2$ ([`SYM1`](./sym1-static-spherical.md))?

## Slow motion, weak field: the geodesic equation collapses

Take a test particle moving slowly ($v\ll c$) in a weak, static field, so $A(r) = 1+\epsilon(r)$ for some small correction $\epsilon$, and to the needed order the spatial metric can be treated as flat (spatial curvature corrections affect light bending and precession, [`PPN4`](../part6-ppn-observation/ppn4-classical-tests.md), but not the leading Newtonian force law — this asymmetry, why $A$ alone governs Newtonian dynamics while $B$ only shows up at higher order, is exactly why $\gamma$ turns out to be invisible to purely Newtonian-limit reasoning). For such a particle, $dt/d\tau\approx1$ and spatial velocities are small, so the spatial components of the geodesic equation ([`F5`](./f5-geodesics.md)) reduce (dropping terms of order $v^2/c^2$ and higher) to

$$\frac{d^2x^i}{dt^2} \approx -\frac{c^2}{2}\,\partial_i A.$$

This is a standard, if slightly technical, weak-field reduction of the full geodesic equation — the key content to take away is simply that in this limit, the particle's ordinary coordinate acceleration is set by the gradient of $A$, scaled by $c^2/2$. Comparing directly to Newton's second law per unit mass, $d^2x^i/dt^2 = -\partial_i\Phi$, forces

$$A(r) = 1 + \frac{2\Phi(r)}{c^2} + O\!\left(\frac{\Phi^2}{c^4}\right).$$

This is the entire content of (I1): **consistency with Newtonian gravity, in the weak-field slow-motion limit, requires the time coefficient of the metric to take exactly this form**, with $\Phi$ identified as the ordinary Newtonian potential.

## Fixing $\Phi$ and the mass scale $r_s$

For a spherical mass $M$ (with the shell theorem justifying that only the total enclosed mass matters outside the source, [`ENE1`](./ene1-self-energy.md)/[`GAUSS1`](./gauss1-flux-laplacian.md)), the Newtonian potential is $\Phi(r) = -GM/r$. Substituting:

$$A(r) = 1 - \frac{2GM}{rc^2} + O(r^{-2}).$$

Define the length scale

$$r_s \equiv \frac{2GM}{c^2},$$

and the dimensionless ratio $x \equiv r_s/r$ (small, and hence a natural expansion parameter, whenever $r\gg r_s$). Then

$$\boxed{A(r) = 1 - x + O(x^2).}$$

This single boxed relation is the anchor for the entire family built later: **every** member $A_\lambda(r) = (1+\lambda r_s/r)^{-1/\lambda}$ ([`CORE4`](../part3-building-the-family/core4-classification-theorem.md)) is required, by construction, to reduce to exactly this leading form — which is precisely why the leading-order behavior alone can never distinguish members ([`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)).

## What this does — and does not — fix

Be precise about the scope, matching the paper's own restraint: (I1) fixes *two* things only —

1. **The mass scale.** The coefficient multiplying $1/r$ in $A(r)$'s leading correction is tied, via $\Phi=-GM/r$, to the physical mass $M$ of the source — this is what lets $r_s=2GM/c^2$ be read off as "the gravitational radius belonging to mass $M$," well before any question of horizons arises.
2. **The leading (first-order in $x$) term of $A(r)$.** Beyond that, (I1) says **nothing whatsoever** about the $O(x^2)$ and higher terms in $A(r)$'s expansion. Those nonlinear terms are exactly where the family's members will later differ from one another ([`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)), and pinning them down requires the additional ingredients (I2)–(I4) built in Part III.

*Beyond the paper (illustrative order of magnitude only):* $r_s$ for the Sun works out to about 3 kilometers, and for the Earth about 9 millimeters — vanishingly small compared to their physical radii, which is exactly why $x=r_s/r \ll 1$ almost everywhere in the solar system, and why the weak-field expansion this tutorial derives is such an excellent approximation for every classical test of gravity ([`PPN4`](../part6-ppn-observation/ppn4-classical-tests.md)).

## Simpler on-ramp

Think of $\Phi$ as measuring "how deep a gravitational well you're standing in" — more negative means deeper, closer to a large mass. The claim of this tutorial is simply: wherever that well is shallow (far from the mass, or for a not-too-massive source), a clock's rate must be lower by an amount directly proportional to how deep the well is — twice the potential, divided by $c^2$, subtracted from the flat-spacetime rate of $1$. That's the entire content of $A\approx1+2\Phi/c^2$: a bookkeeping requirement forced by nothing more exotic than "this theory had better reproduce ordinary falling apples far from any black hole." It says nothing yet about how clocks behave *deep* in the well, close to the mass — that's where the rest of the book's four assumptions, and eventually observation, will have to do more work.

## Check your understanding

1. Why must a valid metric reduce to $A\approx1+2\Phi/c^2$ specifically, rather than some other function of $\Phi$, in the weak-field limit?
2. What does $r_s=2GM/c^2$ physically represent at this stage of the book — is it yet tied to horizons or singularities?
3. Does the Newtonian limit constrain the $O(x^2)$ term in $A(r)$'s expansion? Why does that matter for the rest of the book?
4. Why is it not a coincidence that every member of the later $A_\lambda$ family shares the same leading term $1-x$?

<details>
<summary>Answers</summary>

- **1.** Because matching the weak-field geodesic equation to Newton's second law, term by term, forces exactly this relation — it's a direct consequence of demanding that ordinary Newtonian gravity be recovered as a limiting case, not a free choice among several equally valid options.
- **2.** At this stage, purely a length scale set by the mass, appearing because it's the natural way to write the coefficient of $1/r$ in the weak-field expansion of $A(r)$. Nothing here yet says anything about a horizon or singularity at $r=r_s$ — that identification only becomes meaningful once a specific full metric (Schwarzschild, $\lambda=-1$) is selected.
- **3.** No — (I1) is explicitly silent about $O(x^2)$ and higher terms. This is exactly why the Newtonian limit alone cannot distinguish members of the family: it constrains only the first term, leaving the rest as the genuine freedom that (I2)–(I4) and, later, observation must resolve.
- **4.** Because every family member is *required*, by the very construction of the family (built precisely to satisfy (I1) among its four defining ingredients), to reproduce this same weak-field limit — it's built into the family's definition, not a coincidental agreement discovered afterward.

</details>

## What the paper claims here

Grounds §2 (I1) directly, quoting closely: "$\Phi=-GM/r$, $A=1+2\Phi/c^2+O(\Phi^2/c^4)=1-2GM/(rc^2)+O(r^{-2})$. Define $r_s=2GM/c^2$, $x=r_s/r$, so $A=1-x+O(x^2)$. Fixes mass scale + leading behavior; not nonlinear terms." The paper's own restraint is exactly the point emphasized above: (I1) is deliberately narrow, and the book inherits that narrowness rather than smuggling in more than the Newtonian limit actually supplies.

---
**Path navigation:** ← [prev in default path](./f5-geodesics.md) · [next: SYM1 — Static, spherically symmetric metrics](./sym1-static-spherical.md) →
**See also:** [CORE1](../part3-building-the-family/core1-flux-freedom.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md)
