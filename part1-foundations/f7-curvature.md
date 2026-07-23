# Curvature, Briefly

> **Tutorial `F7`** · Part 1 · **Goal:** enough of Riemann/Ricci/Kretschmann to say "an invariant that diverges is a real singularity," and to tell a coordinate singularity from a curvature singularity. · **Prereqs:** [F1](./f1-metric.md), [F2](./f2-tensors.md), [F4](./f4-curvilinear-coordinates.md).

**Where this sits in the arc.** This tutorial supplies the exact diagnostic that [`S4`](../part2-schwarzschild/s4-singularities.md) uses to separate Schwarzschild's coordinate artifact at $r_s$ from its genuine singularity at $r=0$, and the tool [`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) needs — and the paper deliberately declines to fully use — when asking whether *other* family members' finite-radius zeros are anything more than zeros of $A(r)$.

## The problem: a blown-up number might just be bad coordinates

Suppose some metric component — $B(r)=1/A(r)$, say — diverges as $r\to r_0$ for some radius $r_0$. Is that a real breakdown of the geometry, or merely a symptom of having chosen an unlucky coordinate system there? You cannot tell from a single component alone: components are representation-dependent ([`F2`](./f2-tensors.md)), so a divergence in one of them might vanish entirely in a better-chosen chart. You need a test that gives the *same* answer regardless of which coordinates you used to compute it — a genuine invariant.

## Riemann, Ricci, and why Christoffel symbols aren't enough

The Christoffel symbols used to write the geodesic equation ([`F5`](./f5-geodesics.md)) are not themselves tensors — they can be made to vanish at any single point by a clever local choice of coordinates (this is the mathematical content of the equivalence principle: locally, gravity can always be "transformed away"). So a Christoffel symbol blowing up somewhere doesn't, by itself, mean anything invariant is wrong.

The genuine, coordinate-independent measure of curvature is the **Riemann tensor**, built from derivatives of the Christoffel symbols. Conceptually, it measures tidal effects: how much a small loop of parallel-transported vectors fails to close up on itself, or equivalently, how much nearby freely-falling particles' separations accelerate relative to each other (the actual, physical signature of gravity that cannot be transformed away at a point, unlike a Christoffel symbol). You will not need to compute it directly anywhere in this book — only to know that, unlike the Christoffel symbols, it is a genuine tensor: if all its components vanish in one coordinate system, they vanish in every coordinate system.

The **Ricci tensor** is a particular contraction (trace) of the Riemann tensor. It is what appears directly in the vacuum Einstein equations ([`S1`](../part2-schwarzschild/s1-vacuum-einstein.md)): $R_{\mu\nu}=0$ in vacuum. But Ricci vanishing does **not** mean Riemann vanishes — a vacuum region around a mass has zero Ricci tensor yet nonzero Riemann tensor, which is exactly why tidal forces (real physical stretching and squeezing) are present in the empty space around, say, the Sun, even though there is no local matter there to source them.

## Scalar invariants: a fair test

To get a single, unambiguous, coordinate-independent number out of the Riemann tensor, contract all of its indices against the metric (and its inverse) until nothing is left uncontracted — the result is a **scalar**, and by the transformation rules of [`F2`](./f2-tensors.md), a scalar's *value* at a given event is the same in every coordinate system. The standard example used in this book is the **Kretschmann scalar**,

$$K \equiv R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma},$$

built by fully contracting the Riemann tensor with itself. Whatever coordinates you use to compute $K$ at a given event, you get the same number.

## The diagnostic

This gives a clean, fair test for distinguishing two very different kinds of "something looks broken here":

