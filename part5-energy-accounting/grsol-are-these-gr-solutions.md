# Are these even GR solutions?

> **Tutorial `GRSOL`** · Part 5 · **Goal:** Establish the paper's true logical status — for $\lambda\ne-1$ the members are *not* vacuum-Einstein solutions; feeding $A_\lambda$ into real GR yields a nonzero Einstein tensor (an effective stress-energy). They solve a *postulated flux law*, not $G_{\mu\nu}=0$. · **Prereqs:** [CORE4](../part3-building-the-family/core4-classification-theorem.md), [BIRK](../part2-schwarzschild/birkhoff.md), [S1](../part2-schwarzschild/s1-vacuum-einstein.md)

**Where this sits in the arc.** A load-bearing correction to a natural misreading. The book has built a one-parameter *family of exterior metrics*, and it is tempting to hear "a family of vacuum solutions of general relativity." That is false, and the falsehood is the key to the paper's logical standing. Only $\lambda=-1$ solves the Einstein vacuum equations; the rest solve a *weaker postulate*. This is what makes the family compatible with Birkhoff's uniqueness theorem, and it is what the underdetermination story is really about.

## What the family actually solves

Go back to the construction. The metrics
$$A_\lambda(r)=\Big(1+\lambda\frac{r_s}{r}\Big)^{-1/\lambda}, \qquad B_\lambda=A_\lambda^{-1},$$
were obtained by imposing four assumptions ([CORE0](../part3-building-the-family/core0-four-assumptions.md)), of which the engine was **(I2), the areal-coordinate flux law**:
$$\Delta V = \frac{1}{r^2}\frac{d}{dr}\Big(r^2\frac{dV}{dr}\Big)=0 \quad\text{for some monotonic } V(A).$$
Read the paper's own description of this object carefully. $\Delta$ is the **flat-space radial flux operator** built from the areal radius $r$ — *not* the Laplace–Beltrami operator of the curved slice, and *not* any component of the Einstein tensor. The flux law is a **postulate**: a demand that some potential variable obey a Newton-style Gauss law. It is explicitly **not** the Einstein vacuum equation, not a covariant field equation, and not a consequence of $G_{\mu\nu}=0$.

So the family is a family of solutions of **(I2)**, not of the Einstein equations. The two coincide at exactly one value of $\lambda$.

## Only $\lambda=-1$ is a vacuum-Einstein solution

At $\lambda=-1$ the essential variable is $A$ itself and the flux law reads $\Delta A=0$, giving $A_{-1}=1-r_s/r$ — the Schwarzschild metric, which *does* solve $G_{\mu\nu}=0$. For every other $\lambda$, the flux law closes on a *different* variable ($A^{-\lambda}$, or $\ln A$ at $\lambda=0$), and the resulting metric is Schwarzschild-like only at Newtonian order; it differs at $O(x^2)$ ([WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md)).

Now do the test the paper's negative space demands. Take any $\lambda\ne-1$, form the metric $(A_\lambda,B_\lambda)$, and compute its **Einstein tensor** $G_{\mu\nu}$ honestly — the way you would for any metric in GR ([S1](../part2-schwarzschild/s1-vacuum-einstein.md)). You do **not** get zero. In the "vacuum" exterior,
$$G_{\mu\nu}[A_\lambda] \ne 0 \qquad (\lambda\ne-1).$$
By Einstein's equations $G_{\mu\nu}=\frac{8\pi G}{c^4}T_{\mu\nu}$, a nonzero $G_{\mu\nu}$ in a region means there is **stress-energy** there:
$$T^{\rm eff}_{\mu\nu} \equiv \frac{c^4}{8\pi G}\,G_{\mu\nu}[A_\lambda] \ne 0.$$
The $\lambda\ne-1$ members are therefore metrics of spacetimes whose exteriors are **not empty**: they are filled with an *effective stress-energy* — some effective matter or field distribution — whatever it takes to make $A_\lambda$ satisfy the real Einstein equations. They are solutions of the postulated flux law, and only *derivatively*, and non-vacuously, "solutions of GR" — with a source.

## Why this rescues consistency with Birkhoff

This is where the picture snaps into focus. **Birkhoff's theorem** ([BIRK](../part2-schwarzschild/birkhoff.md)) states:

> static + spherically symmetric + **vacuum Einstein equations** $\Rightarrow$ Schwarzschild, uniquely.

