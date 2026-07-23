# The question: can energy accounting pick $\lambda$?

> **Tutorial `ACC0`** · Part 5 · **Goal:** State the candidate selector "gravitational energy should gravitate," and anchor it to a real measured effect (the Nordtvedt effect via lunar laser ranging). · **Prereqs:** [CORE4](../part3-building-the-family/core4-classification-theorem.md), [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md), [ENE1](../part1-foundations/ene1-self-energy.md)

**Where this sits in the arc.** We have built the whole family $A_\lambda=(1+\lambda r_s/r)^{-1/\lambda}$ and found that the four static assumptions do *not* pin $\lambda$. Part 5 asks whether a *physical* principle — that the energy stored in the gravitational field must itself gravitate — can supply the missing condition and select $\lambda=-1$. This tutorial poses the question honestly; the next six tutorials show that the answer is "not by itself." Energy accounting turns out to be the selector that *fails* (it gives a convention-bound interval that excludes Schwarzschild), which is exactly why observation (Part 6) has to do the real work.

## The tempting idea

The parameter $\lambda$ is, mechanically, the constant coefficient in the vacuum flux law
$$\Delta s = \lambda\,(s')^2, \qquad s=\ln A, \qquad \Delta = \frac{1}{r^2}\frac{d}{dr}\!\left(r^2\frac{d}{dr}\right).$$
Look at the right-hand side. In the weak field $s = 2\Phi/c^2$, so $(s')^2 = |\nabla s|^2$ is a *squared gradient of the potential* — exactly the shape of a field-energy density. In Newtonian gravity the energy stored in the field per unit volume is $-|\nabla\Phi|^2/(8\pi G)$ (see [ENE1](../part1-foundations/ene1-self-energy.md)). So the nonlinear term $\lambda(s')^2$ *looks* like the field sourcing more of itself: gravitational energy gravitating.

This is not a fringe idea. It is the physically respectable statement that **all energy is a source of gravity**, including the energy bound up in the gravitational field. Binding energy is negative, so a bound system weighs slightly less than its dispersed parts; and — the claim goes — that negative energy should curve spacetime just like any other energy. If that principle fixes how much the field feeds back on itself, it might fix $\lambda$.

So the candidate selector is:

> **Proposal.** Gravitational field energy is a source of gravity, universally and with the same coupling as any other energy. Demanding self-consistency of this statement should determine the nonlinear coefficient $\lambda$.

## Why this is a real, measured question — the Nordtvedt effect

Before we test the proposal, it is worth seeing that "does gravitational binding energy gravitate normally?" is not philosophy. It is one of the sharpest experimental questions in gravitation.

Kenneth Nordtvedt (1968) pointed out that in many alternative theories of gravity, a body's *gravitational binding energy* contributes differently to its **inertial** mass (its resistance to acceleration) than to its **passive gravitational** mass (how strongly it responds to an external gravitational field). If those two contributions differ, then two bodies with different fractional binding energies fall with different accelerations in the same external field — a violation of the (strong) equivalence principle.

The cleanest laboratory is the Earth–Moon system falling toward the Sun. Earth has a substantially larger fractional gravitational binding energy than the Moon (roughly $4.6\times10^{-10}$ of its rest energy, versus about a fortieth of that for the Moon). If binding energy did not gravitate "normally," the Earth and Moon would be pulled toward the Sun by slightly different amounts, and the Moon's orbit would be **polarized** — stretched along the Earth–Sun line, a displacement that would oscillate with a monthly-to-synodic period and a predicted amplitude of order meters.

Lunar laser ranging — bouncing laser pulses off the retroreflectors left on the Moon — measures the Earth–Moon distance to the centimeter level. The result (Williams, Turyshev & Boggs 2004) is a **null**: no such polarization is seen, at a level that confirms gravitational binding energy contributes equally to inertial and gravitational mass to about a part in $10^{4}$ or better. In our family's language, this is exactly a test of whether gravitational energy gravitates like everything else — the very principle the Proposal wants to lean on.

The Nordtvedt effect matters here for two reasons. First, it establishes that the Proposal's premise is physically live and confirmed: gravitational energy *does* gravitate universally. Second — and this is the twist Part 5 will develop — even granting that premise, it does **not** hand us $\lambda$. Knowing that the field energy gravitates is not the same as knowing *how much of the total energy to call "field energy" in the first place.*

## What total energy can and cannot tell us

Here is the structural fact that organizes the whole section. In gravity there are two very different quantities:

- **The total energy of a configuration.** This is operationally well defined: assemble the system, measure the work you extract. It is an invariant, independent of how you bookkeep it. We will compute it exactly in [ACC2](acc2-invariant-assembly-energy.md) and get $E_{\rm int}=-U$ for two shells, with $U\equiv Gm_1m_2/b$.
- **The split of that total into "matter energy" and "field energy."** This is *not* well defined. Even in Newtonian gravity there are two equally valid field-energy densities that integrate to different local distributions (see [ENE1](../part1-foundations/ene1-self-energy.md)). In full GR the ambiguity is worse: gravitational energy has no unique local density at all (pseudotensors, quasi-local energy — [ACC6](acc6-energy-localization.md)).

The Proposal secretly needs the *second* quantity. To turn "field energy gravitates" into a number for $\lambda$, you must decide how much of the total is field energy — and that is a convention, not a measurement. This is the seam the next tutorials pry open:

1. [ACC1](acc1-circularity.md) — **The circularity trap.** If you *define* the field-energy density by reading it off the very equation $\Delta s=\lambda(s')^2$ you are trying to solve, the argument is empty: substitution returns the equation unchanged for *every* $\lambda$, including $\lambda=0$. An identity has been mistaken for a measurement.
2. [ACC2](acc2-invariant-assembly-energy.md) — **The invariant.** The one thing that *is* pinned down: the total two-shell assembly energy $-U$, by a convention-free winch argument.
3. [ACC3](acc3-field-cross-term.md)–[ACC4](acc4-matter-conventions-bound.md) — **The conditional bound.** If you commit to a *gradient-local* field density and a *matter convention*, the invariant $-U$ forces $\lambda=\frac{2f-1}{4}$, hence $\lambda\in[-\tfrac14,\tfrac14]$ — an interval that **excludes** Schwarzschild's $\lambda=-1$.
4. [ACC5](acc5-factor-of-four.md)–[ACC6](acc6-energy-localization.md) — **What that does and doesn't mean.** The factor-of-four in Schwarzschild's field density; and the general lesson that energy has no address.

## The caveat we carry throughout

One sentence must never be dropped, because it is the difference between a careful result and a crank claim:

> **The section does not claim that general relativity violates energy conservation.** The invariant total assembly energy is $-U$ in every member and every convention. What the section constrains is the *split* of that total into matter and field pieces under a specific class of localization conventions. A "bound on $\lambda$" derived this way inherits the arbitrariness of the split; it is a statement about bookkeeping, not about whether energy is conserved.

Hold both hands open at once: the total is real and invariant; the matter–field division is a gauge-like convention. That posture — the same one a strong reader brings to representation freedom in any formalism — is the whole skill of Part 5.

## Simpler on-ramp

Think of the total cost of building a piece of furniture. That total — what you actually paid — is a fact; anyone who redoes the purchase gets the same number. Now try to split that total into "cost of the wood" and "cost of the labor." If the store bundled them, you can allocate the split many ways, and each way is a *convention*: none is more true than another, and the total is the same in all of them.

Gravitational energy is like this. The total energy of a configuration is a hard fact (you can measure the work to assemble it). But "how much of that energy lives in the matter vs. in the gravitational field" is a bundled cost with no unique itemization. The Proposal wants to read $\lambda$ off the "field" line of the receipt — but *you* wrote that line by choosing a convention. The Nordtvedt effect tells us the premise (gravitational energy really does gravitate) is true; it just doesn't tell us how to itemize the bill.

## Check your understanding

1. Why does the fact that the *total* assembly energy is invariant not immediately give us $\lambda$?
2. What does the Nordtvedt effect measure, and why is a *null* result the relevant one for the Proposal?
3. A colleague says "the paper is claiming GR gets energy conservation wrong for $\lambda\ne-1$." What's wrong with that reading?

<details>
<summary>Answers</summary>

- **1.** Because $\lambda$ lives in the *field* piece of the energy, and separating "field energy" from "matter energy" out of a well-defined total requires a convention. The invariant constrains only the sum, not the parts; you need an extra choice (a localization rule + a matter convention) before the total says anything about $\lambda$ — and then the answer is only as strong as that choice.
- **2.** It measures whether a body's gravitational binding energy contributes equally to its inertial and gravitational mass, by looking for a polarization of the Moon's orbit toward the Sun. A null result confirms that gravitational energy gravitates universally — the Proposal's premise is correct. But confirming the premise does not itemize the total into matter and field pieces, so it still doesn't fix $\lambda$.
- **3.** The invariant total assembly energy is $-U$ for *every* member and *every* convention; nothing about conservation changes. The section constrains the *matter–field split* under particular localization conventions. Calling that "violating conservation" confuses a bookkeeping convention with a physical law.

</details>

## What the paper claims here

Grounds: **Sec. 4 (introduction)** and the framing of **Sec. 4.1–4.2**. The paper proposes that gravitational field energy might supply the missing condition ("binding energy negative; gravitational energy gravitates universally"), and cites the Nordtvedt effect (Nordtvedt 1968; Williams, Turyshev & Boggs 2004) as the physical motivation that anomalous coupling is a real, tested question. It stresses that the *total* energy is well defined even when the matter/field split is not, and — crucially — that establishing the bound "**is not a claim that general relativity violates energy conservation**." What the paper does **not** claim: that energy accounting *selects* Schwarzschild. On the contrary, Part 5 will show it yields only a *conditional* interval $[-\tfrac14,\tfrac14]$ that excludes $\lambda=-1$; the actual selection is done by observation in Part 6.

---
**Path navigation:** ← [prev: ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) · [next: ACC1](acc1-circularity.md) →
**See also:** [ENE1](../part1-foundations/ene1-self-energy.md), [ACC1](acc1-circularity.md), [ACC6](acc6-energy-localization.md), [EPI2](../part8-synthesis/epi2-identities-not-measurements.md)
