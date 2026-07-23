# Shortcut vs. Real Derivation

> **Tutorial `CORE-CONTRAST`** · Part 3 · **Goal:** Put the four-assumption "shortcut" side by side with the full vacuum-Einstein derivation, name exactly what the shortcut buys and what it gives up, and explain why a family (not a unique metric) is the honest outcome — without contradicting Birkhoff's theorem. · **Prereqs:** [CORE4](./core4-classification-theorem.md), [S1](../part2-schwarzschild/s1-vacuum-einstein.md)

**Where this sits in the arc.** This closes the "build" arc of Part 3 by contrasting what we did with what a real GR derivation does. The comparison is the whole moral of the paper in miniature: the four assumptions are a *weaker* input than the Einstein equations, so they determine *less* — a one-parameter family instead of a unique solution. Everything after this either selects within the family or explains why a historical shortcut appeared to select for free.

## Two derivations, side by side

| | **The four-assumption shortcut** (this book, Part 3) | **Full vacuum GR** ([S2](../part2-schwarzschild/s2-deriving-schwarzschild.md)) |
|---|---|---|
| Governing law | A *postulated* radial flux law $\Delta V = 0$ for one variable $V(A)$ (I2) | The Einstein field equations $G_{\mu\nu} = 0$ (ten coupled equations) |
| Extra structural inputs | (I1) Newtonian limit, (I3) $AB=1$, (I4) constant nonlinear coefficient | Static + spherical symmetry, asymptotic flatness |
| Nature of the law | Coordinate-dependent (uses areal $r$), scalar, one equation | Covariant, tensorial, coordinate-free |
| What it determines | The **one-parameter family** $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$ | The **unique** Schwarzschild metric $A = 1 - r_s/r$ |
| Where Schwarzschild is | One member, $\lambda = -1$ | The whole answer |
| $AB = 1$ | *Assumed* (I3) | *Derived* (a consequence of $G_{\mu\nu}=0$) |
| Status of $\lambda$ | Free — a leftover representation choice | Not present — pinned to $-1$ automatically |

Read the last three rows together. In full GR, two of the shortcut's *assumptions* are *outputs*: the reciprocity $AB = 1$ falls out of the field equations, and the nonlinear structure is fixed with no free coefficient. The shortcut has to *assume* $AB=1$ and *assume* a constant coefficient precisely because it threw away the machinery (the full $G_{\mu\nu}$) that would have produced them. Having assumed less, it concludes less.

## What the four assumptions buy — and what they cost

**What they buy.** Enormous economy. The Einstein tensor for the ansatz is a page of Christoffel symbols and curvature components; the flux law $\Delta V = 0$ is a one-line ODE any calculus student can integrate ([CORE1](./core1-flux-freedom.md)). And they buy *transparency*: because the construction is so simple, we can see exactly which knob (the potential variable) is unconstrained, and label the residual freedom cleanly as $\lambda$. A full derivation hides that freedom by never letting it appear.

**What they cost.** Uniqueness, and physical grounding. The flux law is a *postulate*, not a field equation. It is written in a *chosen* coordinate (areal $r$); a different coordinate choice would give a different flux law and a different family (negative-space fact 3). And crucially it does not know about the $tt$, $rr$, and angular Einstein equations that, in real GR, over-determine the system and force $\lambda = -1$. The cost of the shortcut is exactly the freedom it exposes: **a family, because a scalar flux postulate is weaker than a tensor field equation.**

## The negative-space fact: these are not (mostly) GR solutions

It is worth stating bluntly, because it is easy to misread the family as "a bunch of new vacuum solutions." It is not. For $\lambda \neq -1$, the metric $A_\lambda$ is **not** a solution of the vacuum Einstein equations. If you compute the Einstein tensor of $A_\lambda$ and set it against $G_{\mu\nu} = 0$, you get a **nonzero** $G_{\mu\nu}$ in the region we called "vacuum" — i.e. an effective stress–energy that would have to be present to make $A_\lambda$ a genuine GR spacetime. The members solve a *postulated flux law*, not $G_{\mu\nu} = 0$. Only $\lambda = -1$ coincides with a true vacuum solution. This is developed carefully in [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md); flag it here so the family is never mistaken for a catalogue of vacuum spacetimes.

## Why this does not contradict Birkhoff's theorem

Birkhoff's theorem states: *static (in fact even without assuming static) + spherically symmetric + **the vacuum Einstein equations** $\Rightarrow$ Schwarzschild, uniquely.* A newcomer might worry that a one-parameter family of static spherical exteriors flatly contradicts a uniqueness theorem. It does not, and seeing why is the sharpest possible test of what the shortcut actually did.

The resolution is a single dropped hypothesis. Birkhoff assumes **the Einstein equations**. The family replaces that hypothesis with the *weaker* flux postulate (I2). Weaken a theorem's hypothesis and you weaken its conclusion: dropping "$G_{\mu\nu} = 0$" in favor of "$\Delta V = 0$ for some $V(A)$" turns Birkhoff's *unique* Schwarzschild into a *one-parameter* family. There is no contradiction because the two arguments are not proving the same theorem — they start from different premises. Concretely:

