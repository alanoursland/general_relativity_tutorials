# Coordinate vs. curvature singularities

> **Tutorial `S4`** · Part 2 · **Goal:** Distinguish a coordinate artifact from a genuine physical singularity, and give the tool (Kretschmann scalar) for telling them apart. · **Prereqs:** [S3](./s3-properties.md), [F7](../part1-foundations/f7-curvature.md)

**Where this sits in the arc.** This tutorial hands you the exact discipline that `ZERO2` will later apply, with real restraint, to the *other* members of the $\lambda$-family: a place where a metric component misbehaves is not automatically a place where physics breaks down. You need the criterion settled here — invariant vs. representation-dependent — before you can ask, later, whether a finite-radius zero of some $A_\lambda$ is a horizon, a genuine singularity, or something the paper simply declines to classify.

## Two places where Schwarzschild's metric misbehaves

$$ds^2 = -\left(1-\frac{r_s}{r}\right)c^2dt^2 + \left(1-\frac{r_s}{r}\right)^{-1}dr^2 + r^2 d\Omega^2.$$

Two radii stand out where a metric component either vanishes or diverges:

- **$r=r_s$:** $A=1-r_s/r=0$, so $g_{tt}=0$; $B=1/A\to\infty$, so $g_{rr}\to\infty$.
- **$r=0$:** $A\to-\infty$, $B\to0$; the areal radius itself, the very coordinate labeling the spheres, shrinks to zero.

Both look alarming written this way. Only one of them is a real problem.

## The criterion: coordinate-independent quantities

A metric component blowing up or vanishing tells you the *coordinates* have gone bad at that point — nothing more, by itself. To learn whether the *geometry* is actually singular there, you need a quantity built from the curvature that is guaranteed to give the same answer in every coordinate system: a curvature scalar, or more operationally, whether freely falling observers can be extended smoothly through the point (geodesic completeness) and whether tidal forces (proportional to curvature) stay finite along the way.

The standard tool is the **Kretschmann scalar**,

$$K \equiv R_{\alpha\beta\gamma\delta}R^{\alpha\beta\gamma\delta},$$

a full contraction of the Riemann tensor with itself. Being a scalar built from a coordinate-independent contraction, its value at a given point does not depend on which coordinates you used to compute it — unlike $g_{tt}$ or $g_{rr}$ individually. For the Schwarzschild geometry, working through the Riemann tensor components gives the compact result

$$K(r) = \frac{48\,G^2M^2}{c^4\,r^6}.$$

## Applying it

**At $r=r_s$:** $K(r_s) = 48G^2M^2/(c^4r_s^6)$ — a large but perfectly finite number for any macroscopic $M$ (recall $r_s\propto M$, so $K(r_s)\propto 1/M^4$: bigger black holes have *milder* curvature at their horizon, not sharper). Since $K$ stays finite there — and since one can construct coordinates that remain perfectly regular across $r=r_s$, such as Painlevé–Gullstrand coordinates (`PG1`) or Eddington–Finkelstein coordinates, in which no metric component blows up at all — the conclusion is unambiguous: $r=r_s$ is a **coordinate singularity**. Nothing physical happens there; a freely falling observer crossing it notices nothing special locally, and the areal-coordinate description in `S2` simply happens to use a bad chart at that one radius, the way a map of the Earth in latitude/longitude coordinates misbehaves at the poles without the poles being physically special.

**At $r=0$:** $K(r) = 48G^2M^2/(c^4r^6) \to \infty$ as $r\to0$, in *every* coordinate system — no relabeling can make this finite, because $K$ doesn't care about the labels. Tidal forces (which scale with curvature) diverge; no coordinate transformation removes the blow-up; geodesics reaching $r=0$ cannot be extended further. This is a genuine **curvature singularity**: a real, physical breakdown of the geometry, not an artifact of description.

## The general principle

The lesson generalizes far beyond Schwarzschild, and is the exact tool this book reaches for whenever a metric component looks alarming:

> A vanishing or diverging metric *component* at some radius is, by itself, inconclusive. Check a coordinate-independent quantity — a curvature scalar such as $K$, or the behavior of geodesics — at that same radius. If it stays finite (and a regular coordinate system can be found), the misbehaving component was a coordinate artifact. If it diverges in every coordinate system, the geometry itself is singular there.

This is precisely the discipline `ZERO2` will insist on when the $\lambda$-family's other members produce a zero of $g_{tt}$ at some finite radius $r_0=-\lambda r_s$: a vanishing $g_{tt}$ is, on its own, exactly as inconclusive as $r=r_s$ looked before you computed $K$.

## Simpler on-ramp

Think of a globe with the standard latitude/longitude grid. At the North Pole, "longitude" becomes undefined — every line of longitude converges to the same point, so the coordinate grid tears apart there. But nothing is actually wrong with the Earth at the North Pole; it's an ordinary patch of ground, just like anywhere else, and you could confirm that by, say, measuring the *curvature of the Earth's surface itself* (a coordinate-independent quantity) — which is the same smooth, finite value at the pole as everywhere else on the sphere. Compare that to an actual crumpled or torn piece of the sheet: no matter how you re-draw the grid lines, the crumple is still there, because it's a fact about the sheet, not about the grid. $r=r_s$ is the North Pole — a chart problem. $r=0$ is the crumple — a fact about the spacetime itself.

## Check your understanding

- Why is a vanishing $g_{tt}$, by itself, not enough evidence that spacetime is singular there?
- What makes the Kretschmann scalar a trustworthy diagnostic where individual metric components are not?
- Why does the finiteness of $K(r_s)$ *and* the existence of regular coordinates through $r=r_s$ both matter for concluding it's a coordinate artifact?
- Why does $K(r)\propto 1/M^4$ at $r=r_s$ mean bigger black holes have milder curvature at their horizons?

**Answers**
- Because $g_{tt}$ is a component of the metric in one particular coordinate system; it can vanish or blow up purely because the coordinates are ill-suited there, with nothing physically singular happening, exactly as latitude/longitude coordinates misbehave at the poles of an ordinary sphere.
- Because it is built as a full scalar contraction of the Riemann tensor, so its value at a point is the same number regardless of which coordinates were used to compute it — it cannot be an artifact of a particular chart.
- Finiteness of $K$ rules out an intrinsic curvature blow-up; the existence of a regular coordinate system (like Painlevé–Gullstrand) additionally demonstrates explicitly that the apparent problem in the original coordinates was removable, not merely "possibly" removable.
- Because $r_s\propto M$ and $K(r_s)=48G^2M^2/(c^4r_s^6)$ has $r_s^6\propto M^6$ in the denominator against only $M^2$ in the numerator, giving $K(r_s)\propto 1/M^4$ — larger $M$ pushes the horizon further out into a region where curvature is gentler, even though the total mass is greater.

## What the paper claims here

The paper invokes exactly this coordinate/curvature distinction as an explicit caveat rather than deriving it from scratch: discussing the finite-radius zeros of §3, it states plainly that Schwarzschild's zero at $r_s$ "is the standard horizon," while for other negative-$\lambda$ members "the paper does NOT classify local regularity or global causal character" of the corresponding zero — it refers to those points only as "zeros of the static time coefficient." Section 6 likewise notes that Schwarzschild's coordinates "extend regularly through $A=0$," implicitly invoking the same regular-coordinate-exists criterion used here. This tutorial supplies the machinery (Kretschmann scalar, the general finite-invariant-vs-diverging-invariant criterion) that makes that caveat precise and gives `ZERO2` a tool to apply — carefully, and only as far as the paper's own restraint permits — to the rest of the family.

---
**Path navigation:** ← [prev in default path](./s3-properties.md) · [next](../part3-building-the-family/core0-four-assumptions.md) →
**See also:** [F7](../part1-foundations/f7-curvature.md), [PG1](../part7-michell-pg/pg1-painleve-gullstrand.md), [ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md)
