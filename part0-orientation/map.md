# The Big Picture in One Page

> **Tutorial `MAP`** · Part 0 · **Goal:** hold the entire argument — family, sign switch, three selectors, one thesis — in a single view · **Prereqs:** [`INTRO`](intro.md).

**Where this sits in the arc.** This is the map you return to whenever you lose the thread. It is deliberately spoiler-heavy: it states the destination so that each tutorial reads as a step toward something you already understand in outline. A returning reader re-enters the book here, at the right altitude.

## The one-line thesis

> **Static assumptions build a family of metrics; they do not select Schwarzschild. Extra information — a measurement, or a global kinematic demand — selects it.**

Everything below is the elaboration.

## 1. The family

Assume the exterior is **static**, **spherically symmetric**, and **asymptotically flat**, written in areal coordinates:

$$ds^2 = -A(r)\,c^2 dt^2 + B(r)\,dr^2 + r^2 d\Omega^2, \qquad A, B \to 1 \ \text{as}\ r\to\infty.$$

Then impose four ingredients (detailed in [`CORE0`](../part3-building-the-family/core0-four-assumptions.md)):

- **(I1)** a Newtonian weak-field limit, $A = 1 - r_s/r + O(r^{-2})$ with $r_s = 2GM/c^2$;
- **(I2)** a vacuum **flux law** $\Delta V = 0$ for *some* monotonic potential variable $V(A)$, where $\Delta = \frac{1}{r^2}\frac{d}{dr}(r^2\frac{d}{dr})$ is the flat-space radial flux operator — a **postulate**, not the Einstein equations;
- **(I3)** the reciprocal condition $A B = 1$ (i.e. $g_{tt}g_{rr} = -1$);
- **(I4)** a **constant** nonlinear coefficient in the closed flux equation.

The crux is that (I1)–(I3) do **not** close the system: the flux law never says *which* function of $A$ plays the role of $V$, and different choices give different nonlinear metrics that all agree at Newtonian order ([`CORE1`](../part3-building-the-family/core1-flux-freedom.md)). Introducing $s = \ln A$ and applying the chain rule to $\Delta V = 0$ gives $\Delta s = -\frac{F''}{F'}(s')^2$; the constant-coefficient postulate (I4) sets $-F''/F' = \lambda$, closing everything into

