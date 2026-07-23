# What Is a Metric?

> **Tutorial `F1`** · Part 1 · **Goal:** learn to read $ds^2$ as a machine that outputs proper time and proper length, and fix notation (indices, summation, signature) used for the rest of the book. · **Prereqs:** none — this is the starting point of Part I.

**Where this sits in the arc.** Every claim in this book — the metric ansatz in [`SYM1`](./sym1-static-spherical.md), the Newtonian limit in [`F6`](./f6-newtonian-limit.md), the whole $A_\lambda$ family — is a statement about a metric. Before any of that can mean anything, you need to know what a metric *is* and how to extract physical predictions (clock rates, distances, causal structure) from it. This tutorial is bedrock; nothing downstream works without it.

## The problem a metric solves

In ordinary 3D space, the Pythagorean theorem tells you the distance between two nearby points: $d\ell^2 = dx^2+dy^2+dz^2$. That formula is a *rule* for turning coordinate displacements into a physically meaningful length. A metric is the generalization of that rule to spacetime — a rule for turning a coordinate displacement $dx^\mu$ into a physically meaningful interval $ds^2$, from which you can read off elapsed time on a clock or length on a ruler.

The reason this needs generalizing at all is that spacetime mixes space and time, and — once gravity is present — the rule for combining coordinate displacements into physical intervals can change from point to point. The metric is exactly the data that tells you how.

## Index and summation notation

Label spacetime coordinates $x^0, x^1, x^2, x^3$, with $x^0 \equiv ct$ (time, scaled by $c$ so all four coordinates have units of length) and $x^1,x^2,x^3$ spatial. Greek indices $\mu,\nu,\dots$ run over all four values $0,1,2,3$; this convention is used throughout the book. The metric is a collection of numbers $g_{\mu\nu}$ (one for each pair of indices, so $4\times4 = 16$ numbers, only 10 independent since $g_{\mu\nu}=g_{\nu\mu}$) that define the **line element**

$$ds^2 = \sum_{\mu=0}^{3}\sum_{\nu=0}^{3} g_{\mu\nu}\,dx^\mu dx^\nu \;\equiv\; g_{\mu\nu}\,dx^\mu dx^\nu,$$

