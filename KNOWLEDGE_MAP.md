# Knowledge Map — What It Takes to Understand This Paper Like Its Author

Goal of this document: answer *"I don't know what I need to know."* It reverse-
engineers the competence the author demonstrably used, so the tutorial book can be
built to reconstruct it. This map is the real spec; `PLAN.md` is its table of contents.

**Target level:** *Critique* — re-derive every result unaided, know why each
assumption is load-bearing, and judge the paper's own caveats. (See the four levels
in the project notes: Follow / Reproduce / Critique / Extend.)

---

## A. The genuine cruxes (where the real difficulty and insight live)

Most of the paper is mechanical once you have the machinery. These five are the
conceptual center — if you master only these, you understand the *point*; everything
else is support.

1. **Representation freedom is the whole game.** A vacuum Gauss law + $AB=1$ +
   Newtonian limit does **not** close the system: you're still free to choose *which*
   function $V(A)$ obeys the flux law, and different choices give different nonlinear
   metrics that agree at Newtonian order. (I4) is the closure that tames this. The
   insight most readers miss: "flux law ⇒ done" is false. → tutorials `CORE1`, `CORE2`, `EPI1`.

2. **Circularity: an identity is not a measurement.** You cannot fix $\lambda$ by
   declaring "field energy gravitates universally," because the field density was
   *defined* to make the equation take that form. Substitution returns the equation
   unchanged, for every $\lambda$. This is a logic insight wearing a physics costume.
   → `ACC1`, `EPI2`.

3. **Energy has no address.** The total assembly energy $-U$ is invariant; its split
   into matter and field is a *convention*. The $[-\tfrac14,\tfrac14]$ bound is only
   as strong as the assumption $0\le f\le1$, which is a modeling choice, not a
   theorem. Author-level maturity = holding "the total is real, the split is gauge"
   in one hand. Requires knowing that gravitational energy localization is genuinely
   ambiguous (pseudotensors, quasi-local energy). → `ACC2`–`ACC6`, `ENE1`.

4. **The bridge identity $\beta = \lambda + 2$.** The abstract closure coefficient
   from §2 *equals* a measurable PPN parameter. This is what turns a math family into
   physics. Requires real PPN fluency + a second-order coordinate transformation.
   → `PPN2`, `PPN3`.

5. **The global infall condition selects Schwarzschild.** $\frac12 v^2 = GM/r$ holding
   at *every* radius (not just asymptotically) is strictly stronger than the Newtonian
   limit and picks $\lambda=-1$ alone — which is why Michell's number is a *consequence*
   of the right metric, not a derivation of it. → `PG3`, `HIST1`.

Everything below is the toolkit these five require.

---

## B. The competence inventory, by domain

Each entry: **what the author uses it for in this paper**, then the sub-skills. A `★`
marks a genuine crux-support skill; `∘` marks standard machinery you must be fluent in
but that isn't where the insight lives.

### B1. Differential-geometry / GR machinery
- ∘ Metric, line element, signature, index & summation notation — *read $ds^2$ fluently.*
- ∘ Proper time / proper length from the metric; $-g_{tt}$ as a clock rate.
- ★ **Static + spherically symmetric ⇒ the $-A\,c^2dt^2 + B\,dr^2 + r^2d\Omega^2$ form**,
  and *why* symmetry forces it (Killing vectors, the areal-radius gauge choice).
- ★ **Areal vs. isotropic vs. Painlevé–Gullstrand coordinates** — switch between them
  at will; know what each makes manifest and what it hides.
- ★ **Second-order coordinate transformations** (the $r=\rho(1+k_1w+k_2w^2)$ matching).
  A real, transferable skill; the $\beta$ result depends on it.
- ∘ Geodesics, conserved quantities, effective potentials, the orbit equation (feeds
  perihelion precession).
