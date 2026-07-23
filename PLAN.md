# Tutorial Book Plan — *What the Static Assumptions Determine*

A hyperlinked book of general relativity tutorials, built around one paper:
the derivation of the one-parameter metric family

$$A_\lambda(r) = \left(1 + \lambda\,\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda = A_\lambda^{-1}, \qquad r_s = \frac{2GM}{c^2},$$

with Schwarzschild recovered at $\lambda = -1$.

**Format decisions (locked):**
- **Fully self-contained.** The book teaches everything from "what is a metric"
  upward. A reader with calculus and freshman physics can start cold.
- **Prose + math only.** No code, no notebooks. Derivations are worked in text.
- **Hyperlinked, multi-path.** One dependency graph of tutorials; several
  curated reading routes ("paths") through it for different goals.

**Audience calibration.** Primary reader is a strong CS-researcher-type: comfortable
with abstraction, proofs, underdetermination, and representation/gauge freedom,
but *not* assumed to know differential geometry or GR. Each tutorial has an
optional **"Simpler on-ramp"** hook the reader can request/expand when a section
moves too fast. The connective theme throughout is **epistemic**: *specify the
assumptions, characterize the entire solution set, then account precisely for what
each extra condition adds.*

---

## 1. The book's spine (why it's shaped like this)

The paper is, at heart, an **underdetermination story**, and the book inherits its arc:

1. **Build** — four static assumptions determine a *complete* one-parameter family,
   not a unique metric. $\lambda$ is exposed as a *representation choice* (which
   potential variable closes the flux law), not a fact about gravity.
2. **Sign switch** — $\lambda < 0 \iff$ a finite-radius zero exists; the parameter
   silently controls causal structure.
3. **First selector fails** — energy accounting is circular if read off the
   equation, and its honest operational form gives a *convention-bound* interval
   $[-\tfrac14, \tfrac14]$ that **excludes** Schwarzschild.
4. **Second selector works** — $\beta = \lambda + 2$; Mercury's $\beta \approx 1$
   selects $\lambda = -1$ and simultaneously *falsifies* the accounting interval.
5. **Explain the old coincidence** — Painlevé–Gullstrand form makes Schwarzschild's
   infall exactly Newtonian, so Michell's 1784 number is a *downstream property* of
   the selected metric, not a valid derivation.
6. **Synthesize** — every historical shortcut is "build the family" or "select a
   member with an added ingredient."

Every core tutorial ties back to this arc so the reader never loses the thread.

---

## 2. Parts and tutorials (the table of contents)

Stable IDs (e.g. `F3`, `PPN2`) are permanent anchors for cross-links; titles may
change. Each tutorial stub below lists: **Goal · Prereqs · You'll derive/learn ·
Grounds (paper §) · Cross-links.**

### Part 0 — Orientation
- **`INTRO` — How to read this book.** The three-selector map, the path chooser,
  what "self-contained" and "prose-only" mean here, notation conventions.
  · *Grounds:* whole paper · *Links:* every path entry point.
- **`MAP` — The big picture in one page.** The family, the three selectors
  (accounting / observation / kinematics), which ones actually work. A spoiler-y
  overview the reader can return to. · *Grounds:* Abstract, §1, §7–8.

### Part I — Mathematical & Physical Foundations *(fully self-contained)*
- **`F1` — What is a metric?** Line element, measuring distance/time, index and
  summation notation, signature $(-,+,+,+)$, $g_{\mu\nu}$. · *You'll learn:* read
  $ds^2$ as a machine for proper time and length. · *Links:* `F3`, `CORE0`.
- **`F2` — Vectors, one-forms, tensors, coordinates.** Just enough tensor algebra;
  coordinate change as relabeling; what's invariant vs. representation-dependent.
  *(Sets up the book's recurring "representation vs. fact" theme.)* · *Links:* `F4`, `PPN2`.
- **`F3` — Special relativity as flat spacetime.** Minkowski metric, proper time,
  light cones, why $-g_{tt}$ is a clock rate. · *Links:* `F6`, `PG1`.
- **`F4` — Flat space in curvilinear coordinates.** Spherical coordinates, the
  meaning of $r^2 d\Omega^2$, **areal radius** (a sphere at fixed $r$ has area
  $4\pi r^2$). · *Grounds:* §2 ansatz · *Links:* `SYM1`, `PG1`.
- **`F5` — Geodesics: how things move.** The geodesic equation, conserved
  quantities from symmetry, effective potentials for orbits (used later for
  perihelion precession). · *Links:* `PPN4`, `S3`.
- **`F6` — The Newtonian limit.** How $-g_{tt} \approx 1 + 2\Phi/c^2$ emerges;
  why $\Phi = -GM/r$ fixes the leading metric term; the mass scale $r_s$. · *Grounds:* §2 (I1) ·
  *Links:* `CORE1`, `WEAK1`.
- **`SYM1` — Static, spherically symmetric metrics.** Why symmetry forces the
  $-A(r)c^2dt^2 + B(r)dr^2 + r^2d\Omega^2$ form; what "static" and "asymptotically
  flat" mean precisely. · *Grounds:* §2 · *Links:* `CORE0`, `S1`.
- **`F7` — Curvature, briefly.** Riemann/Ricci/Kretschmann at the level needed to
  say "invariant that diverges = real singularity." · *Grounds:* §3 caveat ·
  *Links:* `ZERO2`, `S4`.
- **`GAUSS1` — Gauss's law, flux, and the radial Laplacian.** The operator
  $\Delta = \frac{1}{r^2}\frac{d}{dr}(r^2\frac{d}{dr})$, why field strength
  $\propto 1/r^2$, flux through a sphere. **Explicit caveat:** this is the
  *flat-space radial* operator, not the Laplace–Beltrami operator of a curved
  slice. · *Grounds:* §2 (I2) · *Links:* `CORE1`.
- **`ENE1` — Newtonian gravitational potential energy & self-energy.** Assembly
  work, the shell theorem, the two equivalent energy densities
  $-\frac{|\nabla\Phi|^2}{8\pi G}$ vs. $\frac12\rho\Phi$ and why they're
  interchangeable (integration by parts + field equation). The localization
  ambiguity, in miniature, before any GR. · *Grounds:* §4 · *Links:* `ACC1`, `ACC2`.

### Part II — The Standard Schwarzschild Solution *(so the reader knows the "real" answer)*
- **`S1` — The vacuum Einstein equations (lightweight).** Just enough to state
  "$G_{\mu\nu}=0$ in vacuum" and what it constrains; not a full GR course.
  · *Links:* `S2`, `CORE-CONTRAST`.
- **`S2` — Deriving Schwarzschild the standard way.** The honest vacuum-GR
  derivation, so the reader can *contrast* the paper's shortcut against it.
  · *Grounds:* §2.5 · *Links:* `CORE4`.
- **`S3` — Properties of Schwarzschild.** Horizon at $r_s$, redshift, orbits,
  the classic tests as GR predicts them. · *Links:* `PPN3`, `PG3`.
- **`S4` — Coordinate vs. curvature singularities.** Why $r_s$ is a coordinate
  artifact (finite invariants) but $r=0$ is real; how to tell. · *Grounds:* §3
  caveat, §6 · *Links:* `ZERO2`, `PG1`.

### Part III — Building the Family *(paper §2 — the mathematical heart)*
- **`CORE0` — The four assumptions in common language.** (I1) Newtonian limit,
  (I2) areal-coordinate flux law, (I3) reciprocity $AB=1$, (I4) constant nonlinear
  coefficient. Stated as a *specification* whose solution set we will characterize.
  · *Grounds:* §2.1 · *Links:* all of Part III.
- **`CORE1` — The flux law and the freedom in the potential variable.** Why (I1)–(I3)
  leave "unrestricted functional freedom" in which $V(A)$ obeys the Gauss law; the
  crux that makes the family non-unique. · *Grounds:* §2.1–2.2 · *Links:* `CORE2`.
- **`CORE2` — The logarithmic variable and the closure ODE.** $s=\ln A$; the chain
  rule $\Delta V = F'\Delta s + F''(s')^2$; (I4) $\Rightarrow -F''/F' = \lambda$
  constant $\Rightarrow \Delta s = \lambda (s')^2$. **The key reveal:** $\lambda$
  is a property of the chosen closure, not the geometry. · *Grounds:* §2.2–2.3 ·
  *Links:* `EPI1`.
- **`CORE3` — Solving the closure: the essential variable $A^{-\lambda}$.**
  $F'' = -\lambda F' \Rightarrow V \propto A^{-\lambda}$ (and $\ln A$ at
  $\lambda=0$). · *Grounds:* §2.3.
- **`CORE4` — Integration and the classification theorem.**
  $\Delta(A^{-\lambda})=0 \Rightarrow A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$;
  boundary conditions; completeness ("unique **within this family**").
  · *Grounds:* §2.4.
- **`WEAK1` — Weak-field degeneracy.** $A_\lambda = 1 - x + \frac{1+\lambda}{2}x^2 + \dots$;
  members first differ at $O(x^2)$; Schwarzschild's expansion terminates at first
  order (a *coordinate* statement). Foreshadows $\gamma$/$\beta$. · *Grounds:* §2.6.
- **`CORE5` — Distinguished members & Shuler.** $\lambda=-1,0,+1$ table; the
  $\lambda\to0$ exponential as the *continuous bridge*; Shuler's three metrics as
  points on the continuum ($n=2\lambda$). · *Grounds:* §2.5.
- **`CORE-CONTRAST` — Shortcut vs. real derivation.** Side-by-side: what the four
  assumptions buy vs. what full vacuum GR buys. · *Links:* `S2`.

### Part IV — Structure of the Family *(paper §3)*
- **`ZERO1` — Finite-radius zeros and the sign of $\lambda$.**
  $A_\lambda = 0$ at $r_0 = -\lambda r_s$; positive iff $\lambda<0$; horizonless for
  $\lambda\ge0$. · *Grounds:* §3.
- **`ZERO2` — When is a zero a horizon?** The paper's restraint: a vanishing
  $g_{tt}$ is necessary, not sufficient. Contrast members via curvature invariants;
  distinguish true horizon (Schwarzschild) from possibly-singular zeros elsewhere.
  *(Goes one careful step past the paper.)* · *Grounds:* §3 caveat · *Links:* `F7`, `S4`.

### Part V — Can Energy Accounting Pick $\lambda$? *(paper §4)*
- **`ACC0` — The question.** "Gravitational energy should gravitate" as a candidate
  selector; the Nordtvedt effect as real-world motivation. · *Grounds:* §4 intro.
- **`ACC1` — The circularity trap (self-consistency lemma).** Defining field
  density by reading the nonlinear term off the equation you're solving *for* that
  term is circular — true for every $\lambda$. **Framed for CS readers as a
  question-begging definition / an identity mistaken for a measurement.**
  · *Grounds:* §4.1 · *Links:* `EPI2`.
- **`ACC2` — The invariant assembly energy.** Two shells, quasi-static lowering,
  winch work $W = Gm_1m_2/b$, so $E_{\rm int} = -U$ — convention-independent.
  · *Grounds:* §4.2 · *Links:* `ENE1`.
- **`ACC3` — The gradient-local field cross term.** Shell theorem localizes the
  cross term to $r>b$; the integral gives $E_{\rm field,cross} = 4\lambda U$.
  · *Grounds:* §4.3.
- **`ACC4` — Matter conventions and the bound.** Local ($f=0$) vs. asymptotic
  ($f=1$) rest energy; $\lambda = \frac{2f-1}{4}$; the interval $[-\tfrac14,\tfrac14]$;
  Schwarzschild would need $f=-\tfrac32$. **Honest caveat:** $0\le f\le1$ is an
  *assumption*, not a theorem. · *Grounds:* §4.4–4.5.
- **`ACC5` — The factor of four.** $u_{-1} = 4u_N$; what it does and doesn't mean
  (the *total* is still $-U$). · *Grounds:* §4.6.
- **`ACC6` — Energy has no address.** Localization conventions in Newtonian gravity
  and GR (pseudotensors, quasi-local energy: Komar/ADM/Bondi as *further reading*).
  Why the split is gauge-like. · *Grounds:* §4.2, §4.7 · *Links:* `EPI2`.

### Part VI — Observation Picks $\lambda$ *(paper §5)*
- **`PPN1` — The PPN formalism, gently.** $\gamma$ = space curvature per unit
  potential; $\beta$ = nonlinearity of the time–time part / superposition; GR's
  $\gamma=\beta=1$. · *Grounds:* §5.1.
- **`PPN2` — Areal vs. isotropic coordinates.** The transformation
  $r=\rho(1+k_1 w + k_2 w^2)$; why PPN wants isotropic form; matching yields
  $k_1=\tfrac12$, $k_2=\frac{1-4a_2}{16}$. · *Grounds:* §5.1.1 · *Links:* `F4`.
- **`PPN3` — $\gamma=1$, $\beta=\lambda+2$.** The derivation and the punchline
  identity: the closure coefficient $\lambda$ *is* the PPN nonlinearity $\beta-2$.
  · *Grounds:* §5.1.1–5.2.
- **`PPN4` — The classical tests, sorted by parameter.** Redshift (Newtonian term,
  blind), light bending + Shapiro delay ($\gamma$, blind), perihelion precession
  ($\gamma$ **and** $\beta$, *sensitive*). Why the family survived until Mercury.
  · *Grounds:* §5.3 · *Links:* `F5`, `S3`.
- **`PPN5` — Perihelion precession & the numbers.** The $\frac{2+2\gamma-\beta}{3}
  = \frac{2-\lambda}{3}$ factor; the $\lambda$-vs-precession table (43″ → 14″); the
  accounting interval predicts 25″–32″ and is *falsified*. · *Grounds:* §5.3.
- **`PPN6` — From $\beta$ to $\lambda$: reading constraints critically.**
  $\lambda+1=\beta-1 \lesssim 10^{-4}$; what LLR+Cassini and INPOP20a *do and
  don't* assume; order-of-magnitude honesty. · *Grounds:* §5.4.
- **`PPN7` — $\beta<2$ and the horizon.** Fuses §3 and §5: the same measurement
  that selects Schwarzschild also implies a finite-radius zero exists. · *Grounds:*
  §5.5 · *Links:* `ZERO1`.

### Part VII — Michell, Painlevé–Gullstrand, and the Coincidence *(paper §6)*
- **`PG1` — Painlevé–Gullstrand coordinates & the river model.** The time shift,
  flat spatial slices, $v = c\sqrt{1-A}$, the "river of space" picture (with the
  caveat that $v$ is a coordinate shift, not a material flow). · *Grounds:* §6.1 ·
  *Links:* `F4`, `S4`.
- **`PG2` — Where did the curvature go?** Trading spatial curvature for the mixed
  $2v\,dr\,dT$ term; same invariant, different representation. **A direct echo of
  the `CORE2` "$\lambda$ is a representation choice" theme.** · *Grounds:* §6.1 ·
  *Links:* `EPI1`.
- **`PG3` — The unique Newtonian infall profile.** $\frac12 v^2 = GM/r$ holds *at
  every radius* only for $\lambda=-1$ — a global condition strictly stronger than
  the weak-field limit. · *Grounds:* §6.2.
- **`PG4` — Horizons as light-cone tipping.** $dr/dT = -v \pm c$; outgoing light
  freezes at $v=c$; the clearest first definition of a horizon; why $\lambda\ge0$
  members never reach it. · *Grounds:* §6.3 · *Links:* `ZERO1`.
- **`HIST1` — Michell & Laplace: right number, wrong reason.** The 1784 dark-star
  calculation; the corrected logical direction
  (observation $\to \lambda=-1 \to v^2=2GM/r \to (v=c)\to r_s$); the coincidence
  *explained*, not vindicated. · *Grounds:* §6.4 · *Links:* `EPI3`.
- **`HIST2` — The factor of two in light bending.** Time coefficient alone gives
  $\gamma=0$ and *half* the deflection (Einstein 1911 vs. 1915); why the rest of
  the metric matters. · *Grounds:* §6.5 · *Links:* `PPN4`.

### Part VIII — Synthesis & Epistemology *(paper §7–8)*
- **`SYN1` — A century of shortcuts, mapped.** The §7.1 table as a navigational
  hub: for each historical route, *does it build the family or select a member, and
  what does it add?* (Michell, Lenz–Sommerfeld, Visser, Czerniawski, Kassner,
  Shuler, Casadio, Deser/Duff.) · *Grounds:* §7.1 · *Links:* everything.
- **`EPI1` — Representation vs. fact.** The book's throughline: $\lambda$ as gauge/
  closure choice; what coordinate changes preserve. · *Links:* `CORE2`, `PG2`, `F2`.
- **`EPI2` — Identities are not measurements.** Generalizing the self-consistency
  lemma into a transferable reasoning lesson. · *Links:* `ACC1`.
- **`EPI3` — Build vs. select.** How to audit any "simple derivation": separate the
  construction from the selecting condition; name the smuggled assumption.
  · *Links:* `SYN1`, `HIST1`.
- **`OUT1` — Exit ramp: the self-coupling bootstrap.** *Beyond this paper.*
  Deser (1970) / Duff (1973): full field self-consistency forces Schwarzschild
  *dynamically* — the "dynamical information absent from static accounting."
  Pointers into real GR for the reader who asks "but what pins $\lambda=-1$ from
  first principles?" · *Grounds:* §4.7, §7.1.

---

## 3. Reading paths (curated routes through the graph)

The book is one graph; these are recommended traversals. Each path page lists its
tutorials in order with a one-line rationale.

- **`PATH-NEWCOMER` — The full climb.** Part I → II → III → IV → V → VI → VII → VIII.
  Linear, self-contained, no prerequisites assumed. The default.
- **`PATH-FAST` — Physicist's fast path.** Skip Part I (assume metrics/coordinates/
  Newtonian limit); start `CORE0`, run the core arc `CORE* → ZERO* → ACC* → PPN* →
  PG* → SYN*`.
