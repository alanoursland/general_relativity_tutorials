# HIST2 — The factor of two in light bending

> **Tutorial `HIST2`** · Part VII · **Goal:** Show that the time coefficient $A=1-r_s/r$ alone, paired with a naively flat spatial metric, predicts only half the correct light deflection — and pin down exactly what the missing half is made of. · **Prereqs:** [PG1](./pg1-painleve-gullstrand.md), [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md), [PPN4](../part6-ppn-observation/ppn4-classical-tests.md)

**Where this sits in the arc.** This closes Part VII with the same moral as HIST1, aimed at a second historical episode: getting the time-time metric coefficient right (even once $\lambda$ has been correctly identified) is necessary but not sufficient for correct relativistic predictions. You need the *whole* metric — the spatial curvature, or equivalently, in PG form, the mixed term — and dropping either half systematically costs you a factor of two.

## The historical episode

Before completing general relativity, Einstein (1911) used only the equivalence principle — gravitational time dilation, with no statement about spatial curvature — to predict the deflection of starlight grazing the Sun. That calculation gives
$$\delta_{1911} = \frac{2GM}{c^2b},$$
where $b$ is the impact parameter. The completed 1915 theory, using the full Schwarzschild metric (time dilation *and* spatial curvature together), gives exactly double:
$$\delta_{1915} = \frac{4GM}{c^2b}.$$
Eddington's 1919 eclipse expedition measured the *doubled* value, not the halved one — a real, historically pivotal confirmation of the completed theory over the equivalence-principle-only calculation that preceded it.

## In PPN language