- Birkhoff's premises $\Rightarrow$ $\lambda = -1$ forced.
- (I1)–(I4) $\Rightarrow$ $\lambda$ free.

The family lives entirely in the gap between "the Einstein equations" and "a scalar flux postulate that agrees with them only at $\lambda = -1$." Naming that gap precisely — which hypothesis of Birkhoff is dropped — is the cleanest way to locate what this whole construction is. See [BIRK](../part2-schwarzschild/birkhoff.md) for the theorem itself.

## The takeaway for reading any "simple derivation"

The historical literature is full of short derivations that "get Schwarzschild" from less than the full Einstein equations. The contrast above tells you what to look for in every one of them: since the honest weak input yields a *family*, any derivation that lands on a *unique* Schwarzschild must have smuggled in a selecting condition somewhere. Your job as a critical reader is to find it — the extra kinematic assumption, the tacit choice of potential variable, the imposed infall law. This is the *build vs. select* audit that organizes Part 8; see [EPI3](../part8-synthesis/epi3-build-vs-select.md) and the literature map in [SYN1](../part8-synthesis/syn1-century-of-shortcuts.md). The four-assumption construction is valuable precisely because it makes the baseline explicit: *this* much you get for free, and no more.

## Simpler on-ramp

Two ways to find the metric outside a star:

- **The real way:** solve Einstein's equations. They are strong and numerous, and they pin down a single answer, Schwarzschild. Along the way they *hand you* facts you would otherwise have to assume — like $AB = 1$.
- **The shortcut way:** replace Einstein's equations with a much simpler rule ("some function of the metric spreads out like a $1/r$ field"), plus a few reasonable-sounding extras. This is easy to solve, but it is *weaker*, so it cannot pin down a single answer. It gives a whole family, with Schwarzschild as one member.

Getting a family instead of one metric is not a mistake in the shortcut — it is the *correct* consequence of using a weaker rule. And it does not clash with the famous uniqueness theorem (Birkhoff), because that theorem assumes the strong rule; drop the strong rule and its uniqueness drops too. The lesson to carry: whenever a simple derivation claims a *unique* Schwarzschild from *less* than Einstein's equations, an extra assumption is hiding in it. Find it.

## Check your understanding

1. Name two things that are *assumptions* in the shortcut but *consequences* in full GR.
2. Why does using a weaker (scalar, postulated) law instead of the Einstein equations yield a family rather than a unique metric?
3. Are the $\lambda \neq -1$ members vacuum-Einstein solutions? If not, what are they?
4. State precisely which hypothesis of Birkhoff's theorem the family drops, and why that removes the contradiction.

<details>
<summary>Answers</summary>

- **1.** $AB = 1$ (assumed as (I3); derived from $G_{\mu\nu}=0$) and the nonlinear structure / value of the coefficient (assumed constant via (I4), with the value free; fixed to $\lambda=-1$ automatically in GR).
- **2.** A single coordinate-dependent scalar postulate constrains less than ten covariant field equations; the unconstrained representation freedom (which $V(A)$ obeys the flux law) survives as the free parameter $\lambda$.
- **3.** No, except $\lambda = -1$. For $\lambda \neq -1$, $G_{\mu\nu}[A_\lambda] \neq 0$ in the "vacuum," i.e. there is an effective stress–energy; the members solve a postulated flux law, not the Einstein vacuum equations. (See [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md).)
- **4.** It drops "the vacuum Einstein equations," replacing them with the weaker flux postulate (I2). Weaker hypothesis, weaker conclusion: Birkhoff's *unique* Schwarzschild becomes a one-parameter family. The two arguments have different premises, so there is no contradiction.

</details>

## What the paper claims here

Grounds: §2 framing, §7, and the paper's negative-space discussion. The paper is explicit that (I2) is *"a postulate, not a covariant field equation and not a consequence of the Einstein equations,"* that it is coordinate-dependent (areal $r$), and that the construction *"determines a complete one-parameter family, not a unique exterior,"* recovering $r_s$ and including Schwarzschild at $\lambda=-1$ without selecting it. The author-level facts that (i) $\lambda \neq -1$ members are not vacuum-Einstein solutions (nonzero effective $G_{\mu\nu}$) and (ii) Birkhoff is evaded by *replacing the field equations with a weaker postulate* are stated in the paper's negative-space notes and elaborated in [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md) and [BIRK](../part2-schwarzschild/birkhoff.md). The paper does **not** claim the shortcut is equivalent to GR — it claims the opposite, and that is the point.

---
**Path navigation:** ← [prev in default path](./core5-distinguished-members.md) · [next](../part4-family-structure/zero1-finite-radius-zeros.md) →
**See also:** [S2](../part2-schwarzschild/s2-deriving-schwarzschild.md), [BIRK](../part2-schwarzschild/birkhoff.md), [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md), [EPI3](../part8-synthesis/epi3-build-vs-select.md)
