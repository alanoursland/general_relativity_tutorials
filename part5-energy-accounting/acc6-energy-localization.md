# Energy has no address

> **Tutorial `ACC6`** · Part 5 · **Goal:** See that gravitational energy has no unique local density — in Newton (two densities differing by a total divergence) and in GR (pseudotensors; quasi-local energy) — and understand why that makes the matter–field split gauge-like, sealing crux 3. · **Prereqs:** [ACC4](acc4-matter-conventions-bound.md), [ACC5](acc5-factor-of-four.md), [ENE1](../part1-foundations/ene1-self-energy.md)

**Where this sits in the arc.** This is the conceptual capstone of Part 5 and the completion of crux 3. Every step so far has leaned on one fact: the *total* energy is invariant but the *split* is a convention. Here we see *why* that is not sloppiness but a deep feature of gravity — energy genuinely has no address — and why, therefore, no accounting scheme can select $\lambda$.

## The Newtonian ambiguity, made precise

We have used twice now the fact that Newtonian gravity offers two energy densities:
$$u_{\rm field} = -\frac{|\nabla\Phi|^2}{8\pi G}, \qquad u_{\rm matter} = \tfrac12\,\rho\,\Phi.$$
They give the same total. Here is the exact reason. Use the field equation $\nabla^2\Phi=4\pi G\rho$ to write $\rho=\nabla^2\Phi/4\pi G$, so
$$u_{\rm matter} = \tfrac12\rho\Phi = \frac{\Phi\,\nabla^2\Phi}{8\pi G}.$$
Now apply the product rule $\nabla\!\cdot\!(\Phi\nabla\Phi) = |\nabla\Phi|^2 + \Phi\nabla^2\Phi$, i.e. $\Phi\nabla^2\Phi = \nabla\!\cdot\!(\Phi\nabla\Phi) - |\nabla\Phi|^2$. Integrate over all space:
$$\int u_{\rm matter}\,dV = \frac{1}{8\pi G}\int \nabla\!\cdot\!(\Phi\nabla\Phi)\,dV - \frac{1}{8\pi G}\int|\nabla\Phi|^2\,dV.$$
The first term is a boundary integral (divergence theorem) over a sphere at infinity; for a localized source $\Phi\sim 1/r$, $\nabla\Phi\sim1/r^2$, and the surface area $\sim r^2$, so it falls off as $1/r\to0$. What remains is
$$\int u_{\rm matter}\,dV = -\frac{1}{8\pi G}\int|\nabla\Phi|^2\,dV = \int u_{\rm field}\,dV.$$
Equal totals. But look at what distinguishes them: the two densities differ *pointwise* by the total divergence $\frac{1}{8\pi G}\nabla\!\cdot\!(\Phi\nabla\Phi)$, a term that **integrates to zero** yet **relabels where the energy sits**. One density piles energy where matter is ($\propto\rho\Phi$); the other spreads it through the field ($\propto|\nabla\Phi|^2$). You may add any total divergence you like and get yet another density with the same total. There is no experiment on the *total* that distinguishes them.

This is the localization ambiguity in miniature, and it already has the structure of a **gauge freedom**: a family of representations (densities) related by terms that vanish in the invariant (the total), with no observable picking one out.

## In general relativity it is worse — and structural

Newtonian gravity at least offers *candidate* densities. Full GR denies even that, for a reason rooted in the equivalence principle.

At any single event you can choose a **local inertial frame**: coordinates in which the metric is Minkowski and its first derivatives (the Christoffel symbols — the "gravitational field") vanish at that point. But any local energy density built from the gravitational field would then have to *vanish at that event* — while at the same event, in a different frame, it would not. A genuine tensor that is zero in one frame is zero in all frames; a "gravitational energy density" that can be transformed to zero at any chosen point therefore **cannot be a tensor**. There is no covariant, pointwise local density of gravitational energy. Energy, in GR, has no address.

What GR *does* offer are two kinds of well-defined answers, neither of them a local density:

- **Pseudotensors** (Einstein's, Landau–Lifshitz's, and others). These are coordinate-dependent objects that, integrated over a suitable region, yield sensible *totals* (they reproduce the right ADM mass, for instance). But their local values are frame-dependent — different pseudotensors and different coordinates distribute the "same" energy differently. They are bookkeeping devices for the total, explicitly not invariant densities.
- **Quasi-local and asymptotic energies**, defined as *boundary integrals* rather than volume integrals of a density:
  - **Komar** mass/energy — for stationary spacetimes, from the timelike Killing vector;
  - **ADM** energy — the total measured at *spatial* infinity;
  - **Bondi** energy — measured at *null* infinity, decreasing as gravitational waves carry energy away.
  These are genuinely meaningful, invariant numbers attached to a *region or an asymptotic boundary*, not to a point. (Their construction is beyond our scope; treat them as further reading — they are the rigorous forms of "the total energy of this region is well defined even though the local density is not.")

The throughline: **totals and fluxes are well defined; pointwise gravitational energy density is not.** This is exactly the shape we met operationally in [ACC2](acc2-invariant-assembly-energy.md) — the winch (a total/flux) is unambiguous — and in [ACC4](acc4-matter-conventions-bound.md) — the split (a density-level notion) is a convention.