- **`PATH-EPI` — The epistemology path.** For the CS reader who wants the
  underdetermination story above the physics: `MAP → CORE0 → CORE2 → EPI1 → ACC1 →
  EPI2 → PPN3 → EPI3 → HIST1 → SYN1`. Physics tutorials linked as needed but not
  required inline.
- **`PATH-COORDS` — Coordinates & horizons.** `F4 → SYM1 → S4 → ZERO1 → ZERO2 →
  PG1 → PG2 → PG4`. "The same spacetime wears many coordinates."
- **`PATH-OBS` — What experiments actually say.** `F6 → WEAK1 → PPN1 → PPN2 → PPN3
  → PPN4 → PPN5 → PPN6`. Ends at "how a headline constraint is really made."
- **`PATH-HIST` — The history.** `HIST1 → S2 → SYN1 → HIST2 → OUT1`. Michell to the
  modern bootstrap.

---

## 4. Recurring tutorial conventions

Every tutorial page follows a fixed template so the book reads as one work:

1. **One-line goal** and **prerequisites** (as links to tutorial IDs).
2. **Where this sits in the arc** (a one-liner tying to the three-selector spine).
3. **Body:** prose-driven derivation, equations worked in full (no skipped steps
   at core-tutorial level).
4. **"Simpler on-ramp"** — a collapsible/linked gentler version the reader can pull
   in on request (satisfies "I'll ask for simpler versions as I need them").
