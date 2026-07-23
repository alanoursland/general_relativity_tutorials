# A Century of Shortcuts, Mapped

> **Tutorial `SYN1`** · Part 8 · **Goal:** turn the paper's literature table into a navigational hub — for each historical route, decide whether it *builds the family* or *selects a member*, and name what it adds · **Prereqs:** [`CORE4`](../part3-building-the-family/core4-classification-theorem.md), [`PPN3`](../part6-ppn-observation/ppn3-gamma-beta.md), [`PG3`](../part7-michell-pg/pg3-newtonian-infall.md).

**Where this sits in the arc.** This is the synthesis payoff. Having built the family and watched the three selectors, we now walk back through a century of "simple derivations of Schwarzschild" and sort each one with a single question: did it *construct the solution set*, or did it *select a member* — and if it selected, what extra ingredient did it quietly supply? Every entry links to the tutorial where that route's mechanism lives.

## The one question

The paper's §1 diagnosis is that the historical shortcuts "differ because the derivations do not use identical assumptions." That is the entire confusion, resolved. So we ask of each route, in order:

1. **Build or select?** Does it produce the whole one-parameter family $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$ (or an unselected sub-shelf of it), or does it land on one member?
2. **If it selects, what does it add?** Name the ingredient beyond "static, spherical, asymptotically flat, Newtonian at infinity." That ingredient is always the real content.

This is the audit method of [`EPI3`](epi3-build-vs-select.md) applied to real history. The routes below are the paper's §7.1 table, expanded.

## The routes

### Michell (1784) & Laplace — *identifies the scale, no metric*
The founding shortcut: set Newtonian escape velocity equal to $c$, $\tfrac12 v^2 = GM/r$ with $v=c$, and read off $r = 2GM/c^2$. Numerically this is $r_s$. But it uses the Newtonian potential and nonrelativistic kinetic energy far outside their validity, and it produces **no metric at all** — no $A(r)$, no spatial structure, no causal statement. **Verdict: neither build nor select.** It fixes the *scale* $2GM/c^2$ and nothing more. Its number becomes meaningful only *after* Schwarzschild is selected by other means, at which point the Painlevé–Gullstrand infall relation $v^2 = 2GM/r$ makes $v=c$ at $r=r_s$ exact. See [`HIST1`](../part7-michell-pg/hist1-michell-laplace.md) for the corrected logical direction and [`PG3`](../part7-michell-pg/pg3-newtonian-infall.md), [`PG4`](../part7-michell-pg/pg4-horizons-light-cones.md) for why.

### Lenz–Sommerfeld and related (Sommerfeld 1952; Schiff 1960; Tangherlini 1962; Sacks–Ball 1968) — *selects, by extra kinematic/metric assumptions*
This lineage relativistically reinterprets Newtonian motion — energy, momentum, or trajectory arguments dressed in special-relativistic kinematics — to reach Schwarzschild. In the paper's accounting these **supply extra kinematic or metric assumptions** beyond the base four; they do not merely build the family, they add the ingredient that picks $\lambda = -1$. **Verdict: select** (with the selecting assumption often left implicit — exactly the situation [`EPI3`](epi3-build-vs-select.md) teaches you to detect). Rindler (1968, 1969) supplied explicit **counterexamples** to several such arguments, and Gruber–Price–Matthews–Cordwell–Wagner (1988) gave the systematic no-go: the usual ingredients *do not* uniquely determine the metric. The present paper is the constructive complement — it states *what they determine instead* (the family). See [`CORE-CONTRAST`](../part3-building-the-family/core-contrast.md).

### Visser (2005); Czerniawski (2006) — *selects Schwarzschild*
Visser reproduces Schwarzschild from a Newtonian heuristic cast in flat-slice (Painlevé–Gullstrand–type) form, noting the agreement is unexplained; Czerniawski is related. The present paper *explains* the agreement: demanding the exact Newtonian infall profile $v^2 = 2GM/r$ hold at **every** radius is a global condition strictly stronger than the Newtonian limit, and it singles out $\lambda = -1$. **Verdict: select — the added ingredient is the exact-infall (flat-slice) condition.** This is precisely the PG-kinematics selector. See [`PG3`](../part7-michell-pg/pg3-newtonian-infall.md) and [`PG1`](../part7-michell-pg/pg1-painleve-gullstrand.md).

### Kassner (2015, 2017) — *selects, by supplying physical/observational information*
Kassner (2015) builds a weak-field metric from enlarged assumptions and fixes one remaining coefficient using **Mercury's perihelion** — i.e. observational input. Kassner (2017) uses orbital / dust-ball constructions. Both **supply physical or observational information beyond the base assumptions**. In the present framework the coefficient Kassner leaves open *is* $\lambda$, and the perihelion datum fixes it through $\beta = \lambda + 2$. **Verdict: select — the added ingredient is a measurement (or a physical model that stands in for one).** See [`PPN5`](../part6-ppn-observation/ppn5-perihelion-precession.md) and the paper's §5.6 note in [`PPN6`](../part6-ppn-observation/ppn6-reading-constraints.md).

### Shuler (2018) — *builds (exhibits three members of the family)*
Shuler presents Schwarzschild together with two alternatives in a common parameterized form $g_{tt} = -(1 + n\,GM/(rc^2))^{-2/n}$. Setting $n = 2\lambda$, this is exactly the present family, and Shuler's $n = -2, -1, +1$ are $\lambda = -1, -\tfrac12, +\tfrac12$. **Verdict: build — three points on the continuous class**, presented without a selecting principle. This is the closest prior work to the paper's own construction: it *displays* the non-uniqueness rather than resolving it. See [`CORE5`](../part3-building-the-family/core5-distinguished-members.md).

