# HIST1 — Michell & Laplace: right number, wrong reason

> **Tutorial `HIST1`** · Part VII · **Goal:** Present Michell's 1784 dark-star calculation, show exactly what it does and doesn't supply, and reconstruct the corrected logical order that actually explains why his number is right. · **Prereqs:** [PG3](./pg3-newtonian-infall.md), [PG4](./pg4-horizons-light-cones.md)

**Where this sits in the arc.** This tutorial is the payoff of the entire book's arc, applied to the oldest claim in the story. Michell got the number $r=2GM/c^2$ right in 1784, a century before anyone had a metric to derive it from. The three-selector spine — build the family, let PPN/accounting/PG-infall each bear on $\lambda$, then read off the horizon — is precisely what is needed to say *why* his number is right without pretending his argument was a valid derivation of it.

## Michell's calculation

In 1784 (and independently, a little later, Laplace), the argument runs entirely inside Newtonian mechanics. For a body of mass $M$ and radius $r$, the escape velocity — the launch speed at which a projectile fired straight up just barely reaches infinity with zero speed to spare — is found from energy conservation:
$$\frac12 v_{\rm esc}^2 = \frac{GM}{r}.$$
Treating light as a stream of corpuscles subject to ordinary gravity (a live and reasonable idea in 1784, well before the wave theory of light was settled and over a century before special relativity), Michell asked: is there a radius small enough that even light, with speed $c$, cannot escape? Setting $v_{\rm esc}=c$:
$$\frac12c^2 = \frac{GM}{r} \quad\Longrightarrow\quad r = \frac{2GM}{c^2}.$$
This is, numerically, *exactly* $r_s$ — the same radius that would fall out of Einstein's field equations 140 years later as the Schwarzschild horizon.

## Why this should raise suspicion, not confidence

Both ingredients of Michell's calculation are used well outside their domain of validity: the Newtonian potential $\Phi=-GM/r$ is a weak-field approximation, and the nonrelativistic kinetic energy $\tfrac12mv^2$ is valid only for $v\ll c$ — yet the calculation is applied at exactly the point where $v=c$, precisely the regime both approximations are least trustworthy. Getting the numerically correct answer from formulas that are invalid exactly where you need them is a strong signal that something is cancelling by coincidence, not that the formulas were secretly good all along. The honest response to "the number came out right anyway" is to ask *why* — not to conclude the Newtonian derivation was rigorous after all.

## What Michell's argument does not supply

Set against the machinery built in this book, three things are conspicuously absent from Michell's calculation:

1. **No radial metric.** Michell never writes anything resembling $A(r)$ or $B(r)$; there is no line element, no notion of $g_{tt}$ or $g_{rr}$, only a scalar velocity compared to $c$.
2. **No mixed term.** [PG2](./pg2-where-did-curvature-go.md) located the actual carrier of curvature in the $2v\,dr\,dT$ term — a structure with no Newtonian counterpart whatsoever. Michell's corpuscular light simply rises against gravity like a thrown ball: it decelerates, and (in his picture) would eventually stop and fall back, tracing something like a parabolic arc. Nothing in that picture resembles the light-cone tipping of [PG4](./pg4-horizons-light-cones.md), where the very notion of "outward progress" vanishes and then reverses — not merely slows.
3. **No causal argument.** Michell's "dark star" is a star whose light cannot travel far enough away to be seen, the way a ball thrown too slowly falls back to Earth. A horizon in the [PG4](./pg4-horizons-light-cones.md) sense is not a "falls back" phenomenon at all: it is a surface at which the outward light-cone itself tips over, so that *no* direction of travel, however fast, increases areal radius. These are different physical claims that happen to share a formula and a number.

## The corrected logical order

The book's own results reconstruct Michell's coincidence, but running in the opposite direction:

1. Independent physical information — the measured PPN parameter $\beta\approx1$ from Mercury's perihelion precession ([PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md), [PPN6](../part6-ppn-observation/ppn6-reading-constraints.md)) — selects $\lambda=-1$ among the whole one-parameter family the static assumptions permit. This step uses no Newtonian escape-velocity reasoning at all.
2. Given $\lambda=-1$ (Schwarzschild), [PG3](./pg3-newtonian-infall.md) proved — as a *derived* fact about the selected metric, not an assumption — that the PG river velocity satisfies $v_{-1}^2=2GM/r$ *exactly*, at every radius, not merely in the weak field.
3. This $v_{-1}(r)$ is a genuine geometric quantity: the coordinate shift of observers falling from rest at infinity ([PG1](./pg1-painleve-gullstrand.md)), and, per [PG4](./pg4-horizons-light-cones.md), exactly the quantity that determines where outgoing light stops making outward progress.
4. Setting $v_{-1}=c$ ([PG4](./pg4-horizons-light-cones.md)) gives precisely $r=r_s=2GM/c^2$ — Michell's number, reproduced as a consequence of a fully specified, independently selected, relativistic spacetime, evaluated exactly at the point where "$v=c$" carries a rigorous operational meaning.

