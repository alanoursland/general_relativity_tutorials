# Build vs. Select

> **Tutorial `EPI3`** · Part 8 · **Goal:** turn the paper's method into a reusable audit — how to take *any* "simple derivation," separate the construction of the solution set from the selecting condition, and name the smuggled assumption · **Prereqs:** [`CORE4`](../part3-building-the-family/core4-classification-theorem.md), [`SYN1`](syn1-century-of-shortcuts.md).

**Where this sits in the arc.** This is the paper's method extracted from its subject matter. Everything the book has done — build a family, watch selectors succeed and fail — was one reasoning move applied to gravity. Here we state the move so cleanly that you can run it on a derivation you have never seen, in a field that is not physics.

## The move

Confronted with a "simple derivation of $X$," do not ask "is it right?" first. Ask, in order:

1. **What is the construction?** Which assumptions are actually in force, and what is the *complete* set of objects consistent with them? Not "does this reach $X$" but "what is *everything* this reaches." Characterize the solution set.
2. **What is the selecting condition?** Which step, if any, narrows that set to the single answer $X$? Isolate it as a distinct ingredient, separate from the construction.
3. **What does the selector add?** Name the extra information the selecting condition carries — the input that was *not* in the construction's assumptions. That is the smuggled assumption. It is the real content of the derivation.

A derivation that reaches $X$ is honest exactly when steps 2 and 3 are stated out loud. It is a *shortcut* — in the pejorative sense — when the selector is disguised as part of the construction, so the added ingredient looks like it fell out of the minimal assumptions for free.

## Why the move works: build and select are different acts

Constructing a solution set and exhibiting one solution are categorically different, and conflating them is the master error the paper diagnoses. **Building** answers "what is possible?" and yields a set — here, the family $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$, complete relative to (I1)–(I4) ([`CORE4`](../part3-building-the-family/core4-classification-theorem.md)). **Selecting** answers "which one is realized?" and requires information the construction does not contain. The base static assumptions build; they never select ([`CORE0`](../part3-building-the-family/core0-four-assumptions.md), [`MAP`](../part0-orientation/map.md)).

For a CS reader the distinction is native: characterizing the language a grammar generates is not the same as exhibiting one string; solving a constraint system's *whole* solution space is not the same as returning one satisfying assignment. A "derivation" that hands you one string while implying the grammar forced it is hiding a selection. The tell is always that the grammar, examined honestly, generates more than one string.

## The tell: it would work for other answers

The sharpest single diagnostic for a smuggled selector is this: **would the construction, with its stated assumptions alone, also have permitted a different answer?** If yes, then any step that nonetheless lands on the specific $X$ must be adding something — find that step. In this paper the diagnostic is dispositive because the construction is *proved complete*: the assumptions permit an entire continuum of $\lambda$, so any argument reaching $\lambda = -1$ **must** contain an ingredient beyond them. There is no escape; the classification theorem forecloses "it just came out that way." This is why building the whole family first is not a detour — it is what makes every subsequent selection auditable.

Contrast this with the weaker situation Rindler and Gruber et al. left the field in ([`SYN1`](syn1-century-of-shortcuts.md)): they showed *by counterexample* that the usual ingredients don't determine the metric. That is a negative result — "your assumptions are insufficient." The present paper upgrades it to a constructive one — "here is exactly what your assumptions *do* determine, and therefore exactly how much any successful derivation must be adding." Negative space becomes a measuring stick.

## Running the audit: worked cases

The full catalogue is [`SYN1`](syn1-century-of-shortcuts.md); here are three, run explicitly through the three questions, to show the method's grip.

**Michell (1784).** *Construction:* Newtonian escape velocity set to $c$. *Solution set:* a single length, $2GM/c^2$ — no metric, no family. *Selector:* none; there is nothing to select because no geometry was built. *What it adds:* only the scale. The error historically attributed to Michell — "he derived the horizon" — fails at step 1: his construction never produces an $A(r)$ at all. The corrected reading ([`HIST1`](../part7-michell-pg/hist1-michell-laplace.md)) runs the logic the other way: select Schwarzschild first (by observation or dynamics), and *then* the Painlevé–Gullstrand infall $v^2 = 2GM/r$ makes $v = c$ at $r = r_s$ true — a downstream property, not a premise.

**Visser (2005).** *Construction:* a Newtonian infall heuristic in flat-slice form. *Solution set:* it looks minimal, but the flat-slice PG form is available for *every* member. *Selector:* the demand that the infall profile equal $v^2 = 2GM/r$ at every radius. *What it adds:* a global kinematic condition strictly stronger than the Newtonian limit — and uniquely $\lambda = -1$ ([`PG3`](../part7-michell-pg/pg3-newtonian-infall.md)). Visser reported the agreement as "unexplained"; the audit locates the explanation as the selector hiding inside the method.

