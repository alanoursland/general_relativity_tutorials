# Flat Space in Curvilinear Coordinates

> **Tutorial `F4`** · Part 1 · **Goal:** derive flat space in spherical coordinates, understand what $r^2 d\Omega^2$ means, and fix the precise definition of **areal radius** used throughout the book. · **Prereqs:** [F1](./f1-metric.md), [F3](./f3-special-relativity.md).

**Where this sits in the arc.** The paper's entire ansatz (§2, developed here in [`SYM1`](./sym1-static-spherical.md)) is written in **areal coordinates** — and the precise meaning of "$r$" defined in this tutorial is exactly what makes that ansatz's radial coordinate a specific, checkable choice rather than a vague "distance from the center." This distinction resurfaces sharply in [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md), where the same geometry is rewritten with a *different* radial coordinate.

## From Cartesian to spherical

Flat 3-space in Cartesian coordinates has line element $d\ell^2 = dx^2+dy^2+dz^2$. Introduce spherical coordinates $(r,\theta,\phi)$ via the usual relations

$$x = r\sin\theta\cos\phi, \qquad y=r\sin\theta\sin\phi, \qquad z=r\cos\theta,$$

with $r\ge0$ the distance from the origin, $\theta\in[0,\pi]$ the polar angle, $\phi\in[0,2\pi)$ the azimuthal angle. Differentiating and substituting into $d\ell^2$ (a standard but instructive piece of algebra — every cross term between $dr$, $d\theta$, $d\phi$ cancels after using $\sin^2+\cos^2=1$ repeatedly) gives the flat-space line element in spherical coordinates:

$$d\ell^2 = dr^2 + r^2\left(d\theta^2+\sin^2\theta\,d\phi^2\right) \equiv dr^2 + r^2 d\Omega^2, \qquad d\Omega^2 \equiv d\theta^2+\sin^2\theta\,d\phi^2.$$

Nothing physical has changed — this is *the same flat space*, just relabeled with a different, curvilinear coordinate grid, exactly the relabeling idea from [`F2`](./f2-tensors.md). The full flat spacetime metric in these coordinates, combining with [`F3`](./f3-special-relativity.md), is

$$ds^2 = -c^2dt^2 + dr^2 + r^2d\Omega^2.$$

## What $r^2 d\Omega^2$ means

The term $d\Omega^2 = d\theta^2+\sin^2\theta\,d\phi^2$ is the standard metric of a unit sphere — the line element you'd get restricting to $r=1$. Multiplying by $r^2$ scales that unit-sphere geometry up to whatever size a sphere of coordinate radius $r$ actually has. Concretely: hold $r$ fixed and look only at the induced 2D geometry on that sphere; its line element is $d\ell^2_{\text{sphere}} = r^2 d\theta^2 + r^2\sin^2\theta\,d\phi^2$, and its total surface area is

$$\text{Area} = \int_0^\pi\int_0^{2\pi} r^2\sin\theta\,d\phi\,d\theta = r^2 \cdot 4\pi = 4\pi r^2.$$

So the coefficient of $d\Omega^2$ being exactly $r^2$ is *equivalent to* the statement that the sphere at fixed coordinate $r$ has area $4\pi r^2$ — the ordinary Euclidean formula.

## Areal radius, precisely

That equivalence is worth naming, because it is about to become nontrivial. Define: a radial coordinate $r$ is an **areal radius** if the sphere it labels (fixed $r$, all $\theta,\phi$) has surface area exactly $4\pi r^2$. In flat space this is automatic — it's just the ordinary radius, and there's nothing to distinguish it from "distance from the center" since $\int_0^r dr' = r$ measures both the coordinate label and the radial proper distance identically.

