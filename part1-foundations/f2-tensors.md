# Vectors, One-Forms, Tensors, Coordinates

> **Tutorial `F2`** · Part 1 · **Goal:** just enough tensor language to know what a coordinate change does and does not change — and to seed the book's recurring theme, representation vs. fact. · **Prereqs:** [F1](./f1-metric.md).

**Where this sits in the arc.** This tutorial seeds the single idea that recurs, in disguise, at every major turn of the book: the closure parameter $\lambda$ is exposed in [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md) as a choice of *representation* (which function of $A$ closes the flux law), the Painlevé–Gullstrand "river velocity" in [`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md) is a representation of where curvature is displayed, and the whole epistemological payload of [`EPI1`](../part8-synthesis/epi1-representation-vs-fact.md) is exactly the distinction drawn here. Get comfortable with it now, in the easiest possible setting.

## Vectors as arrows, not tuples

A **vector** at a point in spacetime is a genuine geometric object — think of it as an arrow, a direction-and-magnitude, tangent to some curve through that point (the velocity of a particle passing through, say). It exists independently of any coordinate system. Once you *choose* coordinates $x^\mu$, the arrow gets a set of **components** $V^\mu$ (superscript index) — four numbers, one per coordinate direction. Change coordinates and the four numbers change, via the chain rule:

$$V'^\mu = \frac{\partial x'^\mu}{\partial x^\nu} V^\nu.$$

The arrow itself hasn't moved. Only its numerical description — its representation in a particular coordinate basis — has changed. This is the exact tensor-calculus analogue of changing basis for an ordinary vector in linear algebra: the vector is the same geometric object; its coordinates in a new basis are related to the old ones by a fixed transformation matrix.

## One-forms: the dual objects

A **one-form** (or covector) is the dual notion: a linear machine that eats a vector and returns a number. The most familiar example is the gradient of a scalar function $\phi$: $d\phi$ is a one-form whose action on a vector $V^\mu$ gives the directional derivative of $\phi$ along $V$. One-forms carry a **subscript** index, $\omega_\mu$, and transform oppositely to vectors under a coordinate change:

$$\omega'_\mu = \frac{\partial x^\nu}{\partial x'^\mu}\,\omega_\nu.$$

The metric $g_{\mu\nu}$ (two subscript indices) is what lets you convert between the two: it defines an inner product on vectors, and also gives a canonical way to turn a vector into a one-form ("lowering an index," $V_\mu \equiv g_{\mu\nu}V^\nu$) and back ("raising an index" with the inverse metric $g^{\mu\nu}$). You will not need to do this bookkeeping explicitly very often in this book, but it is worth knowing it exists: the metric is not just a distance-measuring device, it is also the dictionary between vectors and one-forms.

## Tensors, generally

A **tensor** is simply a multilinear generalization of vectors and one-forms: an object with some number of upper (vector-like) and lower (one-form-like) indices, that transforms by the chain rule applied once per index. The metric $g_{\mu\nu}$ is a tensor with two lower indices. Later, [`F7`](./f7-curvature.md) introduces the Riemann curvature tensor, which has four indices — but you do not need to manipulate it by hand anywhere in this book; you only need to know it is a genuine tensor (transforms consistently), unlike some of the intermediate objects used to build it.

## Coordinate change as relabeling

Here is the idea to hold onto: changing coordinates is **relabeling**, not moving anything physical. If you switch from Cartesian $(x,y,z)$ to spherical $(r,\theta,\phi)$ — worked out fully in [`F4`](./f4-curvilinear-coordinates.md) — you have not changed the room you're describing; you've changed which numbers you write down to describe the same points in it. Every *component* — of a vector, of the metric, of anything with indices — is liable to change under such a relabeling. What must **not** change is anything built as a genuine scalar from these objects (their fully-contracted, index-free combinations): the value of $ds^2$ along a given, physically fixed displacement; the proper time elapsed along a specific worldline; curvature invariants like the Kretschmann scalar ([`F7`](./f7-curvature.md)). These are the same number no matter which coordinates you used to compute them.

This is exactly the CS-familiar distinction between a program's semantics and one particular naming of its variables: alpha-renaming a program's local variables changes every syntactic token you'd point to, but it changes nothing about what the program *computes*. A component like $g_{tt}$, or a coordinate radius $r$, is a variable name; a scalar invariant is the computed value that survives any consistent renaming.

## Representation-dependent vs. invariant statements

This distinction is not academic — it is load-bearing for reading the rest of the book correctly. Two examples you will meet soon:

- **The coordinate radius is a choice, not automatically a fact.** [`F4`](./f4-curvilinear-coordinates.md) defines the *areal* radius (sphere at fixed $r$ has area $4\pi r^2$) — a specific, useful, but still conventional way to label spheres. [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md) shows the same physical geometry rewritten in *isotropic* coordinates, where the radial label is different. Both describe the identical spacetime; neither radial label is more "real" than the other. What *is* invariant — genuinely physical — is something like the proper circumference of a given sphere, or a curvature scalar evaluated there.
- **$\lambda$ is a representation choice, not a fact about gravity.** The whole one-parameter family $A_\lambda(r)$ arises ([`CORE2`](../part3-building-the-family/core2-log-variable-closure.md)) because the paper's flux postulate can be imposed on $A$ itself, on $\ln A$, on $1/A$, or on any other monotonic rescaling — each choice of "which variable obeys the flux law" is a choice of *representation* for the same underlying idea (a Gauss-law-like closure), and different choices give genuinely different metrics. Recognizing $\lambda$ as this kind of choice — rather than as a directly measured physical quantity — is the single most important reading skill the book asks of you.

## Simpler on-ramp

Imagine measuring the size of a room twice: once in feet, once in meters. The numbers you write down are completely different, but the room hasn't changed size. If someone hands you just the number "12" with no unit, you cannot know whether the room is small or enormous — the number alone, divorced from the convention that produced it, tells you nothing. Only a statement like "the room is 3.7 meters *or, equivalently*, 12 feet across" — the invariant fact, expressible in either convention — actually describes the room. Reading this book, whenever you see a coordinate-dependent quantity (a radius, a metric component, a "velocity" in some coordinate system), ask: is this the room's actual size, or just today's choice of units?

## Check your understanding

1. If you rotate your coordinate axes, does a physical velocity vector change? Do its components change?
2. Why is $ds^2$ (evaluated along a fixed, physical displacement) a better candidate for "physically real" than any single component $g_{\mu\nu}$?
3. In what sense is choosing "$V=A$" versus "$V=\ln A$" for the flux law (previewed here, developed in `CORE2`) analogous to choosing feet versus meters?
4. Give one example, from ordinary programming, of the difference between a program's semantics and one particular naming of its variables.

<details>
<summary>Answers</summary>

- **1.** No, the vector itself (an arrow with a definite direction and length) is unchanged; its numerical components in the new (rotated) basis do change.
- **2.** Because $ds^2$ along a specific worldline is a number every observer, in every coordinate system, will agree on (it equals $-c^2$ times the squared proper time elapsed) — it does not depend on how you chose to label events with coordinates, unlike any single component $g_{\mu\nu}$, which is basis-dependent by construction.
- **3.** Both are conventions for measuring the *same* underlying thing. Feet and meters both measure the room's size; $A$ and $\ln A$ are both candidate variables for expressing "a monotonic function of the potential obeys a flux law." Neither choice of unit, and neither choice of variable, is forced by the physics alone — but unlike feet-vs-meters (which agree after a fixed conversion factor), different choices of flux variable give genuinely *different* nonlinear metrics, which is exactly why $\lambda$ ends up being a real, physically distinguishable number once you fix the convention.
- **4.** Renaming every local variable `x` to `y` throughout a function changes every line of source code that mentions it, but the function computes exactly the same thing on the same inputs — the renaming is invisible to anyone who only calls the function and reads its output.

</details>

## What the paper claims here

This tutorial is background machinery, not a specific claim from the paper — but it grounds the discipline the paper practices throughout, most visibly in its insistence that $\lambda$ is "mathematically the constant squared-gradient coefficient" of a *chosen* closure variable (§1, §2.2–2.3), not a directly observed fact about gravity, and in its care to separate coordinate-dependent statements (a finite-radius zero of $A_\lambda$, §3) from invariant ones (a curvature-invariant divergence, bracketed explicitly rather than asserted). The book's recurring "representation vs. fact" thread ([`EPI1`](../part8-synthesis/epi1-representation-vs-fact.md)) is this tutorial's idea, generalized.

---
**Path navigation:** ← [prev in default path](./f1-metric.md) · [next: F3 — Special relativity as flat spacetime](./f3-special-relativity.md) →
**See also:** [F4](./f4-curvilinear-coordinates.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md), [PG2](../part7-michell-pg/pg2-where-did-curvature-go.md)
