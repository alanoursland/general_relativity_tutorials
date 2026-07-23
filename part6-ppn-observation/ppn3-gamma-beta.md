# $\gamma=1$, $\beta=\lambda+2$

> **Tutorial `PPN3`** · Part 6 · **Goal:** Derive the family's PPN parameters and the punchline identity $\lambda=\beta-2$ · **Prereqs:** [PPN2](./ppn2-areal-isotropic.md)

**Where this sits in the arc.** This is the second selector, and the one that works. `CORE2` revealed $\lambda$ as a closure choice in the flux law — a piece of representational freedom, not a fact about geometry. This tutorial shows that the very same constant $\lambda$ reappears, untouched, as the coefficient of the quadratic term in the PPN metric: $\beta=\lambda+2$. That means *measuring* $\beta$ is *measuring* $\lambda$, directly, without needing any of Part V's energy-accounting conventions. `PPN4`–`PPN6` turn this identity into an actual number.

## The spatial part: $\gamma=1$, for every $\lambda$

`PPN2` derived the conformal factor to first order in $w=r_s/\rho$:
$$\frac{r^2}{\rho^2} = 1 + w + O(w^2).$$
Since $w = r_s/\rho = 2GM/(c^2\rho) = 2U$, this is
$$\frac{r^2}{\rho^2} = 1 + 2U + O(U^2).$$
The isotropic spatial metric is $g_{ij} = (r^2/\rho^2)\delta_{ij} = (1+2U+O(U^2))\delta_{ij}$. Comparing with the PPN form $(1+2\gamma U+O(U^2))\delta_{ij}$ term by term gives
$$\boxed{\gamma = 1}.$$
Nothing here depended on $a_2$ (equivalently on $\lambda$): `PPN2` showed the first-order transformation coefficient $k_1=1/2$ is fixed purely by first-order matching, before the nonlinear coefficient $a_2$ ever enters. So *every* member of the family — Schwarzschild, the exponential member, the reciprocal member, all of them — has exactly the GR value $\gamma=1$. Light bending and Shapiro delay, which depend only on $\gamma$ (`PPN4`), cannot distinguish any member of this family from any other, or from GR.

## The temporal part: $\beta = \lambda + 2$

Now use the second-order piece of the coordinate transformation, $x = w - \tfrac12 w^2 + O(w^3)$ (from `PPN2`, using $k_1=1/2$), and substitute it into the areal time coefficient $A(r) = 1-x+a_2x^2+O(x^3)$:
$$x^2 = \left(w-\tfrac12w^2\right)^2 = w^2 + O(w^3),$$
$$A(\rho) = 1 - \left(w-\tfrac12w^2\right) + a_2 w^2 + O(w^3) = 1 - w + \left(a_2+\tfrac12\right)w^2 + O(w^3).$$
Substitute $w=2U$:
$$A(\rho) = 1 - 2U + 4\left(a_2+\tfrac12\right)U^2 + O(U^3).$$
Compare with the PPN form $A_{\rm PPN} = 1-2U+2\beta U^2 + O(U^3)$:
$$2\beta = 4\left(a_2+\tfrac12\right) \implies \beta = 2a_2+1.$$
Now use `WEAK1`'s $a_2 = (1+\lambda)/2$:
$$\beta = 2\cdot\frac{1+\lambda}{2}+1 = (1+\lambda)+1,$$
$$\boxed{\beta = \lambda+2}, \qquad \text{equivalently} \qquad \boxed{\lambda = \beta - 2}.$$

Check against the distinguished members: Schwarzschild ($\lambda=-1$) gives $a_2=0$, hence $\beta=1$ — the GR value, as it must. The exponential member ($\lambda=0$) gives $\beta=2$; the reciprocal member ($\lambda=+1$) gives $\beta=3$.

## The punchline