$$\boxed{\ \Delta s = \lambda\,(s')^2\ } \qquad\Longrightarrow\qquad \boxed{\ A_\lambda(r) = \left(1 + \lambda\,\frac{r_s}{r}\right)^{-1/\lambda}, \quad B_\lambda = A_\lambda^{-1}\ }$$

([`CORE2`](../part3-building-the-family/core2-log-variable-closure.md) through [`CORE4`](../part3-building-the-family/core4-classification-theorem.md)). This is a **classification theorem**: every constant-$\lambda$ member satisfies (I1)–(I4), and these are the only ones. Distinguished members ([`CORE5`](../part3-building-the-family/core5-distinguished-members.md)):

| $\lambda$ | exact-flux variable | $A_\lambda(r)$ | name |
|---|---|---|---|
| $-1$ | $A$ | $1 - r_s/r$ | **Schwarzschild** |
| $0$ | $\ln A$ | $e^{-r_s/r}$ | exponential (continuous bridge) |
| $+1$ | $1/A$ | $(1 + r_s/r)^{-1}$ | reciprocal |

The parameter $\lambda$ is, mathematically, *which potential variable you chose to make the flux law exact* — a **representation choice**, not a fact about gravity ([`EPI1`](../part8-synthesis/epi1-representation-vs-fact.md)). All members share the same Newtonian limit; they first differ at second order, where $A_\lambda = 1 - x + \frac{1+\lambda}{2}x^2 + O(x^3)$ with $x = r_s/r$ ([`WEAK1`](../part3-building-the-family/weak1-weak-field-degeneracy.md)).

**Why this doesn't contradict Birkhoff.** Birkhoff's theorem says static + spherical + *vacuum Einstein* forces Schwarzschild uniquely. The family evades it by **replacing the field equations with the weaker flux postulate (I2)**. For $\lambda \ne -1$ the members are *not* vacuum-Einstein solutions — feed them into real GR and the "vacuum" carries a nonzero effective stress–energy ([`GRSOL`](../part5-energy-accounting/grsol-are-these-gr-solutions.md), [`BIRK`](../part2-schwarzschild/birkhoff.md)).

## 2. The sign / horizon switch

Set $A_\lambda(r) = 0$: the base $1 + \lambda r_s/r$ vanishes at

$$r_0 = -\lambda\, r_s,$$

which is a *positive* radius **iff $\lambda < 0$** ([`ZERO1`](../part4-family-structure/zero1-finite-radius-zeros.md)). For $\lambda \ge 0$ the coefficient $A_\lambda$ stays positive at every finite $r>0$ (including $A_0 = e^{-r_s/r} > 0$). So the *sign of one parameter silently controls causal structure*: whether the geometry has a finite-radius surface where the static time coefficient vanishes. For Schwarzschild ($\lambda=-1$) that surface is at $r_s$ and is the **horizon**. For other negative $\lambda$ the paper establishes only that a zero exists — it does **not** classify its regularity or causal character, and refuses to call it a horizon without the invariant check ([`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md)).

## 3. The three selectors and their verdicts

Which member is real? Three candidate answers.

### Accounting → $[-\tfrac14, \tfrac14]$, **fails**
"Gravitational energy gravitates, so let the field's own energy fix $\lambda$." Read naively off the source equation this is **circular**: the field density was *defined* to make the equation take that form, so substitution returns it unchanged for every $\lambda$ — an identity, not a measurement ([`ACC1`](../part5-energy-accounting/acc1-circularity.md), the self-consistency lemma). The honest version uses a **convention-independent** operational quantity: quasi-statically assembling two thin shells extracts work $U = Gm_1m_2/b$, so the invariant interaction energy is $E_{\rm int} = -U$ ([`ACC2`](../part5-energy-accounting/acc2-invariant-assembly-energy.md)). Assigning a gradient-local field density $u_{\rm field} = \lambda\frac{c^4|\nabla s|^2}{8\pi G}$ gives a cross term $E_{\rm field,cross} = 4\lambda U$ ([`ACC3`](../part5-energy-accounting/acc3-field-cross-term.md)); balancing against a matter convention parameter $f \in [0,1]$ yields

$$\lambda = \frac{2f - 1}{4} \in \left[-\tfrac14, +\tfrac14\right]$$

([`ACC4`](../part5-energy-accounting/acc4-matter-conventions-bound.md)). This interval **excludes Schwarzschild** ($\lambda=-1$ would need $f = -\tfrac32$). But the bound is only as strong as the assumption $0 \le f \le 1$, which is a *modeling choice*, not a theorem: the total $-U$ is invariant, the matter–field split is a convention. So accounting does not truly select — it constrains a class of conventions ([`ACC6`](../part5-energy-accounting/acc6-energy-localization.md), [`EPI2`](../part8-synthesis/epi2-identities-not-measurements.md)).

### Observation → $\beta$ selects $\lambda = -1$
Transform to isotropic coordinates and read off the post-Newtonian parameters ([`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md), [`PPN3`](../part6-ppn-observation/ppn3-gamma-beta.md)):

$$\gamma = 1 \ \text{(all members)}, \qquad \boxed{\ \beta = \lambda + 2\ } \iff \lambda = \beta - 2.$$

Because $\gamma = 1$ throughout, light bending and Shapiro delay are **blind** to $\lambda$; the freedom lives entirely in $\beta$, which perihelion precession sees ([`PPN4`](../part6-ppn-observation/ppn4-classical-tests.md), [`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md)). The anomalous precession scales as $\frac{2+2\gamma-\beta}{3} = \frac{2-\lambda}{3}$; Mercury's $43''$/century forces $\lambda = -1$, and the accounting interval's members would give $\approx 25''$–$32''$ — *falsified*. Solar-system ranging gives $|\beta - 1| \lesssim 10^{-4}$, hence $|\lambda + 1| \lesssim 10^{-4}$: **Schwarzschild selected** to high precision ([`PPN6`](../part6-ppn-observation/ppn6-reading-constraints.md)). And since a zero exists iff $\lambda < 0$ iff $\beta < 2$, the same measurement that selects Schwarzschild implies a finite-radius zero exists ([`PPN7`](../part6-ppn-observation/ppn7-beta-and-horizon.md)).

### PG infall → $\lambda = -1$
Every member has a Painlevé–Gullstrand form with flat spatial slices and a "river" velocity $v_\lambda = c\sqrt{1 - A_\lambda}$ ([`PG1`](../part7-michell-pg/pg1-painleve-gullstrand.md)); the curvature has moved into the mixed $2v\,dr\,dT$ term ([`PG2`](../part7-michell-pg/pg2-where-did-curvature-go.md)). Demand that the infall match the exact Newtonian relation $\tfrac12 v^2 = GM/r$ — i.e. $v^2 = 2GM/r$ — at *every* radius, not just asymptotically. This requires $1 - A_\lambda = r_s/r$, i.e. $A_\lambda = 1 - r_s/r$, i.e. **$\lambda = -1$ alone** ([`PG3`](../part7-michell-pg/pg3-newtonian-infall.md)). This is a global condition strictly stronger than the Newtonian limit. It also **explains Michell** (1784): his escape-velocity number $r = 2GM/c^2$ is a downstream property of the already-selected Schwarzschild geometry, read correctly only in this representation — not a valid metric derivation ([`HIST1`](../part7-michell-pg/hist1-michell-laplace.md)).

## 4. The synthesis

- **[`SYN1`](../part8-synthesis/syn1-century-of-shortcuts.md)** — every historical "simple derivation," sorted into *builds the family* vs. *selects a member*, and what each adds.
- **[`EPI1`](../part8-synthesis/epi1-representation-vs-fact.md)** — $\lambda$ as a gauge/closure choice; what coordinates preserve and what they hide.
- **[`EPI2`](../part8-synthesis/epi2-identities-not-measurements.md)** — the transferable lesson: a definition can beg the question; an identity can constrain nothing.
- **[`EPI3`](../part8-synthesis/epi3-build-vs-select.md)** — how to audit *any* simple derivation.
- **[`OUT1`](../part8-synthesis/out1-self-coupling-bootstrap.md)** — beyond this paper: the dynamical self-coupling bootstrap that *does* force Schwarzschild from first principles.

## Simpler on-ramp

Picture a dial labeled $\lambda$. Turning it sweeps you through a whole shelf of possible "geometry outside a heavy ball" — one book per setting. The famous one, Schwarzschild, sits at $\lambda = -1$. The plain static assumptions build the shelf but leave the dial free. Turn it to any negative number and the geometry grows a special surface at radius $-\lambda r_s$; turn it to zero or positive and that surface disappears. Now three referees try to lock the dial. The first (energy bookkeeping) says "somewhere between $-\tfrac14$ and $+\tfrac14$" — and it is confident but leaning on a convention, and it misses $-1$ entirely. The second (measure Mercury's orbit) says "$-1$, essentially exactly." The third (insist that falling matches Newton at every distance) also says "$-1$." Two referees agree and one is honestly overruled — and the one that failed teaches you the most about how arguments smuggle in their conclusions.

## Check your understanding

1. What single algebraic feature of $A_\lambda$ decides whether a finite-radius zero exists, and for which sign of $\lambda$?
2. Why can't light-bending measurements distinguish members of the family?
3. The accounting selector gives $[-\tfrac14,\tfrac14]$ and observation gives $\lambda\simeq-1$. These disagree. Is this a contradiction?
4. In what precise sense is $\lambda$ a "representation choice"?

<details>
<summary>Answers</summary>

- **1.** The base $1 + \lambda r_s/r$; it hits zero at $r_0 = -\lambda r_s$, positive iff $\lambda < 0$.
- **2.** Light bending and Shapiro delay depend on $\gamma$, and $\gamma = 1$ for every member; the family's freedom lives in $\beta$, which only perihelion precession sees at leading post-Newtonian order.
- **3.** No. They are *different information about the same parameter*. Accounting constrains a class of energy-localization conventions (and is convention-bound); observation is a direct measurement. The measurement wins and, in doing so, falsifies the interval those conventions produced.
- **4.** $\lambda = -F''/F'$ encodes *which* function $V = F(s)$ of the potential was chosen to make the flux law $\Delta V = 0$ exact. That is a choice of description, not a physical input; it becomes physical only when tied to $\beta$ or to the infall condition.

</details>

## What the paper claims here

This page grounds the paper's Abstract, §1, and §7–8. Faithful statement of scope: the family is complete and unique *relative to* (I1)–(I4); it recovers $r_s$ and contains Schwarzschild without selecting it; for $\lambda < 0$ only the *existence* of a finite positive-radius zero is established, called a horizon only at $\lambda=-1$; the §4 accounting bound is *conditional* on the convention $0 \le f \le 1$ and "concerns the split, not energy conservation"; the observational selection is stated at order-of-magnitude honesty with its assumptions ($|\beta-1|\lesssim 10^{-4}$, using a restricted PPN relation). The paper does **not** establish that off-Schwarzschild members are physically sensible (geodesic completeness, energy conditions) — that is deliberately bracketed.

---
**Path navigation:** ← [INTRO](intro.md) · [next: F1 — What is a metric?](../part1-foundations/f1-metric.md) →
**See also:** [`CORE0`](../part3-building-the-family/core0-four-assumptions.md), [`SYN1`](../part8-synthesis/syn1-century-of-shortcuts.md), [`EPI3`](../part8-synthesis/epi3-build-vs-select.md), [path chooser](intro.md#the-path-chooser), [notation](../reference/notation.md)