The same algebraic step — "set $\tfrac12v^2=GM/r$, then set $v=c$" — is performed twice: once by Michell, as an ad hoc extrapolation of Newtonian mechanics past its domain, and once, implicitly, inside the correctly selected Schwarzschild geometry, where [PG3](./pg3-newtonian-infall.md) already established that the Newtonian-looking formula happens to hold exactly. The two calculations agree numerically because, *after selection*, the formula is exactly true of the selected geometry — not because Newtonian mechanics was valid at $v=c$ all along.

## The verdict: explained, not vindicated

The coincidence is *explained*: the book's machinery shows precisely why the Newtonian-looking number is exactly correct for Schwarzschild, and precisely which member of the family that requires. It is not *vindicated*: nothing about this explanation retroactively certifies Michell's reasoning as a valid relativistic derivation. His argument identifies the right scale by a fortunate formal coincidence; it supplies neither the metric, nor the causal structure, nor any way to know — from inside 1784 physics — that the coincidence would hold.

## Simpler on-ramp

Imagine a student computing a definite integral by illegally swapping two limits of integration, and getting the textbook-correct numerical answer because two sign errors happened to cancel. The number is right. The method taught nothing true about integrals, and there is no reason to expect it to keep working on the next problem — indeed, it wouldn't; for any other family member (any $\lambda\neq-1$), the same "set kinetic energy equal to potential energy, then set $v=c$" trick does not reproduce that member's own horizon-analogue radius, exactly because [PG3](./pg3-newtonian-infall.md) showed the Newtonian formula is only exactly true for $\lambda=-1$. Michell's calculation is that lucky integral: right answer, invalid method, no license to trust the method elsewhere.

## Check your understanding

- Which two ingredients of Michell's calculation are used outside their domain of validity, and where exactly does the calculation apply them?
- What three specific structures does Michell's argument fail to supply, that a genuine metric derivation needs?
- What is the corrected four-step logical order, from observation to $r_s$?
- Why does "coincidence explained, not vindicated" avoid over-crediting Michell while still taking his result seriously?

**Answers**
- The Newtonian potential $\Phi=-GM/r$ (a weak-field approximation) and the nonrelativistic kinetic energy $\tfrac12mv^2$ (valid only for $v\ll c$); both are applied at $v=c$, exactly outside their stated range of validity.
- A radial metric ($A(r)$, $B(r)$); the mixed term $2v\,dr\,dT$ that actually carries curvature/light-cone tilting; and a genuine causal (not "falls back like a ball") argument for why light cannot escape.
- (1) Observation ($\beta\approx1$) selects $\lambda=-1$; (2) PG3 shows $v_{-1}^2=2GM/r$ exactly at every radius for that metric; (3) $v_{-1}$ is the real coordinate shift of infalling observers; (4) setting $v_{-1}=c$ gives $r=r_s$ exactly.
- It credits Michell with landing on the correct number and explains, from the correctly selected geometry, exactly why that number is exact — while being explicit that his own reasoning, using formulas invalid at $v=c$, was not a valid relativistic derivation and does not become one in hindsight.

## What the paper claims here

Grounded in Sec. 1 and Sec. 6.4: "Michell (1784): escape velocity $=c$ gives $r=2GM/c^2$, numerically the Schwarzschild radius, but uses Newtonian potential + nonrelativistic KE outside their validity," and the paper's own framing that this is a "coincidence/cancellation" that "shows he didn't derive a horizon but doesn't explain the exact coefficient" on its own. Sec. 6.4 states explicitly: "Michell supplies neither radial metric nor mixed structure; his premises don't determine Schwarzschild or the causal behavior at $r_s$," and gives the valid direction as "dynamics/observation $\to\lambda=-1$; then $\lambda=-1\to v^2=2GM/r$ in PG; then $v=c\to r=r_s$." Sec. 7.3 summarizes: "Michell identifies the scale; Schwarzschild geometry explains why the Newtonian-looking relation becomes exact in this representation." The paper does not claim Michell's argument was secretly correct, nor that the coincidence is inexplicable — only that it requires the independently selected geometry to explain.

---
**Path navigation:** ← [prev: PG4](./pg4-horizons-light-cones.md) · [next: HIST2](./hist2-factor-of-two.md) →
**See also:** [PG3](./pg3-newtonian-infall.md), [PG4](./pg4-horizons-light-cones.md), [EPI3](../part8-synthesis/epi3-build-vs-select.md)
