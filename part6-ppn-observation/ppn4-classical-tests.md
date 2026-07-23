# The Classical Tests, Sorted by Which Parameter They See

> **Tutorial `PPN4`** · Part 6 · **Goal:** Sort redshift, light bending, Shapiro delay, and perihelion precession by whether they see $\gamma$, $\beta$, or neither — and explain why the family survived unchallenged until Mercury · **Prereqs:** [PPN3](./ppn3-gamma-beta.md), [F5](../part1-foundations/f5-geodesics.md), [S3](../part2-schwarzschild/s3-properties.md)

**Where this sits in the arc.** `PPN3` established that every member of the family shares $\gamma=1$ and differs only through $\beta=\lambda+2$. This tutorial works out which classical solar-system tests can, in principle, detect that difference. The answer sorts the tests into two classes: those blind to $\lambda$ (because they only ever see $\gamma$, or only the universal Newtonian term) and the one test that is not — perihelion precession, which is why the whole family remained observationally viable until precise perihelion data existed.

## Redshift: sees only the universal Newtonian term

Gravitational redshift compares clock rates at different radii, and depends only on $-g_{tt}=A$ itself, evaluated to leading order. From `WEAK1`,
$$A_\lambda(r) = 1 - x + O(x^2), \qquad x = r_s/r,$$
and the leading coefficient of $x$ is $-1$ for *every* $\lambda$ — this was exactly the content of imposing the Newtonian limit (I1) in `CORE0`, which fixes the mass scale and the leading behavior but says nothing about the nonlinear terms that distinguish members. So a redshift measurement, read to leading order, cannot tell members of the family apart, nor can it tell any of them apart from GR. (A sufficiently precise redshift measurement sensitive to the $O(x^2)$ term *would* see $a_2$, hence $\lambda$ — but ordinary gravitational redshift experiments, e.g. Pound–Rebka-type or GPS clock comparisons, operate at leading order and do not resolve this.)

## Light bending and Shapiro delay: sees only $\gamma$

Both light bending and the Shapiro radar-echo delay are properties of *null* geodesics — light rays — passing near the mass. A photon's trajectory is fixed by the full metric, but the standard result (worked out in any PPN-formalism reference, e.g. Will) is that to the order these two effects are conventionally measured, the deflection angle and the excess light-travel time both come out proportional to $(1+\gamma)$:
$$\delta\phi = (1+\gamma)\frac{2GM}{c^2 b}, \qquad \Delta t_{\rm Shapiro} \propto (1+\gamma),$$
with $b$ the impact parameter. Structurally, this is because a photon's null condition ($ds^2=0$) mixes the time part and the space part of the metric linearly at leading order — $-g_{tt}c^2dt^2$ contributes one factor of $U$, and $g_{ij}dx^idx^j$ contributes a factor of $\gamma U$, and together they give the combination $(1+\gamma)U$ as the leading relativistic correction to the light path. The $\beta U^2$ term in $g_{tt}$ is one full post-Newtonian order higher than this leading photon-deflection effect; it would only show up in a *second*-order (2PN) correction to light bending, far below the precision of the classical measurements. So both tests depend only on $\gamma$.

Since `PPN3` established $\gamma=1$ for *every* member of the family, light bending and Shapiro delay come out identical, to the precision these tests operate at, for Schwarzschild, the exponential member, the reciprocal member, and every other point on the $\lambda$-line. These two of the three "classical tests of GR" are entirely uninformative about which member of the family is realized in nature.

## Perihelion precession: sees $\gamma$ *and* $\beta$

A bound elliptical orbit, unlike a photon's one-pass trajectory, accumulates the relativistic correction over many orbits, and its shape (not just its light-crossing time) responds to the *full* 1PN structure of the metric — both the spatial curvature term ($\gamma U$, entering the effective potential through the redefinition of angular momentum in curved space) and the nonlinear time term ($\beta U^2$, entering the radial equation of motion at the same post-Newtonian order the orbit itself is being computed to). Both effects arrive at the *same* order in $U$ for a bound massive orbit, unlike the photon case where the $\beta U^2$ term is parametrically suppressed. This is the standard PPN result (again, Will's textbook derivation, not re-derived here since the source paper itself takes it as known): the leading anomalous perihelion precession per orbit, relative to the GR prediction, is rescaled by the factor
$$\frac{2+2\gamma-\beta}{3}.$$
Because this factor depends on *both* $\gamma$ and $\beta$ — and because $\gamma=1$ is common to every member — the whole discriminating power collapses onto $\beta$ alone, and hence (via $\beta=\lambda+2$) onto $\lambda$. `PPN5` works the factor out explicitly and reproduces the numbers.

