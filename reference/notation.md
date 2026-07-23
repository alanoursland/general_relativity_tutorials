# Notation and Conventions Reference

> **Reference `notation`** · Quick-lookup page · **Goal:** one place to check any symbol, sign convention, or index convention used anywhere in the book. · **Prereqs:** none — consult any time; [F1](../part1-foundations/f1-metric.md) teaches these conventions in context.

**Where this sits in the arc.** This page has no place in the reading order — it is a lookup table, referenced from every tutorial rather than read start to finish. Return to it whenever a symbol surprises you; every convention here is fixed once, at the start, and used identically everywhere else in the book.

## Signature and $c$

- **Signature:** $(-,+,+,+)$, fixed throughout. A timelike interval has $ds^2<0$; spacelike, $ds^2>0$; null (light), $ds^2=0$. See [F1](../part1-foundations/f1-metric.md).
- **$c$ is always explicit.** The book never sets $c=1$. Every formula keeps factors of $c$ visible, both to match the source paper's own convention and because those factors mark exactly where relativistic corrections enter (e.g. $r_s=2GM/c^2$ vanishes in the formal $c\to\infty$ limit, cleanly separating Newtonian from relativistic content).
- **Coordinates:** $x^0\equiv ct,\ x^1,x^2,x^3$ spatial, so all four coordinates share units of length. Greek indices $\mu,\nu,\dots$ run $0..3$ (spacetime); where used, Latin indices $i,j,\dots$ run $1..3$ (space only). Einstein summation convention: a repeated index is summed over. See [F1](../part1-foundations/f1-metric.md), [F2](../part1-foundations/f2-tensors.md).

## The core symbol table