where the last form drops the summation signs — the **Einstein summation convention**: any index repeated once "up" and once "down" (or, loosely in this book's index-light usage, simply repeated) is summed over automatically. You will see this convention everywhere; it is bookkeeping, not new physics.

You can think of $g_{\mu\nu}$ at a point as a symmetric matrix, and $ds^2$ as the quadratic form that matrix defines when fed a displacement vector $dx^\mu$ — exactly the inner product $\mathbf{v}\cdot\mathbf{v}$ from linear algebra, generalized to a matrix that need not be the identity and need not even be positive-definite (see below).

## Signature: why one sign is different

In flat 3-space, $d\ell^2=dx^2+dy^2+dz^2 \ge 0$ always — every displacement has a nonnegative squared length. Spacetime's metric is different: it uses the **signature** $(-,+,+,+)$, meaning (in the simplest case, flat spacetime — see [`F3`](./f3-special-relativity.md))

$$ds^2 = -c^2dt^2 + dx^2+dy^2+dz^2.$$

The minus sign on the time part is not a typo or an arbitrary convention pun — it is what makes $ds^2$ capable of distinguishing *when* two events could be cause and effect from when they cannot. Three cases matter:

- $ds^2 < 0$: the separation is **timelike** — a clock could travel between the two events. 
- $ds^2 > 0$: the separation is **spacelike** — no signal (not even light) can connect the events; simultaneity becomes frame-dependent.
- $ds^2 = 0$: the separation is **null** — exactly what light does.

This threefold split is the seed of the light-cone structure worked out fully in [`F3`](./f3-special-relativity.md). (Some books use the opposite overall sign, $(+,-,-,-)$; this book fixes $(-,+,+,+)$ throughout, matching the source paper, so that $-g_{tt}>0$ for an ordinary static metric — see below.)

## Reading $ds^2$ as proper time

For a **timelike** separation, define the **proper time** $d\tau$ — the time actually elapsed on a clock carried along that displacement — by

$$ds^2 = -c^2 d\tau^2 \quad\Longrightarrow\quad d\tau = \frac{\sqrt{-ds^2}}{c}.$$

This is the single most important operational fact about the metric: *it is a clock-reading machine.* Feed it a small displacement along a clock's worldline, and it hands back exactly how much that clock ages. This is not a metaphor — it is the definition of proper time in relativity, and every physical prediction about clocks (gravitational time dilation, twin-paradox-style comparisons in [`F3`](./f3-special-relativity.md)) reduces to evaluating $ds^2$ along a worldline.

For a **spacelike** separation, the analogous quantity is proper *length*: $d\ell^2 = ds^2$ directly (no factor of $c$ needed, since space and time already share units via $x^0=ct$).

## $-g_{tt}$ as a clock rate

Consider a metric of the general static form used throughout this book (derived properly in [`SYM1`](./sym1-static-spherical.md)):

$$ds^2 = -A(r)\,c^2dt^2 + B(r)\,dr^2 + r^2 d\Omega^2, \qquad g_{tt} = -A(r)c^2.$$

A **static observer** sits at fixed $r,\theta,\phi$, so $dr=d\theta=d\phi=0$ along their worldline, and the line element collapses to $ds^2 = -A(r)c^2dt^2$. By the proper-time rule above,

$$d\tau = \sqrt{A(r)}\,dt = \sqrt{-g_{tt}/c^2}\;dt.$$

So $-g_{tt}$ (or, in this book's convention, $A(r)$) is literally the **squared clock rate**: it tells you what fraction of coordinate time $dt$ actually elapses on a clock sitting at that location. Where $A<1$, clocks run *slow* relative to coordinate time $t$ — this single fact is the entire content of gravitational time dilation, and it is exactly the quantity the Newtonian limit ([`F6`](./f6-newtonian-limit.md)) will pin down to leading order.

## What's invariant, what isn't

One last point, developed fully in [`F2`](./f2-tensors.md): the *components* $g_{\mu\nu}$ depend on your choice of coordinates — change coordinates and the numbers change. But $ds^2$ evaluated along a specific, physically given displacement (or the proper time accumulated along a specific worldline) does **not** depend on which coordinates you used to compute it. The metric's components are a representation; the proper time it predicts is a fact. Keeping this distinction sharp is the single habit this book will ask of you more than any other.

## Simpler on-ramp

Think of the metric as a recipe card, different at every location, for converting "how far you moved in coordinates" into "how much you actually aged or how far you actually traveled." On a flat sheet of paper with ordinary $x,y$ axes, the recipe is always the Pythagorean theorem — the same everywhere. In spacetime the recipe includes a time ingredient with a minus sign (so that moving through *time alone* still counts as a valid "distance," but one you measure with a clock, not a ruler), and near a mass, the recipe's numbers change from place to place — clocks tick at different rates and rulers measure different amounts of proper length depending on where they are. The whole business of "gravity curves spacetime" is just this: the recipe card's numbers are no longer the same everywhere.

## Check your understanding

1. Why can't $ds^2$ have the same sign convention as ordinary Euclidean distance?
2. If a metric has $A(r) < 1$ at some radius, what does that tell you about a clock sitting there, compared to one very far away?
3. What is invariant when you change coordinates: the numbers $g_{\mu\nu}$, or the proper time along a specific worldline?
4. Why does this book write $x^0=ct$ rather than just $t$?

<details>
<summary>Answers</summary>

- **1.** Because spacetime needs to distinguish timelike, spacelike, and null separations — a distinction with direct physical meaning (what can causally influence what). A single Euclidean sign can't encode that; the mixed signature $(-,+,+,+)$ can.
- **2.** It ticks slower: $d\tau = \sqrt{A(r)}\,dt < dt$, so less proper time elapses there per unit of coordinate time than for a distant observer at $A\approx1$.
- **3.** The proper time (or $ds^2$ along that worldline) is invariant. The components $g_{\mu\nu}$ are representation-dependent — they change when you change coordinates.
- **4.** So that all four coordinates share the same units (length), which lets the metric components $g_{\mu\nu}$ be compared and combined directly, and keeps $c$ explicit throughout rather than silently setting $c=1$.

</details>

## What the paper claims here

This tutorial is foundational scaffolding rather than a direct claim from the source paper, but it fixes exactly the notation the paper uses throughout: signature $(-,+,+,+)$, $c$ kept explicit, and the metric written as $ds^2=-A(r)c^2dt^2+B(r)dr^2+r^2d\Omega^2$ (§2) with $A(r)$ read as the clock-rate function. The paper's clock-rate relation $d\tau=\sqrt{A}\,dt$ and proper radial distance $d\ell=\sqrt{B}\,dr$ (§2, discussion of (I3)) both rest on exactly the reading of the metric developed here.

---
**Path navigation:** ← [prev in default path](../part0-orientation/map.md) · [next: F2 — Vectors, one-forms, tensors, coordinates](./f2-tensors.md) →
**See also:** [F3](./f3-special-relativity.md), [SYM1](./sym1-static-spherical.md), [notation](../reference/notation.md)