[PPN3](../part6-ppn-observation/ppn3-gamma-beta.md) established that light deflection is controlled entirely by $\gamma$ (the PPN parameter for spatial curvature per unit potential), via the standard formula
$$\delta = \frac{2(1+\gamma)GM}{c^2b}.$$
Setting $\gamma=1$ (general relativity, and — per [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md) — *every* member of this book's $\lambda$-family, since $\gamma=1$ is a consequence of the reciprocal condition (I3) alone, independent of $\lambda$) reproduces $\delta_{1915}=4GM/(c^2b)$. Setting $\gamma=0$ reproduces exactly $\delta_{1911}=2GM/(c^2b)$ — the halved value.

## What $\gamma=0$ corresponds to, physically

$\gamma=0$ is exactly what you get if you take the correctly identified time coefficient, $A=1-r_s/r$, and pair it with a naively flat, Euclidean *static* spatial metric — i.e., you keep $A(r)$ but replace $B(r)=1/A(r)$ with $B=1$, discarding the spatial curvature that (I3) actually requires. This is precisely Einstein's 1911 reasoning: gravitational time dilation alone makes clocks run slow near the Sun, which is enough, by itself, to bend a light ray's path (much as light bends entering a medium whose refractive index varies with position) — but it says nothing about space itself being non-Euclidean, and misses that contribution entirely.

The standard decomposition of the deflection integral splits cleanly into two equal contributions for GR: half from the time-dilation term (the $A(r)$ piece) and half from the spatial-curvature term (the $B(r)=1+2\gamma\,GM/(c^2\rho)$ piece, in isotropic coordinates). Discarding the spatial term — setting $\gamma=0$ — leaves only the temporal half, exactly $\delta_{1911}$. Since $\gamma=1$ for *every* member of this book's family (a direct consequence of $AB=1$, established once in [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md) and never revisited by $\lambda$), *no* member of the family — not even a hypothetical one tuned to match some other observation — predicts the halved deflection; $\gamma=0$ is not a value any family member can take. The "half" answer is not a rival member of this family at all; it is what you get from an altogether different (and incomplete) construction that never imposes (I3) in the first place.

## Reconciling this with PG's flat slices

A careful reader of [PG2](./pg2-where-did-curvature-go.md) should pause here: PG coordinates *also* have flat spatial slices, $d\ell^2=dr^2+r^2d\Omega^2$ — so is the PG representation making the same mistake as the "$\gamma=0$" construction above, and only accidentally getting the right answer? No — and the distinction is exactly the point of [PG2](./pg2-where-did-curvature-go.md). The naive "$\gamma=0$" construction of this tutorial has flat space *and no mixed term*: it is a purely static ansatz, $ds^2=-Ac^2dt^2+dr^2+r^2d\Omega^2$, with the spatial curvature simply thrown away and nothing put in its place. PG coordinates have flat space *and* the mixed term $2v\,dr\,dT$, which — as [PG2](./pg2-where-did-curvature-go.md) showed — carries exactly the gravitational content that isotropic coordinates store in $\gamma$. The deflection computed from the full PG metric agrees with the full isotropic-coordinate result, because both include everything; the naive Euclidean-static metric agrees with neither, because it has discarded the spatial-curvature information without relocating it anywhere. Flat slices are innocuous once you keep the mixed term that goes with them; they are not innocuous if you simply delete the curvature and replace it with nothing.

## The recurring moral

The lesson of HIST1 and HIST2 is the same lesson stated twice, in two different observational currencies. HIST1 showed that correctly identifying the time coefficient's *value* ($\lambda=-1$) is not the same as having derived the full causal structure — Michell's escape-velocity argument never touches the metric at all. This tutorial shows the complementary failure mode: even after $A(r)$ is correctly identified, treating it as though it were the *whole* metric — informally, as popular explanations of light bending sometimes implicitly do, and as Einstein himself did in 1911 before he had the completed field equations — systematically undershoots observable predictions by a factor of exactly two. In both cases, the fix is the same: use the entire metric, in whatever representation, not just the piece that happens to be easiest to reach for first.

## Simpler on-ramp

Light bending near the Sun has two separate physical sources, and popular explanations often mention only one. The first: clocks run slow near mass, which (by an argument no more exotic than "light bends entering glass because its effective speed changes across the boundary") is enough on its own to bend a light ray's path — this is the part Einstein could get in 1911 from the equivalence principle alone, without a full theory of gravity. The second: space itself is subtly non-Euclidean near the Sun — there is slightly more room in the radial direction than a flat ruler would suggest — a purely geometric effect with no pre-1915 analogue at all, and one Einstein could only add once he had completed general relativity. Each source contributes exactly half the total bending; leaving either one out — whichever one — halves the answer.

## Check your understanding

- Which two years and predictions does this history involve, and how do their predicted deflection angles compare?
- Which value of $\gamma$ gives the halved deflection, and why is that value never realized by any member of the $\lambda$-family?
- Painlevé–Gullstrand slices are also flat, yet PG gives the full (correct) deflection, not the halved one — what is the precise difference between PG's flat slices and this tutorial's "naive Euclidean spatial metric"?
- What is the shared moral connecting this tutorial and HIST1?

**Answers**
- Einstein's 1911 prediction, $\delta_{1911}=2GM/(c^2b)$, using time dilation alone; the completed 1915 theory's $\delta_{1915}=4GM/(c^2b)$, using the full metric — exactly double, and the value Eddington's 1919 expedition confirmed.
- $\gamma=0$; every family member has $\gamma=1$ as a direct consequence of the reciprocal condition $AB=1$ (established in PPN3) regardless of $\lambda$, so $\gamma=0$ is not a value any family member — nor any adjustment of $\lambda$ — can produce.
- PG's flat slices come with the mixed term $2v\,dr\,dT$, which carries exactly the gravitational content that spatial curvature carries in isotropic coordinates; the naive Euclidean construction discards the spatial curvature and replaces it with nothing, keeping neither the curvature nor an equivalent substitute.
- Getting one piece of the metric right (the time coefficient's value, or its numerical scale) is not the same as having the whole metric; treating that one piece as though it were sufficient systematically loses real physical content — a wrong horizon interpretation in HIST1, a factor of two in observable deflection here.

## What the paper claims here

Grounded in Sec. 6.5: "pairing $A=1-r_s/r$ with a static Euclidean spatial metric gives $\gamma=0$ and HALF the leading GR light deflection. Flat PG slices avoid this because full metric has the mixed term $2v\,dr\,dT$. Michell's velocity relation is physically meaningful only after remaining metric structure is supplied." The historical Einstein 1911/1915 deflection values and the standard PPN formula $\delta=2(1+\gamma)GM/(c^2b)$ are the well-established textbook facts this section rests on; $\gamma=1$ for the whole family is carried over from [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md)'s Sec. 5.1.1 result and is not re-derived here.

---
**Path navigation:** ← [prev: HIST1](./hist1-michell-laplace.md) · [next: SYN1](../part8-synthesis/syn1-century-of-shortcuts.md) →
**See also:** [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md), [PPN4](../part6-ppn-observation/ppn4-classical-tests.md), [PG2](./pg2-where-did-curvature-go.md)