The constant $\lambda$ was introduced in `CORE2` purely as the closure coefficient of a flux equation, $\Delta s = \lambda(s')^2$ — a statement about which potential variable happens to obey an exact vacuum Gauss law, chosen with no reference to observation at all. That same number, unchanged, is exactly the PPN nonlinearity $\beta-2$. This is not a coincidence of algebra to be shrugged off: it says that the representational choice made deep in the construction of the family — which variable's flux is exactly conserved — has a direct, measurable observational shadow in the *nonlinear* structure of the metric far from the source, in a regime (the solar system) that has nothing to do with how the metric was built. Measuring $\beta$ pins down $\lambda$ without ever touching a matter/field energy-splitting convention of the kind Part V needed. This is why PPN succeeds where the static-accounting selector failed: it reads off a genuinely metric fact ($\beta$), not a choice of how to divide energy between matter and field.

It is worth being precise about what the identity does and doesn't say. $\beta=\lambda+2$ is an exact relation between the *closure constant* and the *leading nonlinear PPN coefficient*; it says nothing by itself about whether two members' full metrics agree beyond this order, nor does it retroactively justify (I2)'s flux postulate as physically necessary — it simply reports what that postulate, once adopted, predicts for $\beta$.

## Picturing Figure 2

The paper's Figure 2 plots $\beta$ against $\lambda$: since $\beta=\lambda+2$, this is a straight line of unit slope, shifted up by 2 — nothing curved, nothing subtle, just the exact algebraic identity just derived. A shaded vertical strip marks $\lambda\in[-\tfrac14,\tfrac14]$ (`ACC4`'s accounting interval), which on the $\beta$-axis lands at $\beta\in[\tfrac74,\tfrac94]$ — comfortably away from $\beta=1$. Shuler's two extra members sit at $\lambda=\pm\tfrac12$, i.e. $\beta=\tfrac32,\tfrac52$. The observationally selected point, $\lambda=-1 \Leftrightarrow \beta=1$, sits on the line far from both the shaded strip and the Shuler points. An inset zooms in on that point to show the tiny band $|\beta-1|\lesssim10^{-4}$ that current solar-system data actually allow (`PPN6`) — at the scale of the main plot this band is effectively a single point, but it is the entire content of what observation has established.

## Simpler on-ramp

Recall from `CORE2` that $\lambda$ started life as an answer to the question "which quantity's flow through a sphere is exactly conserved in vacuum?" — a purely mathematical bookkeeping choice, made before anyone measured anything. What this tutorial shows is that if you instead go out and measure how strongly gravity's *own energy* curves spacetime around the Sun (the $\beta$ number), you get back exactly that same bookkeeping choice, via the simple rule "subtract 2." It's as if a choice you made about how to organize an equation on paper turned out to be directly readable off a telescope. That is what makes $\beta$ a genuine *selector*, unlike the energy-accounting story of Part V, which could only ever report on the accounting convention it started with.

## Check your understanding

- Why does $\gamma=1$ hold for *every* member of the family, rather than only for Schwarzschild?
- Which order of the areal-to-isotropic transformation ($k_1$ or $k_2$) is responsible for $\beta$ depending on $\lambda$, and why?
- In what precise sense is $\beta=\lambda+2$ *not* a claim that two members with different $\lambda$ agree at all orders?
- Why is the identity $\lambda=\beta-2$ a stronger selector than the Sec. 4 accounting bound, even though both are just numbers constraining $\lambda$?

**Answers**
- Because $\gamma$ comes from the first-order coordinate matching ($k_1=1/2$), and that matching is fixed before the nonlinear coefficient $a_2$ (equivalently $\lambda$) enters the calculation at all — it is order-of-magnitude too early in the expansion to see $\lambda$.
- $k_2 = (1-4a_2)/16$, the second-order coefficient, is the one that carries $a_2$ (hence $\lambda$) into the transformation, and it is this order-$w^2$ information, fed into $A(\rho)$, that produces the $\lambda$-dependence of $\beta$.
- The relation is exact only for the coefficient of $U^2$ in $g_{tt}$; it says nothing about $O(U^3)$ or higher terms, or about the spatial metric beyond $\gamma=1$, so two members can (and do) differ at higher post-Newtonian order even though this identity is exact at 1PN.
- The accounting bound (`ACC4`) is conditional on a matter/field energy-splitting convention that is itself an assumption ($0\le f\le1$), not a measurement; $\beta=\lambda+2$ is a metric fact with no such convention built in — $\beta$ is something a clock and a light ray can directly probe.

## What the paper claims here

Grounded in Sec. 5.1.1–5.2: the derivation of $\gamma=1$ from the conformal factor $r^2/\rho^2=1+w+O(w^2)$, the derivation of $\beta=2a_2+1=\lambda+2$ from $A(\rho)=1-2U+4(a_2+\tfrac12)U^2$, and the explicit statement that "the relation $\beta=\lambda+2$ is exact as a relation between $\lambda$ and the 1PN coefficient; [it] doesn't imply full metrics agree/differ only at that order." The description of Figure 2 (the $\beta$-vs-$\lambda$ line, the shaded Sec. 4 strip, the Shuler points, the inset) follows Sec. 5.6's caption description; the book is figure-free, so it is rendered here in prose per the book's convention.

---
**Path navigation:** ← [prev in default path](./ppn2-areal-isotropic.md) · [next](./ppn4-classical-tests.md) →
**See also:** [CORE2](../part3-building-the-family/core2-log-variable-closure.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [ACC4](../part5-energy-accounting/acc4-matter-conventions-bound.md), [PPN5](./ppn5-perihelion-precession.md)
