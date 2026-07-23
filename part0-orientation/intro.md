# How to Read This Book

> **Tutorial `INTRO`** · Part 0 · **Goal:** orient you to the book's one idea, its three selectors, and the reading path that fits you · **Prereqs:** none — start cold.

**Where this sits in the arc.** This is the front door. The whole book turns on a single move: *specify a set of assumptions, characterize the entire set of solutions they allow, and only then ask what extra information picks one solution out.* Everything downstream — building a metric family, watching a sign flip a horizon on and off, three attempts to pin one parameter — is that move applied to one famous question in general relativity. This page tells you what the book is doing and how to move through it.

## The one thing the book is about

There is a standard object in general relativity called the **Schwarzschild metric** — the geometry outside a spherical, non-spinning mass. It is what a black hole's exterior looks like. Textbooks derive it from the Einstein field equations, and for a century people have also offered *shortcut* derivations: quick arguments, some predating relativity, that seem to conjure the same answer from Newtonian physics plus a little cleverness.

The paper this book is built on asks a sharper question than "is the shortcut right?" It asks: **what does a specified set of simple, static assumptions actually determine?** The answer is the spine of the book:

$$A_\lambda(r) = \left(1 + \lambda\,\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda = A_\lambda^{-1}, \qquad r_s = \frac{2GM}{c^2}.$$

This is not *a* metric. It is a **one-parameter family** of metrics, one for every value of the number $\lambda$. Schwarzschild is the single member at $\lambda = -1$. The static assumptions build the whole family and do **not** single out $\lambda = -1$. Something *extra* — beyond "static, spherical, Newtonian at infinity" — is always smuggled in when a shortcut appears to land on Schwarzschild. The book's job is to make you able to name that extra thing every time.

If you take one habit away from this book, take this: **separate the construction of the solution set from the condition that selects a member, and name what the selecting condition adds.** That is [`EPI3`](../part8-synthesis/epi3-build-vs-select.md) in a sentence, and it is the method behind every chapter.

## The three-selector map

Once the family is built, the natural question is: *which member is real?* The book examines three candidate ways to answer, and part of its honesty is that they disagree about whether they even can. Keep this table in your head as you read; the [`MAP`](map.md) page expands it.

| Selector | The idea | Verdict |
|---|---|---|
| **Accounting** — gravitational self-energy | "Gravitational energy gravitates; let the field's own energy fix the coefficient." | Confines $\lambda \in [-\tfrac14, +\tfrac14]$ — and this interval **excludes** Schwarzschild ($\lambda=-1$). It also rests on a convention, so it does not truly select. **Fails as a selector.** |
| **Observation** — post-Newtonian $\beta$ | The nonlinear PPN parameter obeys $\beta = \lambda + 2$; measure $\beta$. | Mercury's perihelion and solar-system ranging give $\beta \simeq 1$, hence $\lambda \simeq -1$. **Selects Schwarzschild.** |
| **Kinematics** — Painlevé–Gullstrand infall | Demand the infall speed match the Newtonian $\tfrac12 v^2 = GM/r$ at *every* radius. | Holds only for $\lambda = -1$. **Selects Schwarzschild** — and explains Michell's 1784 dark-star number as a downstream property, not a derivation. |

Two of the three work; one fails in an instructive way. The accounting selector is worth as much attention as the two that succeed, because *how* it fails — a bound that is real but convention-bound, and an interval that observation later falsifies — is the sharpest lesson in the book. That is the payload of [`EPI2`](../part8-synthesis/epi2-identities-not-measurements.md): an identity is not a measurement.

## The path chooser

The book is one dependency graph with several curated routes through it. Pick the one that matches why you are here. Each path page lists its tutorials in order with a one-line rationale.

- **[The full climb](../paths/newcomer.md)** (`newcomer`) — start cold, assume nothing, walk Part I → VIII linearly. The default if you are not sure.
- **[Physicist's fast path](../paths/fast.md)** (`fast`) — you already own metrics, coordinates, and the Newtonian limit; jump straight to the core construction and the selectors.
- **[The epistemology path](../paths/epistemology.md)** (`epistemology`) — you want the underdetermination story above the physics: build vs. select, representation vs. fact, identities vs. measurements. The CS-researcher's route.
- **[Coordinates & horizons](../paths/coordinates.md)** (`coordinates`) — "the same spacetime wears many coordinates": areal, isotropic, Painlevé–Gullstrand, and when a zero of $g_{tt}$ is really a horizon.
- **[What experiments actually say](../paths/observation.md)** (`observation`) — the weak-field expansion, PPN, and how a headline constraint like $|\beta-1|\lesssim 10^{-4}$ is really assembled.
- **[The history](../paths/history.md)** (`history`) — Michell and Laplace to the modern self-coupling bootstrap.

Two of these are the **major paths** most readers should choose between: the [full climb](../paths/newcomer.md) if you want the physics taught from the ground up, and the [epistemology path](../paths/epistemology.md) if you want the reasoning method and will pull in physics as needed. The other four are focused traversals for a specific curiosity.

## What "self-contained" and "prose-only" mean here

**Self-contained.** The book assumes calculus and freshman physics and *nothing about general relativity or differential geometry*. It teaches from "what is a metric" ([`F1`](../part1-foundations/f1-metric.md)) upward, building exactly the machinery the central argument uses — no orphan mathematics. If a derivation needs the radial flux operator, the Newtonian limit, or a second-order coordinate change, there is a foundation tutorial that teaches it first. You should never have to trust a black box.

Because the hardest parts of this book are *conceptual*, not computational, every core tutorial carries a **"Simpler on-ramp"** section: a genuinely gentler pass at the single hardest idea, in plain language, for when the main text moves too fast. Use it freely; it is not a consolation prize.

**Prose-only.** There is no code, there are no notebooks, and there are no plotting scripts or compute-heavy exercises. Every derivation is worked in the text with the algebra shown. The paper's three figures — the family of curves $A_\lambda(r)$, the line $\beta = \lambda + 2$, and the Painlevé–Gullstrand infall profiles — are **described in prose** so you can picture their shape without an image. The "Check your understanding" questions at the end of each tutorial are conceptual; none require a calculation.

## Notation, in one pointer

The book keeps $c$ **explicit** everywhere (it never sets $c=1$), uses signature $(-,+,+,+)$, and uses the paper's symbols: $r_s = 2GM/c^2$ (the mass scale), $x = r_s/r$ (the weak-field expansion variable), $s = \ln A$ (the logarithmic potential), and $\Delta = \frac{1}{r^2}\frac{d}{dr}\!\left(r^2\frac{d}{dr}\right)$ (the *flat-space radial flux operator*, not the Laplace–Beltrami operator of a curved slice — a distinction the book is careful about). Everything is collected in one place: [**reference/notation.md**](../reference/notation.md). Skim it once now; return to it whenever a symbol surprises you.

## Simpler on-ramp

If the table above is a lot at once, here is the whole book in four sentences. There is a famous "answer" in gravity — the geometry outside a heavy ball — and lots of slick ways people claim to reach it. When you write down only the truly minimal assumptions, you don't get *the* answer; you get a whole shelf of possible answers labeled by a dial called $\lambda$, with the famous one sitting at $\lambda = -1$. The book then tries three ways to justify turning the dial to $-1$: one fails (energy accounting), two succeed (a measurement, and a demand that falling match Newton exactly). The lesson that outlives the physics is a thinking skill: whenever someone shows you a "simple derivation," ask which part *built the shelf* and which part *reached for one book on it* — and make them say out loud what the reaching-for assumed.

## Check your understanding

1. The static assumptions "build the family." What would it take, in addition, to "select a member"?
2. Two of the three selectors agree on $\lambda=-1$; one gives a different answer. Which one, and does that make it wrong or just limited?
3. Why does the book keep $c$ explicit instead of setting $c=1$?
4. You are a physicist who already knows the Newtonian limit and PPN. Which path should you take?

<details>
<summary>Answers</summary>

- **1.** An extra ingredient not contained in "static, spherical, asymptotically flat, Newtonian at infinity" — for example, a measurement of the nonlinear PPN parameter $\beta$, or a global kinematic demand (Newtonian infall at every radius). Naming that ingredient is the whole method.
- **2.** The energy-accounting selector gives the interval $[-\tfrac14,\tfrac14]$, which excludes $\lambda=-1$. It is not "wrong": its assembly bookkeeping is correct. It is *limited* — its bound depends on a convention for splitting energy into matter and field, and that split is not unique. See [`EPI2`](../part8-synthesis/epi2-identities-not-measurements.md).
- **3.** To match the source paper's discipline and to keep every formula dimensionally transparent — factors of $c$ mark where relativistic effects enter, e.g. $r_s = 2GM/c^2$.
- **4.** The [fast path](../paths/fast.md), or the [epistemology path](../paths/epistemology.md) if you care more about the reasoning than the machinery.

</details>

## What the paper claims here

This page grounds the paper as a whole — its Abstract, §1 (Introduction), and §7–8 (Discussion and Conclusion). The paper's central claim is deliberately modest and worth stating in its own terms: the static, spherically symmetric, asymptotically flat assumptions determine a **complete one-parameter family**, not a unique exterior; the family **recovers the scale** $r_s = 2GM/c^2$ and **contains** Schwarzschild at $\lambda=-1$ but does **not select** it. Selection requires extra physical or observational information. The paper is scrupulous about scope — "unique" means *unique within this family*, and a zero of $g_{tt}$ is called a horizon only for Schwarzschild. This book inherits that restraint everywhere.

---
**Path navigation:** ← [README (landing page)](../README.md) · [next: MAP — the big picture in one page](map.md) →
**See also:** [`MAP`](map.md), [`EPI3`](../part8-synthesis/epi3-build-vs-select.md), [`SYN1`](../part8-synthesis/syn1-century-of-shortcuts.md), [notation](../reference/notation.md), [PLAN](../PLAN.md)