## Why the family survived until Mercury

Two of the three classical tests of GR (light bending, radar delay) are, by the argument above, *automatically* satisfied by every member of the $\lambda$-family, because they depend only on $\gamma$, and $\gamma=1$ was never in question — it follows from the reciprocal condition (I3) alone, adopted at the very start of the construction (`CORE0`), regardless of the closure choice $\lambda$. Redshift, similarly, is fixed at leading order by the Newtonian limit (I1), again independent of $\lambda$. So an experimenter confirming Einstein's light-bending prediction, or Shapiro's radar-delay prediction, learns *nothing* that distinguishes Schwarzschild from any other member of this family — every member predicts the identical answer at the precision available. Only perihelion precession, which is sensitive to the second post-Newtonian coefficient $\beta$, has the power to separate them. This is precisely why an entire one-parameter family of metrics — infinitely many candidate exteriors, all sharing the same Newtonian limit and the same leading relativistic corrections — remained, in principle, observationally indistinguishable from Schwarzschild right up until a precession measurement sharp enough to read off $\beta$ became available. Mercury's perihelion is not just "one more test GR happens to pass"; it is *the* test in this family that has any power to fail.

## Simpler on-ramp

Think of the three classical tests as asking successively harder questions of the metric. Redshift asks "how much do clocks slow near the mass?" — a question with the same answer for every member, because all family members were built to agree on that by construction (that's the whole point of the Newtonian-limit assumption). Light bending and radar delay ask a slightly sharper question — "does *space itself* also curve, in step with the clock slowdown?" — but every member of this particular family answers that question identically too ($\gamma=1$ for all of them), because the reciprocal condition that fixes $\gamma$ was baked in from the start, independently of the closure choice that distinguishes members. Only perihelion precession asks the truly hard question — "does gravity's own energy feed back on itself at exactly the strength GR predicts, or a bit more, or a bit less?" — and that is the one question on which the family's members actually disagree.

## Check your understanding

- Why is a redshift experiment, in principle, capable of detecting $\lambda$-dependence at *some* order, even though ordinary redshift tests don't?
- Why do light bending and Shapiro delay depend on $\gamma$ but not (at the order they're measured) on $\beta$?
- Why does a bound orbit "see" $\beta$ when a passing photon doesn't?
- What exactly does "the family survived until Mercury" mean — survived *what*, precisely?

**Answers**
- Redshift is governed by $A(r)=1-x+a_2x^2+O(x^3)$; the $a_2x^2$ term does carry $\lambda$-dependence, so a redshift measurement precise enough to resolve the second-order term would see it. Ordinary redshift tests operate at first order in $x$ and never reach that term.
- Photon trajectories accumulate their leading relativistic correction over a single pass, at an order in $U$ where only the linear terms in the metric ($\gamma U$ in space, the leading $U$ term in time) contribute; the nonlinear $\beta U^2$ term is parametrically one order higher and doesn't affect the leading deflection/delay formulas.
- A bound orbit's shape is computed to the same post-Newtonian order at which $\beta U^2$ contributes, because the orbit integrates the metric's effect over a full revolution rather than a single pass, bringing the nonlinear term into play at leading order for the precession itself.
- It means: every prediction these tests could make (redshift, light bending, Shapiro delay) came out identical for every $\lambda$ in the family, so passing those tests confirmed the *family as a whole*, not Schwarzschild specifically — the family wasn't ruled out by any test until one (perihelion precession) existed that could actually discriminate among its members.

## What the paper claims here

Grounded in Sec. 5.3: "Redshift: leading $A_\lambda=1-r_s/r+O(r^2)$ same for all; doesn't distinguish (higher-order could). Light deflection + Shapiro delay: depend on $\gamma$; $\gamma=1$ throughout so same as GR at leading PN. Perihelion precession: depends on $\gamma$ **and** $\beta$; leading anomalous precession relative to GR multiplied by $\frac{2+2\gamma-\beta}{3}$." The paper states the $(2+2\gamma-\beta)/3$ factor and the qualitative sorting of tests as known PPN results; it does not re-derive the deflection/delay/precession formulas from the geodesic equation from scratch, and neither does this tutorial — the structural *why* given above (order-counting in $U$) is offered as explanation, consistent with, but not more than, what the paper asserts.

---
**Path navigation:** ← [prev in default path](./ppn3-gamma-beta.md) · [next](./ppn5-perihelion-precession.md) →
**See also:** [F5](../part1-foundations/f5-geodesics.md), [S3](../part2-schwarzschild/s3-properties.md), [HIST2](../part7-michell-pg/hist2-factor-of-two.md)