## Why the split is gauge-like, and why accounting can't select $\lambda$

Now crux 3 closes. The conditional bound $\lambda\in[-\tfrac14,\tfrac14]$ was built on a choice: the gradient-local field density (a localization) plus the dial $f$ (a matter convention). We now see that this choice is *precisely* a choice of representation for something that has no invariant representation. The dial $f$ is a gauge parameter. The invariant — the total $-U$ — is fixed; everything the bound adds beyond it is gauge.

So the reason energy accounting cannot select $\lambda$ is not a technical shortfall to be patched by a cleverer scheme. It is structural: **selecting $\lambda$ from a static energy budget would require a fact about where gravitational energy lives, and there is no such fact.** Any scheme that appears to select $\lambda$ has smuggled in a convention (a localization, a value of $f$), and its output is only as real as that convention. The self-consistency lemma of [ACC1](acc1-circularity.md) was the first face of this; the localization ambiguity is its root.

Hold the final posture, the mark of author-level understanding:

- **Invariant (real):** the total assembly energy $-U$; the ADM/Bondi/Komar totals; energy conservation itself.
- **Convention (gauge-like):** the matter–field split; any local gravitational energy density; the dial $f$; the interval $[-\tfrac14,\tfrac14]$ and its exclusion of Schwarzschild.

And, once more, the caveat that separates this from crankery: **none of this says GR violates energy conservation.** The total is perfectly conserved and perfectly invariant. What is ambiguous is only the *localization* — the assignment of that conserved total to matter here versus field there. A "bound on $\lambda$" read off the split is a statement about a gauge choice, not about gravity. That is why observation, not accounting, has to select the metric ([PPN3](../part6-ppn-observation/ppn3-gamma-beta.md)).

## Simpler on-ramp

Imagine a stretched trampoline with a bowling ball in the middle. Ask: "where is the energy stored in the stretched surface?" You could say it's in the fabric right under the ball (where the load is), or spread across the whole sloped sheet (wherever it's taut). Both descriptions add up to the same total stored energy, and no measurement of the total can tell you which is "right" — because the question "where exactly is it?" doesn't have a unique answer. You can shuffle energy from "under the ball" to "across the sheet" and back by re-describing, without changing the total.

Gravitational energy is like this, only more so. In Einstein's theory you can always stand at a point and, by falling freely, make the gravitational field vanish *right there* — so any "energy density of the field" you write down could be zeroed out at that spot by a change of viewpoint. A real, physical density can't be made to disappear just by moving. So there is no real local density; there are only well-defined *totals*. That is why our attempt to pin $\lambda$ by asking "how much energy is in the field?" was doomed: the question has no observer-independent answer. The total was always $-U$; the rest was a way of talking.

## Check your understanding

1. By what precise object do the two Newtonian energy densities differ, and why doesn't it change the total?
2. Give the equivalence-principle argument for why GR has no local gravitational energy density.
3. What kind of object *is* well-defined in GR — Komar/ADM/Bondi energy — and how does that fit the "totals yes, density no" slogan?
4. In one sentence, why does "energy has no address" imply static accounting cannot select $\lambda$?

<details>
<summary>Answers</summary>

- **1.** By a total divergence $\frac{1}{8\pi G}\nabla\!\cdot\!(\Phi\nabla\Phi)$, which integrates (via the divergence theorem) to a boundary term that vanishes at infinity for a localized source; it redistributes energy pointwise without changing the total.
- **2.** At any event one can choose a freely-falling (local inertial) frame in which the Christoffel symbols vanish, so any field-built energy density is zero there; but a tensor zero at a point in one frame is zero in all frames, so such a density cannot be a tensor — there is no covariant local density.
- **3.** They are invariant *boundary/asymptotic* integrals attached to a region or to spatial/null infinity — totals, not pointwise densities. They realize "the total energy of this region is well defined" while "the local density" remains undefined.
- **4.** Because selecting $\lambda$ from a static budget would require knowing where gravitational energy lives, and it lives nowhere in particular; any selection smuggles in a convention and inherits its arbitrariness.

</details>

## What the paper claims here

Grounds: **Sec. 4.2** and **Sec. 4.7**. The paper states localization is convention-dependent even in Newton ($-|\nabla\Phi|^2/8\pi G$ vs. $\tfrac12\rho\Phi$, up to boundary terms and the field equation) and worse in GR (pseudotensors, quasi-local energy), while the total assembly work is unambiguous; and (Sec. 4.7) that "energy conservation determines the total; converting it into a self-coupling coefficient needs localization and matter choices," so "static assembly alone leaves the coefficient undetermined." What the paper does **not** claim: that any particular localization (Komar/ADM/Bondi/pseudotensor) is singled out here — these are named only to establish that the split has no unique answer, which is exactly what makes the Part 4 bound conditional. The overarching caveat stands: this concerns the split, not energy conservation.

---
**Path navigation:** ← [prev: ACC5](acc5-factor-of-four.md) · [next: GRSOL](grsol-are-these-gr-solutions.md) →
**See also:** [ENE1](../part1-foundations/ene1-self-energy.md), [ACC4](acc4-matter-conventions-bound.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md), [EPI2](../part8-synthesis/epi2-identities-not-measurements.md)
