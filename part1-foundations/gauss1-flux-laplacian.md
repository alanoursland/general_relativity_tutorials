# Gauss's Law, Flux, and the Radial Laplacian

> **Tutorial `GAUSS1`** · Part 1 · **Goal:** derive the flat-space radial flux operator $\Delta=\frac1{r^2}\frac{d}{dr}(r^2\frac{d}{dr})$, see why it forces field strength $\propto1/r^2$, and fix an explicit caveat: this is *not* the Laplace–Beltrami operator of a curved slice. · **Prereqs:** [F1](./f1-metric.md), [F4](./f4-curvilinear-coordinates.md).

**Where this sits in the arc.** This tutorial *is* assumption (I2) — the exact vacuum flux law the paper postulates in the areal potential variable, and one half of the mechanism (together with the closure (I4), [`CORE2`](../part3-building-the-family/core2-log-variable-closure.md)) that generates the entire one-parameter family. The caveat this tutorial insists on — that $\Delta$ is a flat-space bookkeeping operator, not a covariant field equation — is exactly why (I2) is called a *postulate* rather than a consequence of general relativity.

## The idea: flux conservation in a source-free region

In ordinary flat 3-space, consider a scalar field $V(r)$, spherically symmetric, with no sources (no mass, no charge) in some region. Gauss's law says: the total flux of $\nabla V$ through *any* sphere enclosing no sources is the same, regardless of the sphere's radius. Physically, this is just "nothing is being created or destroyed in between" — whatever flows out through a small sphere must flow out through a larger one too, since none of it is absorbed or generated along the way.

## Writing the flux explicitly

By spherical symmetry, $V$ depends only on $r$, so $\nabla V = V'(r)\,\hat r$, pointing radially with the same magnitude everywhere on a sphere of fixed $r$. The flux through a sphere of radius $r$ is then simply the field strength times the sphere's area (from [`F4`](./f4-curvilinear-coordinates.md), exactly $4\pi r^2$ for the areal radius):

$$\Phi_{\rm flux}(r) = \oint \nabla V \cdot d\mathbf{A} = 4\pi r^2\, V'(r).$$

"No sources in this region" means this flux is the *same number* at every $r$ within it — i.e. $4\pi r^2 V'(r) = \text{const}$.

## The radial operator

That flux-conservation statement is exactly the vacuum Laplace equation restricted to a radial function. Differentiating the constancy condition, $\frac{d}{dr}\big(4\pi r^2 V'(r)\big) = 0$, and dividing by the (nonzero) constant $4\pi$:

$$\frac{d}{dr}\left(r^2\frac{dV}{dr}\right) = 0.$$

Define the operator this expression is built from:

$$\boxed{\Delta V \equiv \frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{dV}{dr}\right)}.$$

This is exactly the ordinary Laplacian $\nabla^2 V$ of flat 3-space, restricted to functions depending on $r$ alone (the familiar radial part of the spherical-coordinates Laplacian from vector calculus) — the divergence of a purely radial vector field $f(r)\hat r$ is $\frac{1}{r^2}\frac{d}{dr}(r^2 f)$, and setting $f=V'(r)$ recovers the boxed operator directly. "Vacuum flux conservation" and "$\Delta V=0$" are the same statement.

## Solving $\Delta V = 0$: field strength $\propto 1/r^2$

The flux-conservation condition $4\pi r^2 V'(r) = \text{const} \equiv -4\pi K$ integrates immediately:

$$V'(r) = -\frac{K}{r^2} \quad\Longrightarrow\quad V(r) = V_\infty - \frac{K}{r},$$

