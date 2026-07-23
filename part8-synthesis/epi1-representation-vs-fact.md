# Representation vs. Fact

> **Tutorial `EPI1`** · Part 8 · **Goal:** make explicit the book's throughline — $\lambda$ as a gauge/closure choice, and the discipline of separating what a description encodes from what the geometry is · **Prereqs:** [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md), [`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md), [`F2`](../part1-foundations/f2-tensors.md).

**Where this sits in the arc.** This is the epistemic spine of the book stated plainly. Two very different-looking moves in the paper — the appearance of the parameter $\lambda$ in [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md), and the disappearance of spatial curvature into a mixed term in [`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md) — are the *same* phenomenon: quantities that live in the description, not in the geometry. Learning to sort those from invariants is the transferable skill this whole book is teaching under the cover of one physics problem.

## The distinction

A physical setup can be described many ways. Some features of a description track something real about the system; others are artifacts of the choices you made in setting the description up. Call the first kind **facts** (invariants) and the second kind **representation** (gauge). The competence the paper's author repeatedly exercises is telling them apart *without being fooled by how physical the representation looks*.

For a spacetime, the working criterion is coordinate-invariance. A statement is a **fact** if it survives any smooth relabeling of coordinates — proper time along a worldline, the area of a symmetry sphere, a curvature scalar like the Kretschmann invariant. A statement is **representation** if a legal change of description can alter it — the numerical value of $g_{tt}$ at a point, whether a spatial slice looks flat, the coordinate radius at which some coefficient hits a particular value. Coordinate changes are the "gauge transformations" of the metric: they preserve every invariant and are free to rearrange everything else. This is the content of [`F2`](../part1-foundations/f2-tensors.md), now put to work.

For a CS reader the analogy is exact. A representation choice is like a choice of basis, a serialization format, or a coordinate chart on a manifold of possible encodings: it changes the *numbers on the page* while the *object* is untouched. A fact is the analogue of a basis-independent quantity — a trace, a spectrum, a topological invariant. Confusing the two is the source of a remarkable number of "paradoxes," in physics and out of it.

## $\lambda$ is a closure choice

Recall how $\lambda$ enters ([`CORE1`](../part3-building-the-family/core1-flux-freedom.md)–[`CORE2`](../part3-building-the-family/core2-log-variable-closure.md)). The flux postulate (I2) demands that *some* monotonic potential variable $V(A)$ obey the vacuum Gauss law $\Delta V = 0$. It does **not** say which function of $A$ is $V$. Write $V = F(s)$ with $s = \ln A$ and apply the chain rule:

$$\Delta V = F'(s)\,\Delta s + F''(s)\,(s')^2.$$

Setting $\Delta V = 0$ and dividing by $F'$ gives $\Delta s = -\dfrac{F''(s)}{F'(s)}\,(s')^2$, and the constant-coefficient closure (I4) names that coefficient:

$$\boxed{\ \lambda = -\frac{F''}{F'}\ }, \qquad \text{so that}\quad \Delta s = \lambda\,(s')^2.$$

Read this slowly. $\lambda$ is *the constant ratio $-F''/F'$ of the function $F$ you chose to make the flux law exact.* It is manufactured by the choice of potential variable. Choose $V \propto A$ and you have selected $\lambda = -1$; choose $V \propto \ln A$ and you have selected $\lambda = 0$; choose $V \propto 1/A$ and you have selected $\lambda = +1$ ([`CORE5`](../part3-building-the-family/core5-distinguished-members.md)). Nothing in "static, spherical, Newtonian at infinity" prefers one $F$ over another. **$\lambda$ is representation before it is fact.** It labels *which description closes the flux law*, and the different $\lambda$'s genuinely give different geometries only because the postulate (I2) is itself coordinate-dependent — a postulate, not a covariant field equation (see the negative-space note: a different coordinate choice for the flux law would give a different family).

This is the single most important reframing in the book. The historical shortcuts argue about "the" nonlinear term as though the geometry dictated it; the paper shows the nonlinear term is downstream of a closure choice that the base assumptions leave open.

## What a coordinate change preserves — and what it moves

The second appearance of the same lesson is the Painlevé–Gullstrand form ([`PG1`](../part7-michell-pg/pg1-painleve-gullstrand.md)–[`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md)). Start from the areal, diagonal form and change only the time coordinate, $dt = dT - \frac{\sqrt{1-A}}{cA}dr$. The metric becomes

$$ds^2 = -c^2 dT^2 + \big[\,dr + v(r)\,dT\,\big]^2 + r^2 d\Omega^2, \qquad v(r) = c\sqrt{1 - A(r)}.$$

