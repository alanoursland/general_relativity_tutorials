# Special Relativity as Flat Spacetime

> **Tutorial `F3`** · Part 1 · **Goal:** the Minkowski metric, proper time along a worldline, light cones, and why $-g_{tt}$ is a clock rate — the "no gravity" baseline every later metric is compared against. · **Prereqs:** [F1](./f1-metric.md), [F2](./f2-tensors.md).

**Where this sits in the arc.** Special relativity is the $A=B=1$ member of every static spherically symmetric ansatz this book will write down ([`SYM1`](./sym1-static-spherical.md)) — it is what "asymptotically flat" (§2) means: far from any mass, spacetime looks like this. It also supplies the light-cone language [`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md) needs to give the cleanest operational definition of a horizon.

## The Minkowski metric

Special relativity is the physics of flat spacetime — no gravity, no curvature. In Cartesian coordinates $(t,x,y,z)$, its metric is the simplest possible one consistent with the signature fixed in [`F1`](./f1-metric.md):

$$ds^2 = -c^2dt^2 + dx^2+dy^2+dz^2.$$

Every component of $g_{\mu\nu}$ is a constant ($-1$ or $+1$, times $c^2$ where relevant); nothing depends on position. This is what "flat" means concretely: the recipe card from [`F1`](./f1-metric.md)'s on-ramp has the same numbers everywhere. In spherical spatial coordinates (derived in [`F4`](./f4-curvilinear-coordinates.md)), the identical flat geometry reads $ds^2 = -c^2dt^2+dr^2+r^2d\Omega^2$ — this is exactly the $A=B=1$ case of the general static ansatz in [`SYM1`](./sym1-static-spherical.md).

## Proper time along a worldline

Consider an object moving with ordinary velocity $v = |d\mathbf{x}/dt|$ (constant, for simplicity) through flat spacetime. Along its worldline, $dx^2+dy^2+dz^2 = v^2dt^2$, so

$$ds^2 = -c^2dt^2 + v^2dt^2 = -(c^2-v^2)\,dt^2.$$

Using the proper-time rule from [`F1`](./f1-metric.md), $ds^2=-c^2d\tau^2$:

$$c^2 d\tau^2 = (c^2-v^2)dt^2 \quad\Longrightarrow\quad d\tau = dt\sqrt{1-\frac{v^2}{c^2}}.$$

This is ordinary time dilation, derived from nothing but "evaluate $ds^2$ along the worldline and read off proper time" — no separate postulate needed beyond the metric itself. Two things worth flagging for later: first, proper time is accumulated by *integrating* $d\tau$ along a specific worldline, so two worldlines connecting the same pair of events can accumulate different total proper time (the textbook "twin paradox" is exactly this — a moving twin's path integrates less $d\tau$ than a stationary one's). Second, among all timelike worldlines between two fixed events, the straight (inertial, unaccelerated) one *maximizes* accumulated proper time — this extremal property is exactly what a geodesic is ([`F5`](./f5-geodesics.md)), and free-fall trajectories in curved spacetime generalize it.

## Light cones

Set $ds^2=0$ in the Minkowski metric: $c^2dt^2 = dx^2+dy^2+dz^2$, i.e. $|d\mathbf{x}|/dt = c$ — exactly the locus traced out by light emitted from an event in every direction. At any event, this null condition carves spacetime into three regions relative to that event:

- **Timelike future/past** ($ds^2<0$, inside the cone): events a slower-than-light signal, or an observer's own worldline, can reach or have come from.
- **Spacelike** ($ds^2>0$, outside the cone): events no signal from the event can reach or could have influenced it — causally disconnected.
- **Null** ($ds^2=0$, on the cone itself): what light rays trace out.

This partition — the **light cone** at each event — is the entire causal structure of spacetime. Nothing more exotic is needed to say what can influence what. When later chapters ask whether a horizon exists ([`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md)), the sharpest possible statement of the question is exactly "do the light cones tip over so far that even the *outgoing* branch fails to escape?" — a question phrased entirely in the vocabulary introduced here.

## Why $-g_{tt}$ is a clock rate, revisited

In Minkowski coordinates, $g_{tt}=-c^2$, and for a static observer ($dx=dy=dz=0$) the proper-time relation from [`F1`](./f1-metric.md) gives $d\tau = \sqrt{-g_{tt}/c^2}\,dt = dt$ exactly — flat spacetime's clocks tick at the coordinate rate, with no correction, precisely because there is no gravity to slow them. This is the reference point against which the Newtonian limit ([`F6`](./f6-newtonian-limit.md)) will introduce the first nonzero correction: a metric of the general form $ds^2=-A(r)c^2dt^2+\dots$ reduces to flat Minkowski spacetime exactly when $A\to1$, and asymptotic flatness (required of every member of the $A_\lambda$ family, §2) is precisely the statement that this happens far from the source.

## Simpler on-ramp

Picture a spacetime diagram: time running up the page, one spatial direction running across. A flash of light from the origin traces two 45° lines — the light cone. Anything that could ever affect you, or that you could ever affect, has to lie inside those lines (or on them, for light itself); anything outside is permanently out of causal reach. A clock's worldline is some path up the page; if it wiggles back and forth (accelerates) it always logs *less* total elapsed time than a clock that goes straight up between the same two endpoints — motion "costs" proper time. This is why a traveling twin comes back younger: not a paradox, just the geometric fact that the straight path between two spacetime events is the one that accumulates the most proper time.

## Check your understanding

1. Why does a moving clock accumulate less proper time than a stationary one between the same two events, using only the metric (no separate postulate)?
2. What three regions does the light cone at an event divide spacetime into, and what physically distinguishes them?
3. In Minkowski spacetime, what is $d\tau/dt$ for a static observer, and why does that make sense given no gravity is present?
4. Why is "asymptotically flat" (used throughout the rest of the book) best understood as "approaches the metric of this tutorial far from the source"?

<details>
<summary>Answers</summary>

- **1.** Because $ds^2=-(c^2-v^2)dt^2$ for a moving worldline is less negative (in magnitude) than $-c^2dt^2$ for a stationary one over the same coordinate time $dt$ — directly from evaluating the metric, with no extra assumption.
- **2.** Timelike (inside the cone: causally reachable/reaching, by a slower-than-light signal or worldline), spacelike (outside: causally disconnected), and null (on the cone: what light traces out).
- **3.** $d\tau/dt=1$ exactly — coordinate time and proper time coincide, because $g_{tt}=-c^2$ has no position-dependent suppression; with no mass around to curve the metric, there is nothing to slow the clock.
- **4.** Because "asymptotically flat" is defined (§2) as $A,B\to1$ as $r\to\infty$, which is exactly the condition for the metric to reduce, far away, to the flat Minkowski line element of this tutorial.

</details>

## What the paper claims here

The paper does not re-derive special relativity; it assumes it as the $r\to\infty$ limit required by **asymptotic flatness** in §2's ansatz ("asymptotic flatness: $A,B\to1$ as $r\to\infty$"). This tutorial supplies exactly that background: what "the metric approaches Minkowski spacetime" concretely means, and why it is the natural boundary condition to impose on an isolated, static, spherical source.

---
**Path navigation:** ← [prev in default path](./f2-tensors.md) · [next: F4 — Flat space in curvilinear coordinates](./f4-curvilinear-coordinates.md) →
**See also:** [F5](./f5-geodesics.md), [PG1](../part7-michell-pg/pg1-painleve-gullstrand.md), [PG4](../part7-michell-pg/pg4-horizons-light-cones.md)
