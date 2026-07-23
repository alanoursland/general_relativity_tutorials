# The vacuum Einstein equations (lightweight)

> **Tutorial `S1`** · Part 2 · **Goal:** State $G_{\mu\nu}=0$ in vacuum and say precisely what it constrains, without a full course in general relativity. · **Prereqs:** [F7](../part1-foundations/f7-curvature.md), [SYM1](../part1-foundations/sym1-static-spherical.md)

**Where this sits in the arc.** Part III's family is built from a *postulated flux law*, not from Einstein's equations. To see exactly what gets replaced, and by how much weaker a condition, you need to know what the real field equations say — that is the entire purpose of this tutorial and the next.

## What the equations say

General relativity's field equation relates the curvature of spacetime to the matter and energy present in it:

$$G_{\mu\nu} = \frac{8\pi G}{c^4}\,T_{\mu\nu}.$$

The right side, the stress–energy tensor $T_{\mu\nu}$, is a bookkeeping device for energy density, momentum density, and stress (pressure, shear) at each point — the "sources." The left side, the Einstein tensor $G_{\mu\nu} = R_{\mu\nu} - \tfrac12 R\,g_{\mu\nu}$, is built entirely from the metric $g_{\mu\nu}$ and its first and second derivatives: $R_{\mu\nu}$ is the Ricci tensor (a contraction of the Riemann curvature tensor introduced in `F7`) and $R = g^{\mu\nu}R_{\mu\nu}$ is the Ricci scalar. This book does not re-derive the field equations from an action principle or from the equivalence principle plus covariance — that derivation belongs to a full GR course. Here we simply *use* the equation, the way you would use Maxwell's equations without re-deriving them from charge conservation and gauge invariance every time.

The essential fact about $G_{\mu\nu}$ that matters for everything downstream: it is a genuinely *covariant* object. Its ten independent components (symmetric $4\times4$ tensor) are built the same way in every coordinate system, out of the metric and its derivatives, by a fixed geometric prescription. Nothing about $G_{\mu\nu}$ depends on which coordinates you happened to choose to write the metric down. That will matter enormously when we contrast it with the paper's flux postulate.

## The vacuum case

"Vacuum" means no matter or energy at the spacetime point in question: $T_{\mu\nu}=0$ there. The field equation then reduces to

$$G_{\mu\nu} = 0.$$

Taking the trace of $G_{\mu\nu}=0$ (contract both sides with $g^{\mu\nu}$) gives $R - 2R = 0$, i.e. $R=0$. Feeding that back into $G_{\mu\nu}=R_{\mu\nu}-\tfrac12 Rg_{\mu\nu}=0$ collapses it to the cleaner statement

$$R_{\mu\nu} = 0,$$

called *Ricci-flat*. This is the vacuum Einstein equation in its most-used form: ten coupled, second-order, nonlinear partial differential equations for the ten independent components of $g_{\mu\nu}$.

Ricci-flat does **not** mean flat. The full Riemann tensor has more independent components than the Ricci tensor; the piece of curvature that Ricci flatness leaves untouched is called the Weyl tensor, and it can be nonzero even when $R_{\mu\nu}=0$ everywhere. Physically, this is the curvature that produces tidal stretching and squeezing — exactly the kind of curvature a planet or a black hole imprints on the empty space around it. If $R_{\mu\nu}=0$ forced flatness, there would be no gravity outside a star at all. It is precisely because Ricci-flat spacetimes can be curved that $G_{\mu\nu}=0$ has a nontrivial solution describing the field around a mass — worked out in full in `S2`.

## What it constrains, concretely

For a general metric, $R_{\mu\nu}=0$ is ten equations in ten unknown functions of four coordinates — intractable without simplifying the metric first. Restricting to a static, spherically symmetric, asymptotically flat ansatz (built up in `SYM1`),

$$ds^2 = -A(r)\,c^2dt^2 + B(r)\,dr^2 + r^2 d\Omega^2,$$

collapses the unknowns to just two functions of one variable, $A(r)$ and $B(r)$. Plugging this ansatz into $R_{\mu\nu}=0$ produces a small, solvable system of ordinary differential equations relating $A$, $B$, and their derivatives. That system — and its unique solution — is the content of `S2`.

## Simpler on-ramp

Think of Newtonian gravity's field equation in empty space, $\nabla^2\Phi = 0$ (Laplace's equation): away from any mass, the gravitational potential obeys a specific differential constraint, and once you fix boundary conditions (how $\Phi$ behaves at infinity and near the source), the solution is unique. $G_{\mu\nu}=0$ is the tensor-valued, relativistic descendant of that same idea: away from any mass or energy, spacetime's curvature obeys a specific differential constraint. It is a much richer equation — ten coupled equations for a whole metric instead of one equation for a single scalar potential — but it plays the same logical role: it is the "no sources here" law, and it is what actually pins down the shape of empty space around a star.

## Check your understanding

- Why does "vacuum" mean $T_{\mu\nu}=0$ rather than $g_{\mu\nu}=$ flat metric?
- Why doesn't $R_{\mu\nu}=0$ imply the Riemann tensor vanishes?
- In what sense is $G_{\mu\nu}$ "coordinate-independent" and why will that matter when comparing it to a postulated flux law?
- What does restricting to a static, spherically symmetric ansatz buy you, computationally?

**Answers**
- Vacuum is a statement about the source term, not the geometry; the whole point of solving $G_{\mu\nu}=0$ is to find out what (possibly curved) geometry is consistent with no local sources.
- The Ricci tensor is a particular contraction (trace) of the full Riemann tensor; the traceless remainder (the Weyl tensor) carries tidal curvature and is unconstrained by $R_{\mu\nu}=0$.
- $G_{\mu\nu}$ is built from the metric and its derivatives by a fixed geometric rule that transforms consistently under any change of coordinates — it is not tied to areal coordinates, isotropic coordinates, or any other choice, unlike a postulate stated in one specific radial variable.
- It reduces ten unknown functions of four spacetime coordinates to two unknown functions of one radial coordinate, turning ten coupled PDEs into a short, closed system of ODEs.

## What the paper claims here

The paper does not derive or restate the Einstein field equations at all — it is explicitly about what happens when you *replace* them with a weaker, coordinate-dependent flux postulate (I2). This tutorial exists purely as backdrop, so that the contrast in `CORE-CONTRAST` and the resolution of Birkhoff's theorem in `BIRK` are precise rather than hand-wavy. The negative-space fact this sets up: members of the paper's family with $\lambda\neq-1$ solve (I2), not $G_{\mu\nu}=0$; fed into the real field equations they produce a *nonzero* Einstein tensor, i.e. an effective stress–energy, even though the exterior is nominally "vacuum" in the paper's construction.

---
**Path navigation:** ← [prev in default path](../part1-foundations/ene1-self-energy.md) · [next](./s2-deriving-schwarzschild.md) →
**See also:** [F7](../part1-foundations/f7-curvature.md), [SYM1](../part1-foundations/sym1-static-spherical.md), [CORE-CONTRAST](../part3-building-the-family/core-contrast.md)