| Symbol | Meaning | Where introduced |
|---|---|---|
| $G$ | Newton's gravitational constant | — |
| $M$ | Mass of the central source | [F6](../part1-foundations/f6-newtonian-limit.md) |
| $\Phi = -GM/r$ | Newtonian potential | [F6](../part1-foundations/f6-newtonian-limit.md) |
| $r$ | **Areal** radial coordinate — sphere at fixed $r$ has area $4\pi r^2$ | [F4](../part1-foundations/f4-curvilinear-coordinates.md) |
| $A(r),\,B(r)$ | Metric functions: $ds^2=-Ac^2dt^2+Bdr^2+r^2d\Omega^2$ | [SYM1](../part1-foundations/sym1-static-spherical.md) |
| $r_s \equiv 2GM/c^2$ | Gravitational (mass) length scale, fixed by the Newtonian limit — *not* automatically a horizon radius | [F6](../part1-foundations/f6-newtonian-limit.md) |
| $x \equiv r_s/r$ | Dimensionless weak-field expansion parameter | [F6](../part1-foundations/f6-newtonian-limit.md) |
| $s \equiv \ln A$ | Logarithmic potential variable; the closure equation is written as $\Delta s = \lambda (s')^2$ | Part III |
| $\Delta \equiv \frac1{r^2}\frac{d}{dr}\!\left(r^2\frac{d}{dr}\right)$ | The **flat-space radial flux operator** in areal $r$. Explicitly **not** the Laplace–Beltrami operator of a curved slice, and **not** a covariant field equation | [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md) |
| $\lambda$ | The constant nonlinear closure coefficient (assumption I4); a representation choice, not a directly measured quantity, until PPN identifies it | Part III |
| $A_\lambda(r) = \left(1+\lambda\frac{r_s}{r}\right)^{-1/\lambda}$ | The one-parameter metric family; $B_\lambda = A_\lambda^{-1}$; Schwarzschild at $\lambda=-1$ | Part III |
| $U$ (PPN sense) | $U \equiv GM/(c^2\rho)$, the Newtonian potential written in the **isotropic** radial coordinate $\rho$ | Part VI |
| $U$ (assembly-energy sense) | $U \equiv Gm_1m_2/b$ — the *magnitude* of the two-shell interaction energy, $E_{\rm int}=-U$ | Part V |
| $\gamma$ | PPN parameter: spatial curvature per unit potential. All family members share $\gamma=1$ | Part VI |
| $\beta$ | PPN parameter: nonlinearity of the time–time metric term. $\beta = \lambda+2$ | Part VI |

**Disambiguating $U$:** the symbol $U$ carries two distinct meanings depending on context, matching the source paper's own (slightly overloaded) usage — always check which part of the book you're in. In Part V (energy accounting), $U$ is the *magnitude of a two-shell assembly energy*, $U=Gm_1m_2/b>0$. In Part VI (PPN), $U$ is the *dimensionless Newtonian potential in isotropic coordinates*, $U=GM/(c^2\rho)$. The two are related in spirit (both are dimensionless-or-energy expressions of "how deep a gravitational well") but are not the same variable and should not be conflated.

## Index conventions

- Superscript indices ($V^\mu$) denote vector components; subscript indices ($\omega_\mu$) denote one-form (covector) components. The metric $g_{\mu\nu}$ raises and lowers indices between the two. See [F2](../part1-foundations/f2-tensors.md).
- A prime ($'$) denotes an ordinary derivative with respect to $r$: $V'(r) \equiv dV/dr$. An overdot ($\dot{}$) denotes a derivative with respect to proper time $\tau$: $\dot x^\mu \equiv dx^\mu/d\tau$, used for geodesics ([F5](../part1-foundations/f5-geodesics.md)).
- $d\Omega^2 \equiv d\theta^2 + \sin^2\theta\,d\phi^2$, the metric of a unit 2-sphere.

## Simpler on-ramp

If you only remember three things from this page: (1) the minus sign always sits on the time part of the metric; (2) $c$ is never set to 1 — every formula keeps it visible; (3) $r$ means *areal* radius (defined by sphere area, $4\pi r^2$) unless a tutorial explicitly says otherwise (e.g. isotropic $\rho$ in Part VI). Everything else on this page is a lookup detail you can return to as needed.

## Check your understanding

1. Which sign in the metric is negative, and what physical distinction does that encode?
2. Why does the book never set $c=1$?
3. The symbol $U$ appears in both Part V and Part VI. Are these the same quantity?
4. What does the operator $\Delta$ in this book explicitly *not* mean?

<details>
<summary>Answers</summary>

- **1.** The time part, $g_{tt}$ (negative in this book's $(-,+,+,+)$ signature) — this is what lets $ds^2$ distinguish timelike, spacelike, and null separations.
- **2.** To match the source paper's own convention and to keep every formula's relativistic content dimensionally visible — factors of $c$ mark exactly where a correction is relativistic rather than Newtonian.
- **3.** No — in Part V it is the magnitude of a two-shell assembly energy, $Gm_1m_2/b$; in Part VI it is the dimensionless isotropic-coordinate Newtonian potential, $GM/(c^2\rho)$. Same letter, genuinely different quantities; always check context.
- **4.** It is explicitly *not* the Laplace–Beltrami operator of a curved spatial slice, and *not* the spacetime wave operator — it is the ordinary flat-space radial flux operator, applied (as a postulate) in the areal coordinate.

</details>

## What the paper claims here

This page collects, in one place, the notation the source paper itself fixes and uses throughout — signature and explicit $c$ are the book's own editorial choices made to match the paper's discipline; every other symbol ($r_s$, $x$, $s$, $\Delta$, $A_\lambda$, $U$ in both senses, $\gamma$, $\beta$) is used with exactly the paper's own definition, given in full where each is first introduced (§2 for $r_s,x,s,\Delta,A_\lambda$; §4 for the assembly-energy $U$; §5 for the PPN $U,\gamma,\beta$).

---
**Path navigation:** ← back to [MAP](../part0-orientation/map.md) · onward into Part I: [F1 — What is a metric?](../part1-foundations/f1-metric.md)
**See also:** [F1](../part1-foundations/f1-metric.md), [F6](../part1-foundations/f6-newtonian-limit.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md), [CORE0](../part3-building-the-family/core0-four-assumptions.md), [PPN1](../part6-ppn-observation/ppn1-ppn-formalism.md)