for two integration constants $V_\infty$ (the value at infinity) and $K$ (fixed, physically, by the source's strength). This is the entire content of "$\Delta V=0$": the field strength $V'(r)$ falls off as exactly $1/r^2$, and the potential itself as $1/r$ — the familiar inverse-square law of Newtonian gravity (or Coulomb's law), rederived here from nothing but "no sources, and spherical symmetry" — no differential equation of motion, no calculus of variations, just flux bookkeeping.

## The caveat, stated as sharply as the paper states it

This is the single most important thing to carry out of this tutorial, and the paper is explicit and insistent about it: **the operator $\Delta$ derived above is the ordinary radial Laplacian of *flat* 3-space, computed using the literal Euclidean radial coordinate.** It is emphatically **not**:

- the wave operator (d'Alembertian) of the full 4-dimensional spacetime, and
- **not** the Laplace–Beltrami operator you would get by doing the analogous flux calculation on a *genuinely curved* spatial slice — i.e., one that properly accounts for a non-trivial radial metric coefficient $B(r)\ne1$ in the volume and area elements used to define flux and divergence there.

When the paper later *postulates* (I2) that some potential variable $V(A)$ built from the metric obeys this exact same operator, $\Delta V=0$, even in the curved geometry sourced by the mass itself, that is a **nontrivial, additional assumption** — a specific choice of bookkeeping in the areal coordinate — not a rederivation of a genuine field equation on the true curved slice, and not a consequence of Einstein's equations. A different choice of radial coordinate (say, isotropic, [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md)) would produce a genuinely different-looking flux condition for the same physical geometry. This coordinate-dependence is exactly why the paper insists on calling (I2) a **postulate**, not a covariant field equation.

One more piece of freedom worth flagging here explicitly, because it drives the entire construction in Part III: this flux law, by itself, does **not** say *which* function of $A$ plays the role of $V$. Imposing $\Delta A=0$, $\Delta(\ln A)=0$, or $\Delta(1/A)=0$ are three different conditions on $A(r)$ — each perfectly consistent with everything derived in this tutorial, and each agreeing with every other choice only at leading (Newtonian) order. Pinning down *which* variable closes the flux law is exactly the job of assumption (I4), taken up in [`CORE1`](../part3-building-the-family/core1-flux-freedom.md)/[`CORE2`](../part3-building-the-family/core2-log-variable-closure.md).

## Simpler on-ramp

Picture water flowing steadily outward from a source, with no leaks and no extra water joining in along the way. Draw any two concentric spherical shells around the source: however much water crosses the inner shell per second must also cross the outer one per second — none of it vanishes in between. Since the outer shell has more surface area, the same total flow spreads thinner over it, so the flow *per unit area* — the field strength — must fall off exactly as $1/(\text{area}) \propto 1/r^2$. The caveat, in the same picture: this bookkeeping assumes you're measuring shell areas with an ordinary flat ruler. If the space between the shells were itself stretched or warped, "area" and "distance" would no longer relate to each other in the simple $4\pi r^2$ way, and the flow-per-area calculation would look different. The paper's postulate is to keep using the flat-ruler bookkeeping anyway, as a deliberate simplifying choice — not because it's automatically still true once the space is curved.

## Check your understanding

1. Why does "no sources in a region" translate into "flux through any enclosing sphere is the same number"?
2. Solve $\Delta V=0$ from scratch: what functional form must $V(r)$ take, and how many free constants does it have?
3. Why is $\Delta$, as derived here, *not* automatically the correct operator to use once the spatial geometry is curved?
4. Does the flux law $\Delta V=0$, by itself, tell you which function of $A$ should play the role of $V$?

<details>
<summary>Answers</summary>

- **1.** Because flux measures the net outward flow through a closed surface, and with no sources or sinks inside, whatever crosses one enclosing sphere must equal what crosses any other enclosing sphere — nothing is created or absorbed in the source-free region between them.
- **2.** $V(r) = V_\infty - K/r$, with two free constants: $V_\infty$ (the asymptotic value) and $K$ (set by the source strength) — directly from integrating $4\pi r^2 V'(r)=\text{const}$ twice.
- **3.** Because $\Delta$ was built assuming flat-space Euclidean area/volume elements (literally $4\pi r^2$ for a sphere's area); a genuinely curved spatial slice has a different relationship between coordinate radius and proper area/volume (via the metric coefficient $B(r)$), so the true, covariant flux operator there (the Laplace–Beltrami operator) is a different, more complicated expression — $\Delta$ as derived here is only its flat-space special case.
- **4.** No. The flux law constrains whichever variable $V$ you apply it to, but leaves entirely open *which* function of $A$ that variable should be — $V=A$, $V=\ln A$, and $V=1/A$ are all consistent choices at this stage, and they lead to different metrics once the closure (I4) is applied.

</details>

## What the paper claims here

Grounds §2 (I2) directly, quoting closely: "there exists monotonic $V(A)$ with $\Delta V = \frac{1}{r^2}\frac{d}{dr}(r^2\frac{dV}{dr})=0$... This $\Delta$ is the ordinary radial flux operator from areal $r$, NOT the wave operator or Laplace–Beltrami of a curved slice. The flux law is a POSTULATE, not a covariant field equation and not a consequence of the Einstein equations." The paper is equally explicit that the flux law alone does not specify which function of $A$ plays the role of $V$ — exact flux laws for $A$, for $\ln A$, for $1/A$ give different nonlinear metrics, though all agree at Newtonian order.

---
**Path navigation:** ← [prev in default path](./f7-curvature.md) · [next: ENE1 — Newtonian gravitational potential energy & self-energy](./ene1-self-energy.md) →
**See also:** [CORE1](../part3-building-the-family/core1-flux-freedom.md)