On a constant-$T$ slice the spatial metric is $d\ell^2 = dr^2 + r^2 d\Omega^2$ — *exactly flat Euclidean space*. The spatial curvature that was manifest in the diagonal form ($B = 1/A \ne 1$) has not been destroyed; it has been **moved into the mixed term $2v\,dr\,dT$**, which tilts the radial light cones. Flat slices do **not** mean flat spacetime. The invariants — the Kretschmann scalar, the tidal forces, the causal structure — are untouched; the change of clock merely repackages where the geometry's content is displayed.

The parallel to $\lambda$ is exact and deliberate. In [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md) a choice of *potential variable* decides how a nonlinear term is displayed; in [`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md) a choice of *time coordinate* decides how curvature is displayed. Both are representation. The discipline is to ask, of any striking feature, *does it survive relabeling?* — and if it does not, to refuse to draw a physical conclusion from it. This is why the book never calls a flat PG slice "evidence of no curvature," and never calls a zero of $g_{tt}$ a "horizon" without an invariant check ([`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md)).

## When representation becomes fact

Representation is not *meaningless* — it becomes physical the moment you tie it to an invariant. $\lambda$ is a closure choice, but $\beta = \lambda + 2$ is a post-Newtonian parameter that couples to a measurable orbit ([`PPN3`](../part6-ppn-observation/ppn3-gamma-beta.md)); the moment you measure perihelion precession, the once-free $\lambda$ acquires a fact-valued reading. Likewise the PG river velocity $v$ is a coordinate shift, not a material flow, yet $v = c$ pinpoints an invariant surface *for Schwarzschild specifically*. The lesson is not "ignore representation." It is: **know which side of the line you are on at every step, and only cross from representation to fact through an invariant you can name.** That crossing is what turns the math family of Part III into the physics of Part VI.

## Simpler on-ramp

Two maps of the same city can disagree about which street is "vertical" without disagreeing about the distance between two cafés. "Vertical" is a feature of the map; the distance is a feature of the city. In this book, $\lambda$ is a "which-way-is-up" choice — it records which variable you decided to make simple — and the flat-looking Painlevé–Gullstrand slice is another such choice, one that makes space look Euclidean by hiding the gravity in how clocks are drawn. Neither choice changes the city. What *does* live in the city — proper times, sphere areas, tidal stretching, whether outgoing light can escape — is the same no matter which map you hold. The skill the whole book drills is reading a map and instantly knowing which lines are the city and which are the cartographer.

## Check your understanding

1. In one sentence, what does $\lambda$ actually measure, mathematically?
2. A Painlevé–Gullstrand spatial slice is flat. Why is it wrong to conclude the spacetime is flat?
3. If $\lambda$ is "just" a representation choice, how can different $\lambda$'s be different physical spacetimes at all?
4. Give the general rule for deciding whether a feature of a metric is a fact or an artifact.

<details>
<summary>Answers</summary>

- **1.** The constant ratio $-F''/F'$ of the function $F$ you chose so that $V = F(\ln A)$ makes the flux law $\Delta V = 0$ exact — i.e. which potential variable closes the system.
- **2.** Flatness of a *slice* is a property of the chosen time-slicing; the spacetime curvature has been moved into the mixed $2v\,dr\,dT$ term. The invariants (e.g. Kretschmann) are unchanged and nonzero.
- **3.** Because the flux postulate (I2) is written in a *fixed* coordinate (areal $r$) and is not covariant. Once you commit to that postulate, different closures give genuinely different geometries. The representation-freedom is upstream, in choosing $V$; it induces real physical differences downstream. Tie $\lambda$ to $\beta$ and the difference becomes measurable.
- **4.** Ask whether a smooth change of coordinates can alter it. If yes, it is representation (gauge). If it survives every relabeling — a proper time, an area, a curvature scalar — it is a fact.

</details>

## What the paper claims here

This tutorial grounds §2.2–2.3 (the emergence of $\lambda = -F''/F'$), §6.1 (the PG mixed term), and the paper's repeated insistence on coordinate-dependence: the flux law is "a postulate, not a covariant field equation," written in areal coordinates, and "a different coordinate choice gives a different family." The paper is explicit that the PG river velocity is "a representation of the coordinate shift, not a material velocity," and that flat constant-$T$ slices coexist with genuine curvature. The framing of $\lambda$ as a representation/closure choice is faithful to the paper's own language ("the effective coefficient," "$\lambda$ is mathematically the constant squared-gradient coefficient; only under Sec. 4's extra assumptions can it be read as a self-energy weight"). The CS gauge-freedom analogy is the book's pedagogy, not the paper's wording.

---
**Path navigation:** ← [SYN1 — a century of shortcuts](syn1-century-of-shortcuts.md) · [next: EPI2 — identities are not measurements](epi2-identities-not-measurements.md) →
**See also:** [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md), [`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md), [`F2`](../part1-foundations/f2-tensors.md), [`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md), [`MAP`](../part0-orientation/map.md)