If our family were a family of static, spherically symmetric *vacuum* solutions, it would flatly contradict Birkhoff — there would be a continuum of them, not one. There is no contradiction, and the reason is exactly the previous section:

> The family evades Birkhoff by **dropping one of its hypotheses — the Einstein equations themselves** — and replacing them with the weaker postulate (I2).

Birkhoff's premises are static + spherical + *vacuum Einstein*. The family keeps static and spherical but swaps *vacuum Einstein* for *the flux law*. Since (I2) is genuinely weaker than $G_{\mu\nu}=0$ (it is a single scalar Gauss law in a chosen variable, not ten tensor equations), it admits more solutions. The moment you re-impose the actual Einstein equations, Birkhoff bites and collapses the family to its single vacuum member, $\lambda=-1$. Equivalently: the non-Schwarzschild members *must* be non-vacuum (carry $T^{\rm eff}_{\mu\nu}\ne0$), because if any of them were vacuum, Birkhoff would force it to be Schwarzschild, and it isn't.

So the family and Birkhoff are not in tension; they are two views of the same gap. The family lives in the space *between* "the usual heuristic ingredients (a Gauss law, $AB=1$, the Newtonian limit)" and "the full Einstein equations." Birkhoff measures how big that gap is: it is exactly one parameter wide, and closing it (re-adding the field equations) leaves only Schwarzschild.

## Why the logical status matters

This reframes what the paper is doing, and it is worth stating without hedging.

- **The underdetermination is not a claim about vacuum GR.** Vacuum GR is *not* underdetermined here — Birkhoff makes its static spherical exterior unique. The family shows instead that the *popular shortcut ingredients* — a Newtonian-style flux law standing in for the field equations — are strictly weaker than GR and admit a whole continuum. The paper's target is the folklore of "simple derivations of Schwarzschild," not general relativity.
- **This is why the selectors have work to do.** Because (I2) is weaker than $G_{\mu\nu}=0$, nothing in the *construction* picks $\lambda=-1$. Something must be *added*: the full field equations (Birkhoff), or a global kinematic condition (Newtonian infall in PG, [PG3](../part7-michell-pg/pg3-newtonian-infall.md)), or observation ($\beta=\lambda+2$, [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md)). Each is a genuine *selecting* ingredient beyond the flux postulate.
- **The flux law is not even covariant.** (I2) is written with the *areal* radial operator; a different coordinate choice for the Gauss law would produce a *different* family. That coordinate dependence is precisely why it is a postulate rather than a law of the theory: real field equations are tensor equations, true in every coordinate system. The family is an artifact of a chosen representation, which is the same "representation vs. fact" theme that runs through the book ([EPI1](../part8-synthesis/epi1-representation-vs-fact.md)).

This connects back to energy accounting. Part 5 asked whether energy could select $\lambda$; the answer was "only conditionally, via a convention." GRSOL explains the deeper reason the whole family exists to be selected among: it is not the solution set of GR's vacuum equations at all, but of a weaker, coordinate-bound postulate. The energy bound, the PPN identity, and the Einstein equations themselves are three different ways of importing the missing content.

## Beyond the paper: in what sense is *any* metric a "GR solution"?

*The following extends the paper's negative-space facts; it is not stated in the paper.*

There is a trivial sense in which every smooth metric "solves general relativity": given any $g_{\mu\nu}$, simply *define* $T_{\mu\nu}\equiv\frac{c^4}{8\pi G}G_{\mu\nu}[g]$, and $G_{\mu\nu}=\frac{8\pi G}{c^4}T_{\mu\nu}$ holds by fiat. In this sense the $\lambda\ne-1$ members are "GR solutions" — but so is *any* metric you scribble, which shows the sense is empty. What gives a solution physical content is that its source $T_{\mu\nu}$ be *independently motivated* (a real matter model) and *physically admissible* (satisfying energy conditions, yielding a geodesically complete, causally sensible spacetime). The paper's members are motivated by the flux postulate, **not** by a matter model — and whether their $T^{\rm eff}_{\mu\nu}$ satisfies any energy condition, and whether the surfaces $r_0=-\lambda r_s$ are regular horizons or something pathological, is **deliberately bracketed** (the paper "does not classify local regularity or global causal character" of the non-Schwarzschild zeros). One could in principle compute $T^{\rm eff}_{\mu\nu}[A_\lambda]$ explicitly and ask these questions; the paper leaves them open on purpose, and so should we. The honest statement is: the $\lambda\ne-1$ members are consistent geometries *sourced by an unspecified effective stress-energy*, exhibited to characterize what the flux postulate allows — not put forward as physical spacetimes.