### Kassner (2019) — *selects Schwarzschild among Shuler's*
Kassner (2019) shows that only Schwarzschild satisfies a standard relativistic generalization of Newton's law, thereby selecting among Shuler's alternatives. In the present framework the family exists *before* any such condition, and this is one more selecting principle applied on top of it. **Verdict: select — the added ingredient is the relativistic Newton's-law condition.** The paper's stance: the family "comes before" such conditions, which clarifies that Kassner is choosing, not deriving uniqueness from the base assumptions. See [`CORE5`](../part3-building-the-family/core5-distinguished-members.md).

### Casadio et al. (2018, 2021) — *related bootstrap, not selection within the family*
Casadio and collaborators construct an effective metric from a nonlinear Poisson self-interaction (a bootstrap of the potential). This is **kin to the paper's constructions but does a different job**: it builds an effective metric from a nonlinear model, not the static local-energy assignment of §4, and it is not posed as a selection within the $\lambda$-family. **Verdict: neither — a related but distinct construction.** Flagged so the reader does not mistake it for the §4 accounting selector; contrast with [`ACC3`](../part5-energy-accounting/acc3-field-cross-term.md).

### Deser (1970); Duff (1973) — *stronger dynamical constructions, not selection within the family*
These are the field self-coupling / tree-graph reconstructions: a massless spin-2 field consistently coupled to its own stress–energy is forced, order by order, to full nonlinear general relativity. They are **stronger dynamical constructions** and — crucially — they **do not study selection within the $\lambda$-family**. They supply the *dynamical* information the static accounting of §4 lacks, and in doing so force Schwarzschild from first principles. **Verdict: neither build nor select within this family — they operate one level up, on the field equations themselves.** This is the exit ramp beyond the paper; see [`OUT1`](out1-self-coupling-bootstrap.md) and §4.7's remark that bootstrapped constructions "supply dynamical information absent" from static accounting.

## The pattern

Read the column of verdicts and a shape appears. Exactly two things are ever going on:

- **Building** — Michell's scale, Shuler's three points, the base four assumptions themselves: these *characterize what is possible* and stop there.
- **Selecting** — Lenz–Sommerfeld's kinematics, Visser/Czerniawski's exact infall, Kassner's measurement, Kassner-2019's Newton's-law condition: each *adds one ingredient* and lands on $\lambda = -1$.
- **Operating elsewhere** — Casadio's effective metric and Deser/Duff's dynamical bootstrap sit outside the build/select-within-family frame; they change the *rules* rather than picking from the shelf.

No route is a counterexample to the paper. Each is either a construction of (part of) the family, or a member-selection with a nameable added ingredient, or a move to a different problem entirely. That exhaustiveness *is* the synthesis.

## Simpler on-ramp

Imagine a museum wall of a dozen "proofs that the answer is Schwarzschild," collected over 240 years. It looks like a pile of competing claims. The paper hands you one sorting rule and the pile becomes tidy: some exhibits merely *drew the shelf of possible answers* (Shuler literally lines up three of them; Michell just measures the shelf's width). Others *pointed at one book* — but each did so by carrying in a rule from outside: "make falling exactly Newtonian," "match Mercury," "obey this relativistic force law." Once you demand that each exhibit say out loud what it carried in, none of them conflict; they were answering slightly different questions all along.

## Check your understanding

1. Shuler and Michell are both "build," but in very different senses. How do they differ?
2. Visser's derivation "just works" and he says the agreement is unexplained. What is the explanation, in the paper's terms?
3. Why are Deser/Duff and Casadio placed *outside* the build/select dichotomy rather than as selectors?
4. A route lands on Schwarzschild but never states an assumption beyond the base four. What should you suspect?

<details>
<summary>Answers</summary>

- **1.** Michell produces *no metric* — only the scale $2GM/c^2$. Shuler produces *three actual members* of the metric family (points on the $\lambda$ continuum). One fixes a length; the other exhibits geometry.
- **2.** Visser's flat-slice heuristic secretly imposes the exact Newtonian infall profile at every radius, which is the PG-kinematics selector, and that condition is uniquely $\lambda=-1$. The "unexplained agreement" is the selecting ingredient hiding in the method.
- **3.** They do not pick a member of the family from the same shelf; they change the underlying rules — Casadio builds a different effective metric from a nonlinear model, Deser/Duff impose full dynamical self-consistency on the field equations. Selection within the family presumes the family; these operate above it.
- **4.** That a selecting ingredient is present but unstated — a smuggled assumption. Find it: it will be a kinematic demand, a measurement, or an extra field-law condition. This is the [`EPI3`](epi3-build-vs-select.md) audit.

</details>

## What the paper claims here

This tutorial grounds the paper's §7.1 table and its surrounding discussion. Faithful caveats: the paper is explicit that Deser (1970) and Duff (1973) "do not study selection within the $\lambda$-family," and that Casadio et al. "construct an effective metric from a nonlinear model, not the static local-energy assignment of Sec. 4." The paper does **not** claim any of these routes is *wrong*; it claims each uses non-identical assumptions, and it locates the difference. It also does not adjudicate the physical validity of the non-Schwarzschild members — that remains bracketed. The Rindler counterexamples and Gruber et al. no-go are cited as the negative results this paper complements constructively.

---
**Path navigation:** ← [HIST2 — the factor of two](../part7-michell-pg/hist2-factor-of-two.md) · [next: EPI1 — representation vs. fact](epi1-representation-vs-fact.md) →
**See also:** [`EPI3`](epi3-build-vs-select.md), [`HIST1`](../part7-michell-pg/hist1-michell-laplace.md), [`CORE5`](../part3-building-the-family/core5-distinguished-members.md), [`OUT1`](out1-self-coupling-bootstrap.md), [`MAP`](../part0-orientation/map.md), [bibliography](../reference/bibliography.md)