- **Coordinate singularity**: some metric *component* misbehaves (diverges, or the metric fails to be invertible) at some location, but curvature invariants like $K$ remain perfectly finite there. This signals nothing more than an unlucky choice of coordinates — a better chart, extended smoothly through that location, removes the apparent problem entirely (this is exactly what happens at Schwarzschild's $r=r_s$, and exactly what motivates switching to Painlevé–Gullstrand coordinates, [`PG1`](../part7-michell-pg/pg1-painleve-gullstrand.md), to see through it).
- **Curvature singularity**: an invariant like $K$ **genuinely diverges** at some location, in every coordinate system. No relabeling fixes this — it is a real breakdown of the geometry itself, not an artifact of description. Schwarzschild's $K \propto r_s^2/r^6$ diverging as $r\to0$ is the standard example.

The rule this book holds to throughout, stated plainly: **never call a zero of $g_{tt}$ (or any other single metric component) a "real" singularity — or a horizon — without checking a curvature invariant.** A vanishing metric component is, by itself, evidence of nothing beyond "this coordinate system is behaving badly (or interestingly) here."

## What this diagnostic does *not* establish

Be careful about the limits of this test, matching the restraint the rest of the book practices: showing that curvature invariants stay finite at some location is evidence the *geometry* is regular there — it does **not**, by itself, establish everything one might eventually want to know about that location's global causal structure (whether it behaves like a genuine, complete, one-way membrane — a horizon in the full sense). That is a further, separate question about the global behavior of light cones there ([`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md)), not something the local finiteness of an invariant settles on its own. This book is careful to keep "invariants are finite here" and "this is a fully understood horizon" as two separate claims, only the first of which this tutorial's tools directly establish.

## Simpler on-ramp

Think of a flat map of the Earth (a Mercator projection): near the poles, distances on the map become wildly distorted — lines that should be short look infinitely long. But the actual surface of the Earth at the pole is perfectly smooth; nothing is wrong with the *sphere*, only with that particular flattened drawing of it. That's a coordinate singularity: fixable by choosing a better map centered on the pole. Contrast a genuine tear or hole ripped in a piece of fabric: no matter how you re-photograph it, from any angle, in any lighting, the tear is still there — it's a property of the fabric itself, not of how you're looking at it. That's a curvature singularity. The whole point of a scalar invariant like the Kretschmann scalar is that it's the mathematical equivalent of "check the fabric itself, not just one photograph of it."

## Check your understanding

1. Why isn't a divergence in a Christoffel symbol, by itself, evidence of a real curvature problem?
2. Why can the Ricci tensor vanish (vacuum) while genuine tidal forces (Riemann) are still present?
3. What makes the Kretschmann scalar a "fair" test, when a single metric component is not?
4. If curvature invariants are finite at some location, does that alone tell you it's a fully-understood horizon? Why or why not?

<details>
<summary>Answers</summary>

- **1.** Because Christoffel symbols are not tensors — they can be made to vanish at a point by a suitable local coordinate choice even in genuinely curved spacetime, so their value alone carries no coordinate-independent information.
- **2.** Because Ricci is only a particular trace (partial contraction) of the full Riemann tensor; the Einstein vacuum equations set that trace to zero, but the rest of Riemann's information (encoding tidal stretching/squeezing) can be, and generically is, nonzero in vacuum around a mass.
- **3.** Because it is a fully contracted scalar built from a genuine tensor (Riemann), so by the transformation rules of tensors, its numerical value at a given event is the same regardless of which coordinate system was used to compute it — unlike any single metric or Riemann component.
- **4.** No — finite curvature invariants show the local geometry is regular there, but they don't by themselves establish the full global causal structure (whether light cones tip over irrevocably, [`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md)); that is a separate, further question this book keeps distinct.

</details>

## What the paper claims here

Grounds the §3 caveat directly: for members of the family with $\lambda<0$ other than Schwarzschild, the paper explicitly declines to classify "local regularity or global causal character" of the finite-radius zero $r_0=-\lambda r_s$, referring to it only as "a zero of the static time coefficient." This tutorial supplies exactly the machinery (curvature invariants) that such a classification would require, precisely so the reader can see what question is being deliberately left open rather than answered by assumption.

---
**Path navigation:** ← [prev in default path](./sym1-static-spherical.md) · [next: GAUSS1 — Gauss's law, flux, and the radial Laplacian](./gauss1-flux-laplacian.md) →
**See also:** [ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md), [S4](../part2-schwarzschild/s4-singularities.md)