**Kassner (2015).** *Construction:* an enlarged weak-field ansatz. *Solution set:* leaves one nonlinear coefficient free — which is $\lambda$. *Selector:* fits that coefficient to Mercury's perihelion. *What it adds:* an observational datum, entering through $\beta = \lambda + 2$ ([`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md)). Honest and explicit — this is a *stated* selection, which is exactly how a derivation should look once audited.

Notice the pattern the audit exposes: the ingredient a route adds is precisely one of the book's three selectors — a kinematic demand, an energy convention, or a measurement — or else the route is merely building. Nothing else ever happens.

## The two ways an audit ends

Run the three questions to completion and a derivation resolves into exactly one of two honest verdicts:

- **It builds.** It characterizes (part of) the solution set and adds no selector. Fine — but then it has *not* derived $X$ uniquely, and any claim that it did is the error. Shuler (2018) builds three members and, read correctly, claims no more ([`CORE5`](../part3-building-the-family/core5-distinguished-members.md)).
- **It selects, with a named ingredient.** It adds a stated condition that narrows the set to $X$. Fine — but then the *content* of the derivation is that ingredient, and its persuasiveness is exactly the persuasiveness of the ingredient, no more. If the ingredient is a convention (as in the energy accounting), the "selection" inherits the convention's arbitrariness ([`EPI2`](epi2-identities-not-measurements.md)).

A derivation that fits *neither* — that reaches a unique $X$ from minimal assumptions with no added ingredient — is, when the construction is provably complete, impossible. If you think you have one, you have missed a selector. Go find it.

## Simpler on-ramp

Think of a magic trick where the magician "guesses" your card. The honest description has two separate parts: the *setup* (a full deck — any card is possible) and the *force* (the sleight that made you pick the one card). A spectator who forgets the force concludes the magician read their mind. The paper's method is refusing to forget the force. First it insists on seeing the whole deck — proving that the plain assumptions really do leave every card on the table (the family). Then, whenever a "derivation" pulls out the Schwarzschild card, it asks: *what forced this one?* Sometimes the answer is an honest, stated rule ("we matched Mercury"). Sometimes the force was hidden in how the trick was set up ("we quietly demanded exact Newtonian falling"). Either way, once you name the force, the mystery — "how did minimal assumptions produce a unique answer?" — dissolves. They didn't. Something picked.

## Check your understanding

1. What makes the completeness of the family (the classification theorem) essential to this audit method?
2. A derivation reaches Schwarzschild and states no assumption beyond the base four. What have you learned before reading a single line of its algebra?
3. Distinguish the Rindler/Gruber result from this paper's, in terms of build vs. select.
4. Why is "it selects, with a named ingredient" not a criticism of a derivation?

<details>
<summary>Answers</summary>

- **1.** Because it proves the base assumptions permit a whole continuum of answers. Any derivation reaching one specific answer must therefore be adding information — the audit can assert this with certainty, not just suspicion.
- **2.** That it must contain a smuggled selector, since the base four provably do not determine $\lambda$. You know a hidden ingredient exists before you find it.
- **3.** Rindler/Gruber established *negatively* that the usual ingredients don't determine the metric (counterexamples, no-go). This paper establishes *constructively* what they build (the complete family) and thereby measures exactly what any selection must add. Same fact, from "insufficient" to "here is the sufficient measuring stick."
- **4.** Because selecting with a stated ingredient is how correct derivations work. The criticism is reserved for *hiding* the ingredient or for pretending the base assumptions forced the answer. A named selector is honest; the derivation's strength is then just the ingredient's strength.

</details>

## What the paper claims here

This tutorial grounds the paper's central methodological claim (§1, §7–8): that the static assumptions determine a complete family rather than a unique exterior, and that the historical derivations differ because they use non-identical assumptions — so the productive question is "what does the specified common construction determine *before* any selection?" Faithful scope: the paper frames its completeness as relative to (I1)–(I4) and its uniqueness as "within this family"; it does not claim the added ingredients are wrong, only that they must be named. The elevation of this into a general "audit any simple derivation" procedure, and the card-trick and grammar analogies, are the book's pedagogy built directly on the paper's method and its §7.1 catalogue.

---
**Path navigation:** ← [EPI2 — identities are not measurements](epi2-identities-not-measurements.md) · [next: OUT1 — the self-coupling bootstrap](out1-self-coupling-bootstrap.md) →
**See also:** [`SYN1`](syn1-century-of-shortcuts.md), [`HIST1`](../part7-michell-pg/hist1-michell-laplace.md), [`CORE4`](../part3-building-the-family/core4-classification-theorem.md), [`EPI2`](epi2-identities-not-measurements.md), [`MAP`](../part0-orientation/map.md)