The reason this tutorial insists on the distinction is that once the spatial geometry stops being flat (once a mass is present and $B(r)\ne1$ in the general ansatz $ds^2=-Ac^2dt^2+Bdr^2+r^2d\Omega^2$), these two notions of "radius" **split apart**. The coordinate $r$ appearing in the metric is *defined* — by convention, by construction — to be whichever radial label makes the angular part come out to exactly $r^2d\Omega^2$; that is what "areal coordinates" means, and it is a coordinate *choice*, not an automatic geometric fact once curvature is present. The radial *proper distance* from the origin to a sphere of areal radius $r$ is instead $d\ell = \sqrt{B(r')}\,dr'$ integrated from $0$ to $r$ — and if $B\ne1$, that integral will *not* equal $r$. So: "areal radius $r$" means precisely "the label such that a sphere at fixed $r$ has area $4\pi r^2$" — full stop, nothing about proper distance from the center is implied by that label alone. [`SYM1`](./sym1-static-spherical.md) uses exactly this coordinate for the entire $A_\lambda$ construction; [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md) later shows the same spacetime rewritten with a genuinely different radial coordinate (isotropic), where the angular coefficient is *not* simply (new radius)$^2$.

## Flat bookkeeping, not curvature

One more thing worth being explicit about, since it will matter once curvature is discussed ([`F7`](./f7-curvature.md)): writing $r^2d\Omega^2$ in the *flat*-space metric above does **not** mean flat space is curved. It is purely spherical bookkeeping — an artifact of choosing a coordinate grid adapted to spheres rather than to Cartesian axes. Whether the underlying geometry is actually curved is a separate question, entirely about whether $A(r)$ and $B(r)$ depart from $1$ — the angular part $r^2d\Omega^2$ looks the same (given areal $r$) whether or not gravity is present.

## Simpler on-ramp

Think of the Earth's surface, described by latitude and longitude. A circle of constant latitude near the equator is large; one near the pole is small — the *radius* of that circle (its distance, measured along the surface, from the pole) doesn't simply equal some fixed multiple of latitude in general, once you account for the sphere's curvature. Areal radius is the analogous idea turned around: instead of asking "how far away is this sphere, measured with a ruler," we *define* the radial label by asking "how big is this sphere's *area*," and back out an $r$ from that area via the familiar $4\pi r^2$ formula. In flat space, that areal label and the ruler-measured distance from the center happen to agree — which is exactly why the distinction is invisible until you meet a genuinely curved spatial slice, where the two can disagree.

## Check your understanding

1. What does it mean, precisely, for $r$ to be an "areal" radial coordinate?
2. In flat space, why do areal radius and radial proper distance from the origin coincide?
3. If a metric's spatial part is $B(r)dr^2 + r^2d\Omega^2$ with $B\ne1$, is the proper distance from the origin to the sphere at coordinate $r$ equal to $r$? Why or why not?
4. Does writing the metric with an $r^2d\Omega^2$ term, by itself, tell you whether the space is curved?

<details>
<summary>Answers</summary>

- **1.** That the sphere at fixed coordinate value $r$ has surface area exactly $4\pi r^2$ — the ordinary Euclidean sphere-area formula, taken as the *definition* of what that coordinate label means.
- **2.** Because in flat space $B(r)=1$, so radial proper distance $\int_0^r \sqrt{B}\,dr' = \int_0^r dr' = r$ exactly equals the coordinate label.
- **3.** No, not in general — proper distance is $\int_0^r\sqrt{B(r')}\,dr'$, which differs from $r$ whenever $B\ne1$ anywhere along the path. The coordinate label ($r$, tied to area) and the radial ruler-distance are two different things once $B\ne1$.
- **4.** No. $r^2d\Omega^2$ is just the standard spherical bookkeeping for the angular directions; it appears in flat space too (this tutorial). Whether the geometry is curved depends on whether $A(r)$ and $B(r)$ (or their flat-space values $1$) depart from their flat values — not on the presence of the angular term itself.

</details>

## What the paper claims here

Grounds §2 exactly: "$r$ = areal radius (sphere at fixed $r$ has area $4\pi r^2$)." The entire ansatz $ds^2=-A(r)c^2dt^2+B(r)dr^2+r^2d\Omega^2$ is written in this specific coordinate choice, and the paper is explicit that this choice matters — the flux postulate (I2), grounded in [`GAUSS1`](./gauss1-flux-laplacian.md), is stated as coordinate-dependent precisely *because* it is written using this areal $r$; a different radial coordinate (e.g. isotropic, [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md)) would yield a different-looking flux law for the same physical geometry.

---
**Path navigation:** ← [prev in default path](./f3-special-relativity.md) · [next: F5 — Geodesics](./f5-geodesics.md) →
**See also:** [SYM1](./sym1-static-spherical.md), [PPN2](../part6-ppn-observation/ppn2-areal-isotropic.md), [PG1](../part7-michell-pg/pg1-painleve-gullstrand.md)