- ∘ Curvature: Riemann/Ricci/**Kretschmann** — enough to say "invariant diverges = real
  singularity," to separate coordinate from curvature singularities.
- ★ **Birkhoff's theorem** and *why it does not contradict a family* — the single most
  important backdrop fact (see §C).

### B2. The paper's own closure machinery (§2)
- ∘ The **radial flux / Gauss operator** $\Delta=\frac1{r^2}\frac{d}{dr}(r^2\frac{d}{dr})$;
  field strength $\propto 1/r^2$; flux through a sphere. **Not** the Laplace–Beltrami
  operator of the curved slice — a distinction the author is explicit about.
- ★ The **chain-rule identity** $\Delta V = F'\Delta s + F''(s')^2$ and the recognition
  that $-F''/F'$ is the effective nonlinear coefficient.
- ∘ Solving the constant-coefficient linear ODE $F''=-\lambda F'$; the essential
  variable $A^{-\lambda}$; the $\lambda\to0$ exponential as the *continuous* limit.
- ∘ Asymptotic matching / boundary conditions to fix integration constants.
- ★ **Completeness/uniqueness reasoning scoped precisely** — "unique *within this
  family*," "complete *relative to* (I1)–(I4)." Knowing exactly what a theorem claims.

### B3. Weak-field & post-Newtonian expertise
- ∘ The **Newtonian limit**: $-g_{tt}\approx 1+2\Phi/c^2$, $\Phi=-GM/r$, the scale $r_s$.
- ∘ **Post-Newtonian bookkeeping**: expanding in $x=r_s/r$, tracking orders, knowing
  where members first diverge ($O(x^2)$).
- ★ **The PPN formalism**: what $\gamma$ (space curvature per unit potential) and
  $\beta$ (nonlinearity of the time–time part) *mean*; the standard PPN metric;
  GR's $\gamma=\beta=1$.
- ★ **The observational tests and which parameter each sees**: redshift (blind),
  light bending + Shapiro delay ($\gamma$, blind), perihelion precession
  ($\gamma$ **and** $\beta$). The precession factor $\frac{2+2\gamma-\beta}{3}$.
- ★ **Reading real constraints critically**: the LLR+Cassini value and INPOP20a bound,
  *and their provenance* — the assumed $\eta_N=4\beta-\gamma-3$ relation, "acceptance
  bound" vs. "confidence interval," order-of-magnitude honesty. Knowing the numbers
  *and their fine print* is subject-matter fluency, not lookup.

### B4. Energy in gravity (the hardest conceptual domain)
- ∘ **Newtonian self-energy**: assembly work, the shell theorem, quasi-static processes.
- ★ **The two energy densities** $-\frac{|\nabla\Phi|^2}{8\pi G}$ vs. $\frac12\rho\Phi$
  and why they're interchangeable (integration by parts + field equation) — the
  localization ambiguity in miniature.
- ★ **Gravitational energy localization is genuinely ambiguous**: pseudotensors,
  quasi-local energy (Komar / ADM / Bondi). You don't need to compute these, but you
  must *know they exist and why the split has no unique answer.*
- ★ **The invariant/convention split discipline**: total $-U$ is operational; the
  matter–field division is not; a "bound" on $\lambda$ inherits the arbitrariness of
  the division.
- ∘ **The Nordtvedt effect** and its tests (lunar laser ranging) — why "does binding
  energy gravitate normally?" is a real, measured question, not philosophy.
- ★ **The self-consistency lemma** (crux 2) — recognizing circular definitions.

### B5. Causal structure & Painlevé–Gullstrand
- ★ **The PG transformation**, flat spatial slices, the river velocity $v=c\sqrt{1-A}$
  (a coordinate shift, not a material flow).
- ★ **Where the curvature went**: it's in the mixed $2v\,dr\,dT$ term; flat slices
  ≠ flat spacetime. A direct echo of crux 1 (representation choice).
- ∘ **Radial null geodesics**, $dr/dT=-v\pm c$, the **horizon as $v=c$** (outgoing
  light frozen). The cleanest operational definition of a horizon.

### B6. History & literature (scholarship)
- The lineage: Michell (1784), Laplace; Lenz/Sommerfeld, Schiff, Tangherlini,
  Sacks–Ball; **Rindler's counterexamples**; **Gruber et al.'s systematic no-go**;
  Visser (2005), Czerniawski (2006), Kassner (2015/2017/2019), Shuler (2018);
  Casadio et al.; **Deser (1970), Duff (1973)** (the self-coupling bootstrap); Will
  (PPN). You must know *what each did and how it relates to the family* — this is the
  §7.1 table, and reproducing it from understanding (not copying) is a real test.

### B7. Meta-skills (the author's actual edge)
- ★ **Build vs. select**: separating the construction of a solution set from the
  extra condition that picks a member; naming the smuggled assumption in any "simple
  derivation." This is the paper's method and its main contribution.
- ★ **Characterizing solution sets, not exhibiting solutions.** The mindset shift from
  "here's a derivation of Schwarzschild" to "here's everything these assumptions allow."
- ★ **Scope discipline and intellectual honesty**: never overclaiming ("unique within
  this family"; "zero, not necessarily horizon"; "order of magnitude").
- ∘ **Dimensional analysis and coefficient tracking** (the factor-of-4, the factor-of-2)
  as a routine sanity net.

---

## C. The negative space — questions the paper doesn't ask but the author can answer

This is the real test of *Critique*-level understanding. If you can answer these, you
understand it as well as the author. They should each become a tutorial aside or an
"Extend" exercise.

1. **If these aren't vacuum-Einstein solutions, what are they?** (I2) is explicitly
   *not* the Einstein vacuum equation. So for $\lambda\ne-1$, feeding $A_\lambda$ into
   real GR gives a **nonzero Einstein tensor** in the "vacuum" exterior — i.e. an
   effective stress–energy. The members are solutions of a *postulated flux law*, not
   of $G_{\mu\nu}=0$. Understanding this is central to the paper's logical status.
2. **Why doesn't Birkhoff's theorem forbid a family?** Birkhoff: static + spherical +
   *vacuum Einstein* ⇒ Schwarzschild, uniquely. The family evades this precisely by
   **replacing the field equations with a weaker postulate**. Knowing exactly which
   hypothesis of Birkhoff is dropped is the sharpest way to locate what the paper does.
3. **Why areal coordinates for the flux law, and not isotropic?** The flux law is
   **coordinate-dependent** — that's why the paper calls it a postulate, not a covariant
   equation. A different coordinate choice for (I2) would give a different family.
4. **What if you drop $AB=1$ (I3)?** Two free functions again; the class explodes.
   Knowing what each assumption is *holding down* is load-bearing-analysis.
5. **Are the $\lambda\ne-1$ spacetimes physically sensible?** Geodesic completeness,
   energy conditions on the effective stress–energy, the nature of the $r_0$ surfaces —
   the paper deliberately brackets this ("does not classify... causal character").
6. **How does this relate to Rindler's counterexamples and Gruber et al.'s no-go?**
   Those said "the usual ingredients don't determine the metric"; this paper says
   *exactly what they determine instead.* Same fact, constructive form.

---

## D. Honest difficulty ranking (where to expect to struggle)

- **Hardest (conceptual, not computational):** energy localization & the convention
  bound (B4, crux 3); the circularity lemma (crux 2); the negative-space facts C1–C2
  (why these aren't GR solutions / Birkhoff). These are where smart readers go wrong.
- **Medium (real skill, learnable):** PPN formalism and the $\beta=\lambda+2$
  transformation (B3, crux 4); the closure ODE and completeness reasoning (B2).
- **Mechanical (fluency, not insight):** the weak-field expansions, the PG algebra,
  the flux-operator integration. Important, but not where understanding is won or lost.

The book should spend its *depth budget* on the Hardest tier and move briskly through
the Mechanical tier.

---

## E. Self-assessment — you understand it as well as the author when you can:

1. Derive $A_\lambda=(1+\lambda r_s/r)^{-1/\lambda}$ from the four assumptions with the
   paper closed, and state precisely what "complete" and "unique" mean here.
2. Explain, unprompted, why (I1)–(I3) don't close the system and what (I4) adds.
3. Reconstruct the two-shell calculation *and* articulate why its bound is conditional
   on a convention — without conflating that with "GR violates energy conservation."
4. Derive $\beta=\lambda+2$ and explain why $\gamma=1$ blinds light-bending to $\lambda$.
5. Explain why Michell got the right number and why that isn't a derivation.
6. Answer every question in §C above.
7. Reproduce the §7.1 literature table from understanding, classifying each route as
   *build* or *select* and naming what it adds.
8. State what the paper deliberately does **not** establish, and why that restraint is
   correct.

---

*Companion to `PLAN.md`. Reshaping note: this map surfaces gaps to add to the plan —
an explicit **Birkhoff's theorem** tutorial, an **"are these GR solutions?"**
tutorial (the effective stress–energy of off-Schwarzschild members), and deeper
**quasi-local energy** coverage than "further reading." These move from nice-to-have
to load-bearing once the target is author-level understanding.*
