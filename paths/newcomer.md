# Path: The full climb

For readers taking the whole book, start to finish, with nothing assumed beyond
calculus and freshman physics. This is the default reading order — every
tutorial's "prev / next" links follow it — so you can also just start at
[`INTRO`](../part0-orientation/intro.md) and follow the arrows; this page is the
same order laid out as one list, with a reason for every stop.

The climb has a shape: build the family (Part I–III), notice it splits by sign
(Part IV), watch the first candidate selector fail (Part V), watch a real one
succeed (Part VI), understand *why* the old shortcut looked right for the wrong
reason (Part VII), then step back and generalize the lesson (Part VIII).

## Part 0 — Orientation
1. [`INTRO` — How to read this book](../part0-orientation/intro.md) — conventions, notation, what "self-contained" and "prose-only" mean here.
2. [`MAP` — The big picture in one page](../part0-orientation/map.md) — the family and the three selectors, spoiler-y on purpose, so you always know where a detail fits.

## Part I — Foundations
3. [`F1` — What is a metric?](../part1-foundations/f1-metric.md) — the one object everything else is built from: $ds^2$ as a machine for proper time and length.
4. [`F2` — Vectors, one-forms, tensors, coordinates](../part1-foundations/f2-tensors.md) — just enough tensor algebra to tell a coordinate artifact from an invariant fact, a distinction the whole book turns on.
5. [`F3` — Special relativity as flat spacetime](../part1-foundations/f3-special-relativity.md) — the flat baseline; why $-g_{tt}$ is a clock rate.
6. [`F4` — Flat space in curvilinear coordinates](../part1-foundations/f4-curvilinear-coordinates.md) — spherical coordinates and areal radius, the specific coordinate choice the whole construction depends on.
7. [`F5` — Geodesics: how things move](../part1-foundations/f5-geodesics.md) — the equation of motion you'll need for perihelion precession in Part VI.
8. [`F6` — The Newtonian limit](../part1-foundations/f6-newtonian-limit.md) — how $-g_{tt}\approx1+2\Phi/c^2$ emerges and where the mass scale $r_s$ comes from.
9. [`SYM1` — Static, spherically symmetric metrics](../part1-foundations/sym1-static-spherical.md) — why symmetry forces the $-A\,c^2dt^2+B\,dr^2+r^2d\Omega^2$ form the entire family lives in.
10. [`F7` — Curvature, briefly](../part1-foundations/f7-curvature.md) — enough Riemann/Kretschmann to say "an invariant diverges" precisely, needed before you can call anything a real singularity.
11. [`GAUSS1` — Gauss's law, flux, and the radial Laplacian](../part1-foundations/gauss1-flux-laplacian.md) — the flat-space flux operator that (I2) will demand vanish — and the explicit warning that it is *not* the curved-space Laplace–Beltrami operator.
12. [`ENE1` — Newtonian potential energy & self-energy](../part1-foundations/ene1-self-energy.md) — the localization ambiguity, in miniature, before any GR — this is what makes Part V's failure unsurprising in hindsight.

## Part II — The standard Schwarzschild solution
13. [`S1` — The vacuum Einstein equations, lightweight](../part2-schwarzschild/s1-vacuum-einstein.md) — just enough of "real GR" to know what the shortcut in Part III is a shortcut *from*.
14. [`S2` — Deriving Schwarzschild the standard way](../part2-schwarzschild/s2-deriving-schwarzschild.md) — the honest derivation, so you can contrast it against the paper's four-assumption route later.
15. [`BIRK` — Birkhoff's theorem](../part2-schwarzschild/birkhoff.md) — why full vacuum GR gives a *unique* answer, which is exactly the uniqueness the family construction will not have.
16. [`S3` — Properties of Schwarzschild](../part2-schwarzschild/s3-properties.md) — the horizon, redshift, orbits, and classic tests as GR actually predicts them — your answer key.
17. [`S4` — Coordinate vs. curvature singularities](../part2-schwarzschild/s4-singularities.md) — why $r_s$ is a coordinate artifact but $r=0$ is real, the diagnostic you'll reuse on the whole family.

## Part III — Building the family
18. [`CORE0` — The four assumptions in common language](../part3-building-the-family/core0-four-assumptions.md) — the specification whose solution set the rest of Part III characterizes.
19. [`CORE1` — The flux law and the freedom in the potential variable](../part3-building-the-family/core1-flux-freedom.md) — the crux: an exact flux law doesn't say *which* function of $A$ obeys it, so the system isn't closed yet.
20. [`CORE2` — The logarithmic variable and the closure ODE](../part3-building-the-family/core2-log-variable-closure.md) — the key reveal: $\lambda$ is a property of the closure you pick, not a fact about the geometry.
21. [`CORE3` — Solving the closure: the essential variable $A^{-\lambda}$](../part3-building-the-family/core3-essential-variable.md) — the ODE solved, giving the variable in which the flux law is exact.
22. [`CORE4` — Integration and the classification theorem](../part3-building-the-family/core4-classification-theorem.md) — boundary conditions close the family: $A_\lambda=(1+\lambda r_s/r)^{-1/\lambda}$, complete but not unique.
23. [`WEAK1` — Weak-field degeneracy](../part3-building-the-family/weak1-weak-field-degeneracy.md) — members agree through $O(x)$ and split at $O(x^2)$ — foreshadows why only precision tests can tell them apart.
24. [`CORE5` — Distinguished members & Shuler](../part3-building-the-family/core5-distinguished-members.md) — Schwarzschild, the exponential, and the reciprocal as three named points on one continuum.
25. [`CORE-CONTRAST` — Shortcut vs. real derivation](../part3-building-the-family/core-contrast.md) — side by side against `S2`: what four assumptions buy versus what full vacuum GR buys.

## Part IV — Structure of the family
26. [`ZERO1` — Finite-radius zeros and the sign of $\lambda$](../part4-family-structure/zero1-finite-radius-zeros.md) — $\lambda<0$ is exactly the condition for a positive-radius zero of $A_\lambda$.
27. [`ZERO2` — When is a zero a horizon?](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) — the book's central discipline: a vanishing $g_{tt}$ is necessary, never sufficient, for a horizon.

## Part V — Can energy accounting pick $\lambda$?
28. [`ACC0` — The question](../part5-energy-accounting/acc0-the-question.md) — does "gravitational energy gravitates universally" finish the job the static assumptions left open?
29. [`ACC1` — The circularity trap](../part5-energy-accounting/acc1-circularity.md) — no: reading the field density off the equation you're solving for $\lambda$ is circular, for every $\lambda$.
30. [`ACC2` — The invariant assembly energy](../part5-energy-accounting/acc2-invariant-assembly-energy.md) — the one thing that *is* convention-free: the two-shell winch work $-U$.
31. [`ACC3` — The gradient-local field cross term](../part5-energy-accounting/acc3-field-cross-term.md) — computing the field's share of that energy, which comes out proportional to $\lambda$.
32. [`ACC4` — Matter conventions and the bound](../part5-energy-accounting/acc4-matter-conventions-bound.md) — the honest operational bound: $\lambda\in[-\tfrac14,\tfrac14]$ — which excludes Schwarzschild.
33. [`ACC5` — The factor of four](../part5-energy-accounting/acc5-factor-of-four.md) — Schwarzschild's field-energy coefficient is $4\times$ the plain Newtonian one; what that does and doesn't mean.
34. [`ACC6` — Energy has no address](../part5-energy-accounting/acc6-energy-localization.md) — why the matter/field split is gauge-like, in Newtonian gravity and in GR alike.
35. [`GRSOL` — Are these GR solutions?](../part5-energy-accounting/grsol-are-these-gr-solutions.md) — no, except at $\lambda=-1$: the rest solve a postulated flux law, not $G_{\mu\nu}=0$.

## Part VI — Observation picks $\lambda$
36. [`PPN1` — The PPN formalism, gently](../part6-ppn-observation/ppn1-ppn-formalism.md) — $\gamma$ and $\beta$, the two numbers that summarize a metric's post-Newtonian content.
37. [`PPN2` — Areal vs. isotropic coordinates](../part6-ppn-observation/ppn2-areal-isotropic.md) — the coordinate transformation needed before you can compare $A_\lambda$ to the PPN metric at all.
38. [`PPN3` — $\gamma=1$, $\beta=\lambda+2$](../part6-ppn-observation/ppn3-gamma-beta.md) — the bridge identity: the closure coefficient from Part III *is* a measurable PPN parameter.
39. [`PPN4` — The classical tests, sorted by parameter](../part6-ppn-observation/ppn4-classical-tests.md) — why redshift and light bending are blind to $\lambda$ but perihelion precession isn't.
40. [`PPN5` — Perihelion precession & the numbers](../part6-ppn-observation/ppn5-perihelion-precession.md) — Mercury's 43″/century picks $\lambda=-1$ and falsifies Part V's accounting interval outright.
41. [`PPN6` — From $\beta$ to $\lambda$: reading constraints critically](../part6-ppn-observation/ppn6-reading-constraints.md) — what the real bounds on $\beta$ do and don't assume — reading a headline number honestly.
42. [`PPN7` — $\beta<2$ and the horizon](../part6-ppn-observation/ppn7-beta-and-horizon.md) — the same measurement that selects Schwarzschild also implies the finite-radius zero from Part IV exists.

## Part VII — Michell, Painlevé–Gullstrand, and the coincidence
43. [`PG1` — Painlevé–Gullstrand coordinates & the river model](../part7-michell-pg/pg1-painleve-gullstrand.md) — a new coordinate slicing that makes space flat and puts all the gravity in one mixed term.
44. [`PG2` — Where did the curvature go?](../part7-michell-pg/pg2-where-did-curvature-go.md) — a direct echo of `CORE2`: same invariant spacetime, curvature traded for the $2v\,dr\,dT$ term by a representation choice.
45. [`PG3` — The unique Newtonian infall profile](../part7-michell-pg/pg3-newtonian-infall.md) — the genuine crux: $\tfrac12v^2=GM/r$ holding at *every* radius picks out $\lambda=-1$ alone.
46. [`PG4` — Horizons as light-cone tipping](../part7-michell-pg/pg4-horizons-light-cones.md) — the cleanest operational horizon definition: outgoing light frozen at $v=c$.
47. [`HIST1` — Michell & Laplace: right number, wrong reason](../part7-michell-pg/hist1-michell-laplace.md) — the 1784 coincidence explained, not vindicated — the logic runs selector-first, Michell-second.
48. [`HIST2` — The factor of two in light bending](../part7-michell-pg/hist2-factor-of-two.md) — why the time part of the metric alone gives only half of Einstein's deflection.

## Part VIII — Synthesis & epistemology
49. [`SYN1` — A century of shortcuts, mapped](../part8-synthesis/syn1-century-of-shortcuts.md) — every historical "simple derivation" sorted into *build* or *select*, and what each one adds.
50. [`EPI1` — Representation vs. fact](../part8-synthesis/epi1-representation-vs-fact.md) — the book's throughline named directly: $\lambda$ as a closure/gauge choice, not a geometric fact.
51. [`EPI2` — Identities are not measurements](../part8-synthesis/epi2-identities-not-measurements.md) — generalizing `ACC1`'s circularity lemma into a transferable reasoning habit.
52. [`EPI3` — Build vs. select](../part8-synthesis/epi3-build-vs-select.md) — how to audit any "simple derivation" you meet in the wild: separate the construction from the selecting condition.
53. [`OUT1` — Exit ramp: the self-coupling bootstrap](../part8-synthesis/out1-self-coupling-bootstrap.md) — beyond the paper: how full field self-consistency (Deser, Duff) forces Schwarzschild *dynamically*, for the reader still asking "but what really pins $\lambda=-1$?"

---
You've reached the end of the default reading order. From here: revisit
[`MAP`](../part0-orientation/map.md), or branch into one of the other
[paths](../README.md#choose-a-path) for a different angle on material you've
already met.