## Simpler on-ramp

We built a dial of metrics, $A_\lambda$. It is easy to assume they are all "vacuum solutions of Einstein's theory" — different empty-space gravitational fields. They are not. Only the Schwarzschild one ($\lambda=-1$) is truly empty-space. If you take any other setting of the dial and ask Einstein's equations "what matter would produce this?", the answer is *not* "nothing" — it's "some stuff," an effective source spread through the exterior.

That single fact dissolves a paradox. There's a famous theorem (Birkhoff) that says: a static, round, *empty* gravitational field *must* be Schwarzschild — there's only one. So how can we have a whole dial of them? Answer: our dial isn't made of *empty* fields. We never used Einstein's full equations to build it; we used a weaker, Newton-flavored rule (a "flux law"). That weaker rule lets more things through. The instant you demand real emptiness — the actual Einstein equations — the dial snaps to its single empty setting, Schwarzschild. So the family isn't a loophole in GR; it's a map of how much room you have *before* you put GR's real equations in. That room is exactly one dial wide, and that is the whole point of the paper.

## Check your understanding

1. Is $A_\lambda$ for $\lambda=+1$ a vacuum solution of the Einstein equations? What is $G_{\mu\nu}$ there?
2. State precisely which hypothesis of Birkhoff's theorem the family drops, and why that removes the contradiction.
3. Why is "you can always define $T_{\mu\nu}=\frac{c^4}{8\pi G}G_{\mu\nu}$" not a good reason to call the members physical GR solutions?
4. How does the non-covariance of the flux law (its dependence on areal coordinates) reinforce that it is a postulate, not a field equation?

<details>
<summary>Answers</summary>

- **1.** No. $G_{\mu\nu}[A_{+1}]\ne0$; the exterior carries a nonzero effective stress-energy $T^{\rm eff}_{\mu\nu}=\frac{c^4}{8\pi G}G_{\mu\nu}$. Only $\lambda=-1$ gives $G_{\mu\nu}=0$.
- **2.** It drops the **vacuum Einstein equations**, replacing them with the weaker flux postulate (I2). Birkhoff requires vacuum Einstein to conclude uniqueness; without that hypothesis its conclusion doesn't apply, so a family can coexist with Birkhoff. Re-imposing the Einstein equations collapses the family to Schwarzschild.
- **3.** Because that defines a source for *any* metric whatsoever, so it carries no content; a physical solution needs an *independently motivated, admissible* source (real matter, energy conditions, causal sanity), which the flux-postulate members are not given.
- **4.** Genuine field equations are tensor (covariant) equations, holding in all coordinate systems. The flux law uses the areal-$r$ operator specifically; a different coordinate choice yields a different family. Coordinate-dependence marks it as a chosen representation — a postulate — rather than a law of the theory.

</details>

## What the paper claims here

Grounds: **Sec. 2 (I2)** and the **negative-space facts 1–3**. The paper is explicit that the flux operator $\Delta$ is the flat-space radial operator (not Laplace–Beltrami), that (I2) is "a **postulate**, not a covariant field equation and not a consequence of the Einstein equations," and that the construction is complete only *relative to* (I1)–(I4). The negative-space facts record that for $\lambda\ne-1$ the members are **not** vacuum-Einstein solutions (feeding $A_\lambda$ into GR gives a nonzero $G_{\mu\nu}$ = effective stress-energy), that this is why **Birkhoff's theorem is not contradicted** (the dropped hypothesis is the Einstein equations), and that the flux law is coordinate-dependent (hence a postulate). What the paper does **not** establish (and explicitly brackets): the physical sensibility of the $\lambda\ne-1$ members — energy conditions on $T^{\rm eff}_{\mu\nu}$, geodesic completeness, and the nature of the $r_0$ surfaces. The "Beyond the paper" section above is flagged as an extension, not a paper claim.

---
**Path navigation:** ← [prev: ACC6](acc6-energy-localization.md) · [next: PPN1](../part6-ppn-observation/ppn1-ppn-formalism.md) →
**See also:** [BIRK](../part2-schwarzschild/birkhoff.md), [S1](../part2-schwarzschild/s1-vacuum-einstein.md), [CORE4](../part3-building-the-family/core4-classification-theorem.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md)