5. **Check-your-understanding** — a few conceptual questions (no code), answers linked.
6. **What the paper claims here** — the exact section grounded, with the paper's own
   caveats quoted where it matters (the book *inherits the paper's restraint*).
7. **Cross-links** — "prev / next in path," plus lateral links.

**Editorial rules the book commits to (mirroring the paper's discipline):**
- Never call a zero of $g_{tt}$ a "horizon" without the invariant check.
- Always mark a selector as *build* vs. *select* and name what it adds.
- Distinguish *representation-dependent* statements from *invariant* ones explicitly.
- Quote observational bounds at the honesty level the paper uses (order of magnitude,
  stated assumptions).

---

## 5. Proposed repository structure

```
/
├── README.md                     # = INTRO, the landing page + path chooser
├── PLAN.md                       # this document
├── paths/
│   ├── newcomer.md  fast.md  epistemology.md  coordinates.md  observation.md  history.md
├── part0-orientation/
│   └── intro.md  map.md
├── part1-foundations/
│   └── f1-metric.md … ene1-self-energy.md
├── part2-schwarzschild/
│   └── s1-vacuum-einstein.md … s4-singularities.md
├── part3-building-the-family/
│   └── core0 … core5, weak1, core-contrast
├── part4-family-structure/
│   └── zero1-zeros.md  zero2-when-horizon.md
├── part5-energy-accounting/
│   └── acc0 … acc6
├── part6-ppn-observation/
│   └── ppn1 … ppn7
├── part7-michell-pg/
│   └── pg1 … pg4, hist1, hist2
├── part8-synthesis/
│   └── syn1, epi1, epi2, epi3, out1
└── reference/
    ├── notation.md               # signature, symbols, index conventions
    ├── glossary.md               # areal radius, PPN, horizon, pseudotensor, …
    └── bibliography.md           # Michell, Lenz/Sommerfeld, Rindler, Gruber et al.,
                                  # Visser, Kassner, Shuler, Deser, Duff, Will, …
```

- **Hyperlinking:** every tutorial is a Markdown file; cross-links use relative
  paths anchored by the stable IDs above. Path pages are thin ordered link-lists.
  The three figures from the paper (family curves, $\beta$-dictionary, PG river
  ledger) are described in prose (`WEAK1`/`ZERO1`, `PPN3`, `PG3`) since the book is
  code/figure-free; each notes the qualitative shape the reader should picture.
- **Landing page (`README.md`)** opens with the one-page `MAP`, then the path
  chooser, so a returning reader re-enters at the right altitude.

---

## 6. Suggested build order (when we start writing)

Not the reading order — the *authoring* order, chosen so each written tutorial can
be validated against the paper before dependents are built:

1. **Backbone first:** `MAP`, `CORE0`–`CORE5`, `WEAK1` (Part III). This is the
   verifiable heart; everything else supports or extends it.
2. **Selectors:** `ZERO1`, `ACC1`–`ACC4`, `PPN1`–`PPN5`, `PG1`–`PG4`. The three
   selection stories.
3. **Foundations backfill:** Part I, written *to serve* the backbone (so we teach
   exactly the prerequisites the core actually uses — no orphan math).
4. **Contrast & context:** Part II (`S1`–`S4`), synthesis/epistemology (Part VIII).
5. **Polish layer:** on-ramps, check-your-understanding, glossary, bibliography,
   path pages, cross-link pass.

---

## 7. Open questions to resolve before/while authoring

- **Depth of Part II (standard Schwarzschild).** Full-ish derivation, or a compact
  "here's the real answer, trust it for now" with a pointer? (Affects how much
  tensor calculus Part I must teach.)
- **How much real GR to gesture at in `OUT1`.** A paragraph, or a genuine mini-path
  toward the Einstein equations and the spin-2 bootstrap?
- **On-ramp mechanism.** Separate `*-simple.md` companion files, or inline
  collapsible sections? (Prose-only, so likely companion files linked at the top.)
- **Notation lock.** Signature, whether to keep $c$ explicit (paper does) or ever
  go to $c=1$. Recommend: keep $c$ explicit throughout to match the paper.
```
```

*This is a first draft of the plan, meant to be revised. Nothing in the book itself
has been written yet.*
