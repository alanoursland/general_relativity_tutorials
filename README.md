# What the Static Assumptions Determine

*A hyperlinked tutorial book on the Schwarzschild metric, its one-parameter family
of "static-assumption" cousins, and what it actually takes to select one of them.*

## What this book is

This book is a single sustained argument, built as a graph of self-contained
tutorials rather than a linear text. It teaches general relativity from "what is
a metric" upward — no differential geometry assumed — and it is prose and math
only: no code, no notebooks, no computational exercises. Every tutorial ends with
a "Simpler on-ramp" for when the main text moves too fast, a handful of conceptual
"Check your understanding" questions, and an explicit accounting of exactly what
the source paper does and does not claim.

**The thesis, in one paragraph.** Four static, spherically symmetric assumptions —
a Newtonian limit, an exact vacuum flux law in *some* monotonic potential variable,
the reciprocal condition $g_{tt}g_{rr}=-1$, and a constant nonlinear coefficient —
do **not** pin down the Schwarzschild metric. They pin down a *complete
one-parameter family*
$$A_\lambda(r) = \left(1+\lambda\,\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda = A_\lambda^{-1}, \qquad r_s=\frac{2GM}{c^2},$$
of which Schwarzschild ($\lambda=-1$) is only one member. $\lambda$ turns out to be
a property of *which variable you chose to make the flux law exact in* — a
representation/closure choice, not a fact read off the geometry. Selecting
$\lambda=-1$ takes information the static construction doesn't contain: measuring
the post-Newtonian parameter $\beta=\lambda+2$ (Mercury's perihelion) does the job
cleanly; a naive energy-accounting argument does not (it gives the *wrong* answer,
excluding Schwarzschild); and in Painlevé–Gullstrand coordinates, $\lambda=-1$ is
exactly the condition under which Michell's 1784 Newtonian escape-velocity
coincidence becomes exact. The book's throughline is epistemic: **specify the
assumptions, characterize the entire solution set they permit, then account
precisely for what each extra condition adds.**

For the full rationale behind this shape, see [PLAN.md](PLAN.md) (the table of
contents and reading paths) and [KNOWLEDGE_MAP.md](KNOWLEDGE_MAP.md) (which
reverse-engineers the competence the argument requires and ranks where the real
difficulty lives) — "about this book."

**Start here:** [`part0-orientation/intro.md`](part0-orientation/intro.md) — how to
read this book — and [`part0-orientation/map.md`](part0-orientation/map.md) — the
whole argument on one page, for orientation or for returning readers.

---

## Choose a path

The book is one dependency graph; these are curated traversals through it for
different goals. Every path page is a short ordered list of links with a
one-line rationale for each stop.

| Path | For readers who... | Start |
|---|---|---|
| [**The full climb**](paths/newcomer.md) | want the complete self-contained course, foundations through synthesis, in one line | [`INTRO`](part0-orientation/intro.md) |
| [**Physicist's fast path**](paths/fast.md) | already know metrics, coordinates, and the Newtonian limit and want the argument's spine | [`CORE0`](part3-building-the-family/core0-four-assumptions.md) |
| [**The epistemology path**](paths/epistemology.md) | want the underdetermination story above the physics — representation vs. fact, build vs. select | [`MAP`](part0-orientation/map.md) |
| [**Coordinates & horizons**](paths/coordinates.md) | want to see one spacetime wear many coordinate systems and learn what a horizon really is | [`F4`](part1-foundations/f4-curvilinear-coordinates.md) |
| [**What experiments actually say**](paths/observation.md) | want the observational story: PPN, the classical tests, how a headline constraint is really made | [`F6`](part1-foundations/f6-newtonian-limit.md) |
| [**The history**](paths/history.md) | want Michell to the modern self-coupling bootstrap, with the myths corrected | [`HIST1`](part7-michell-pg/hist1-michell-laplace.md) |

---

## Full table of contents

### Part 0 — Orientation
- [`INTRO` — How to read this book](part0-orientation/intro.md)
- [`MAP` — The big picture in one page](part0-orientation/map.md)

### Part I — Mathematical & physical foundations *(fully self-contained)*
- [`F1` — What is a metric?](part1-foundations/f1-metric.md)
- [`F2` — Vectors, one-forms, tensors, coordinates](part1-foundations/f2-tensors.md)
- [`F3` — Special relativity as flat spacetime](part1-foundations/f3-special-relativity.md)
- [`F4` — Flat space in curvilinear coordinates](part1-foundations/f4-curvilinear-coordinates.md)
- [`F5` — Geodesics: how things move](part1-foundations/f5-geodesics.md)
- [`F6` — The Newtonian limit](part1-foundations/f6-newtonian-limit.md)
- [`SYM1` — Static, spherically symmetric metrics](part1-foundations/sym1-static-spherical.md)
- [`F7` — Curvature, briefly](part1-foundations/f7-curvature.md)
- [`GAUSS1` — Gauss's law, flux, and the radial Laplacian](part1-foundations/gauss1-flux-laplacian.md)
- [`ENE1` — Newtonian gravitational potential energy & self-energy](part1-foundations/ene1-self-energy.md)

### Part II — The standard Schwarzschild solution *(so you know the "real" answer)*
- [`S1` — The vacuum Einstein equations, lightweight](part2-schwarzschild/s1-vacuum-einstein.md)
- [`S2` — Deriving Schwarzschild the standard way](part2-schwarzschild/s2-deriving-schwarzschild.md)
- [`BIRK` — Birkhoff's theorem](part2-schwarzschild/birkhoff.md)
- [`S3` — Properties of Schwarzschild](part2-schwarzschild/s3-properties.md)
- [`S4` — Coordinate vs. curvature singularities](part2-schwarzschild/s4-singularities.md)

### Part III — Building the family *(the mathematical heart)*
- [`CORE0` — The four assumptions in common language](part3-building-the-family/core0-four-assumptions.md)
- [`CORE1` — The flux law and the freedom in the potential variable](part3-building-the-family/core1-flux-freedom.md)
- [`CORE2` — The logarithmic variable and the closure ODE](part3-building-the-family/core2-log-variable-closure.md)
- [`CORE3` — Solving the closure: the essential variable $A^{-\lambda}$](part3-building-the-family/core3-essential-variable.md)
- [`CORE4` — Integration and the classification theorem](part3-building-the-family/core4-classification-theorem.md)
- [`WEAK1` — Weak-field degeneracy](part3-building-the-family/weak1-weak-field-degeneracy.md)
- [`CORE5` — Distinguished members & Shuler](part3-building-the-family/core5-distinguished-members.md)
- [`CORE-CONTRAST` — Shortcut vs. real derivation](part3-building-the-family/core-contrast.md)

### Part IV — Structure of the family
- [`ZERO1` — Finite-radius zeros and the sign of $\lambda$](part4-family-structure/zero1-finite-radius-zeros.md)
- [`ZERO2` — When is a zero a horizon?](part4-family-structure/zero2-when-is-a-zero-a-horizon.md)

### Part V — Can energy accounting pick $\lambda$?
- [`ACC0` — The question](part5-energy-accounting/acc0-the-question.md)
- [`ACC1` — The circularity trap](part5-energy-accounting/acc1-circularity.md)
- [`ACC2` — The invariant assembly energy](part5-energy-accounting/acc2-invariant-assembly-energy.md)
- [`ACC3` — The gradient-local field cross term](part5-energy-accounting/acc3-field-cross-term.md)
- [`ACC4` — Matter conventions and the bound](part5-energy-accounting/acc4-matter-conventions-bound.md)
- [`ACC5` — The factor of four](part5-energy-accounting/acc5-factor-of-four.md)
- [`ACC6` — Energy has no address](part5-energy-accounting/acc6-energy-localization.md)
- [`GRSOL` — Are these GR solutions?](part5-energy-accounting/grsol-are-these-gr-solutions.md)

### Part VI — Observation picks $\lambda$
- [`PPN1` — The PPN formalism, gently](part6-ppn-observation/ppn1-ppn-formalism.md)
- [`PPN2` — Areal vs. isotropic coordinates](part6-ppn-observation/ppn2-areal-isotropic.md)
- [`PPN3` — $\gamma=1$, $\beta=\lambda+2$](part6-ppn-observation/ppn3-gamma-beta.md)
- [`PPN4` — The classical tests, sorted by parameter](part6-ppn-observation/ppn4-classical-tests.md)
- [`PPN5` — Perihelion precession & the numbers](part6-ppn-observation/ppn5-perihelion-precession.md)
- [`PPN6` — From $\beta$ to $\lambda$: reading constraints critically](part6-ppn-observation/ppn6-reading-constraints.md)
- [`PPN7` — $\beta<2$ and the horizon](part6-ppn-observation/ppn7-beta-and-horizon.md)

### Part VII — Michell, Painlevé–Gullstrand, and the coincidence
- [`PG1` — Painlevé–Gullstrand coordinates & the river model](part7-michell-pg/pg1-painleve-gullstrand.md)
- [`PG2` — Where did the curvature go?](part7-michell-pg/pg2-where-did-curvature-go.md)
- [`PG3` — The unique Newtonian infall profile](part7-michell-pg/pg3-newtonian-infall.md)
- [`PG4` — Horizons as light-cone tipping](part7-michell-pg/pg4-horizons-light-cones.md)
- [`HIST1` — Michell & Laplace: right number, wrong reason](part7-michell-pg/hist1-michell-laplace.md)
- [`HIST2` — The factor of two in light bending](part7-michell-pg/hist2-factor-of-two.md)

### Part VIII — Synthesis & epistemology
- [`SYN1` — A century of shortcuts, mapped](part8-synthesis/syn1-century-of-shortcuts.md)
- [`EPI1` — Representation vs. fact](part8-synthesis/epi1-representation-vs-fact.md)
- [`EPI2` — Identities are not measurements](part8-synthesis/epi2-identities-not-measurements.md)
- [`EPI3` — Build vs. select](part8-synthesis/epi3-build-vs-select.md)
- [`OUT1` — Exit ramp: the self-coupling bootstrap](part8-synthesis/out1-self-coupling-bootstrap.md)

### Reference
- [Notation](reference/notation.md)
- [Glossary](reference/glossary.md)
- [Bibliography](reference/bibliography.md)

---

*About this book:* [PLAN.md](PLAN.md) is the design document (the spine argument,
the full tutorial table of contents with grounding sections, the six paths, and
the repository layout). [KNOWLEDGE_MAP.md](KNOWLEDGE_MAP.md) reverse-engineers the
competence the source paper's argument demonstrably requires, names the five
genuine conceptual cruxes, and ranks where the real difficulty lives — read it if
you want to know *why* the book is shaped this way, not just *what* is in it.
