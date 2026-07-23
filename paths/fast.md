# Path: Physicist's fast path

For readers who already have metrics, curvilinear coordinates, the Newtonian
limit, and Schwarzschild's standard derivation comfortably in hand. This path
skips Part I and Part II entirely and starts directly at the paper's actual
argument: build the family, split it by sign, watch the energy selector fail,
watch the PPN selector succeed, then see why Painlevé–Gullstrand explains the
old Michell coincidence.

If a step assumes foundational machinery you want refreshed, the relevant
Part I/II tutorial is one click away from each entry below.

## Build the family
1. [`CORE0` — The four assumptions in common language](../part3-building-the-family/core0-four-assumptions.md) — the specification: (I1) Newtonian limit, (I2) areal-coordinate flux law, (I3) $AB=1$, (I4) constant nonlinear coefficient.
2. [`CORE1` — The flux law and the freedom in the potential variable](../part3-building-the-family/core1-flux-freedom.md) — why (I1)–(I3) leave the potential variable unfixed — the system isn't closed yet.
3. [`CORE2` — The logarithmic variable and the closure ODE](../part3-building-the-family/core2-log-variable-closure.md) — $s=\ln A$, the chain-rule identity, and (I4) reducing the closure to $\Delta s=\lambda(s')^2$.
4. [`CORE3` — Solving the closure: the essential variable $A^{-\lambda}$](../part3-building-the-family/core3-essential-variable.md) — $F''=-\lambda F'$ solved.
5. [`CORE4` — Integration and the classification theorem](../part3-building-the-family/core4-classification-theorem.md) — $A_\lambda=(1+\lambda r_s/r)^{-1/\lambda}$, complete relative to (I1)–(I4), not unique.
6. [`WEAK1` — Weak-field degeneracy](../part3-building-the-family/weak1-weak-field-degeneracy.md) — members agree through $O(x)$, split at $O(x^2)$ by $(1+\lambda)/2$.
7. [`CORE5` — Distinguished members & Shuler](../part3-building-the-family/core5-distinguished-members.md) — $\lambda=-1,0,+1$ and Shuler's parameterization as points on the continuum.
8. [`CORE-CONTRAST` — Shortcut vs. real derivation](../part3-building-the-family/core-contrast.md) — what these four assumptions buy against what full vacuum GR buys.

## The sign switch
9. [`ZERO1` — Finite-radius zeros and the sign of $\lambda$](../part4-family-structure/zero1-finite-radius-zeros.md) — $A_\lambda=0$ at $r_0=-\lambda r_s$, positive iff $\lambda<0$.
10. [`ZERO2` — When is a zero a horizon?](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) — necessary, never sufficient, without the curvature-invariant check.

## The energy selector — and why it fails
11. [`ACC0` — The question](../part5-energy-accounting/acc0-the-question.md) — can "gravitational energy gravitates" pin down $\lambda$?
12. [`ACC1` — The circularity trap](../part5-energy-accounting/acc1-circularity.md) — reading the field density off the equation you're solving for $\lambda$ is circular, for every $\lambda$.
13. [`ACC2` — The invariant assembly energy](../part5-energy-accounting/acc2-invariant-assembly-energy.md) — the convention-free piece: two-shell winch work $E_{\rm int}=-U$.
14. [`ACC3` — The gradient-local field cross term](../part5-energy-accounting/acc3-field-cross-term.md) — $E_{\rm field,cross}=4\lambda U$.
15. [`ACC4` — Matter conventions and the bound](../part5-energy-accounting/acc4-matter-conventions-bound.md) — $\lambda=(2f-1)/4$, $-\tfrac14\le\lambda\le\tfrac14$ — excludes Schwarzschild.
16. [`ACC5` — The factor of four](../part5-energy-accounting/acc5-factor-of-four.md) — $u_{-1}=4u_N$; the total stays $-U$ regardless.
17. [`ACC6` — Energy has no address](../part5-energy-accounting/acc6-energy-localization.md) — why the matter/field split is gauge-like, with or without GR.

## The PPN selector — and why it works
18. [`PPN1` — The PPN formalism, gently](../part6-ppn-observation/ppn1-ppn-formalism.md) — $\gamma$ and $\beta$ defined; GR's $\gamma=\beta=1$.
19. [`PPN2` — Areal vs. isotropic coordinates](../part6-ppn-observation/ppn2-areal-isotropic.md) — the second-order transformation $r=\rho(1+k_1w+k_2w^2)$ needed to compare to standard PPN.
20. [`PPN3` — $\gamma=1$, $\beta=\lambda+2$](../part6-ppn-observation/ppn3-gamma-beta.md) — the bridge identity: closure coefficient = PPN nonlinearity.
21. [`PPN4` — The classical tests, sorted by parameter](../part6-ppn-observation/ppn4-classical-tests.md) — redshift and light bending blind to $\lambda$; perihelion precession sees it.
22. [`PPN5` — Perihelion precession & the numbers](../part6-ppn-observation/ppn5-perihelion-precession.md) — the $(2-\lambda)/3$ factor; Mercury selects $\lambda=-1$ and falsifies the accounting interval.
23. [`PPN6` — From $\beta$ to $\lambda$: reading constraints critically](../part6-ppn-observation/ppn6-reading-constraints.md) — $|\lambda+1|\lesssim10^{-4}$, with the provenance and assumptions of that bound made explicit.
24. [`PPN7` — $\beta<2$ and the horizon](../part6-ppn-observation/ppn7-beta-and-horizon.md) — the measurement that selects Schwarzschild also implies the zero from `ZERO1` exists.

## Painlevé–Gullstrand explains the coincidence
25. [`PG1` — Painlevé–Gullstrand coordinates & the river model](../part7-michell-pg/pg1-painleve-gullstrand.md) — flat spatial slices, $v=c\sqrt{1-A}$.
26. [`PG2` — Where did the curvature go?](../part7-michell-pg/pg2-where-did-curvature-go.md) — traded into the mixed $2v\,dr\,dT$ term; same invariant, different representation.
27. [`PG3` — The unique Newtonian infall profile](../part7-michell-pg/pg3-newtonian-infall.md) — $\tfrac12v^2=GM/r$ at every radius holds only for $\lambda=-1$.
28. [`PG4` — Horizons as light-cone tipping](../part7-michell-pg/pg4-horizons-light-cones.md) — $dr/dT=-v\pm c$; the horizon as $v=c$.

## Synthesis
29. [`SYN1` — A century of shortcuts, mapped](../part8-synthesis/syn1-century-of-shortcuts.md) — every historical route sorted into *build* or *select*, and what each adds.

---
That closes the fast path's core arc. If you want the epistemological
generalization of what you just saw (`EPI1`–`EPI3`), the historical framing
(`HIST1`–`HIST2`), or the field-theoretic exit ramp (`OUT1`), see the
[epistemology path](epistemology.md) and [history path](history.md), or continue
from `SYN1` along the [default order](newcomer.md).
