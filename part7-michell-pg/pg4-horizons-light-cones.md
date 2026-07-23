# PG4 — Horizons as light-cone tipping

> **Tutorial `PG4`** · Part VII · **Goal:** Derive the radial null-geodesic equation in PG coordinates, show the horizon is exactly the surface $v=c$, and confirm that only Schwarzschild puts this surface at $r_s$. · **Prereqs:** [PG1](./pg1-painleve-gullstrand.md), [PG3](./pg3-newtonian-infall.md), [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md), [F3](../part1-foundations/f3-special-relativity.md)

**Where this sits in the arc.** With $\lambda=-1$ selected three independent ways (energy accounting's exclusion, PPN's measurement, and PG3's exact infall condition), this tutorial cashes out the payoff in causal-structure terms: the PG river gives the single cleanest operational definition of a horizon in the whole book, phrased without any of the coordinate-singularity worries that dog the areal-coordinate zero of $A(r)$.

## Radial light rays in the river

Radial null rays satisfy $ds^2=0$ with $d\Omega=0$. From [PG1](./pg1-painleve-gullstrand.md)'s metric,
$$0 = -c^2dT^2 + \big(dr+v(r)\,dT\big)^2 \quad\Longrightarrow\quad dr+v\,dT = \pm c\,dT,$$
so
$$\boxed{\frac{dr}{dT} = -v(r) \pm c.}$$
Two branches: the **outgoing** branch $(dr/dT)_{\rm out} = c-v(r)$, and the **ingoing** branch $(dr/dT)_{\rm in} = -c-v(r)$, which is negative whenever $v\geq0$ — ingoing light always makes inward progress, at a coordinate rate that can exceed $c$ once $v>0$ simply because $T,r$ are not a locally orthonormal pair at fixed $r$; this is a coordinate speed, not a local one, and no local causality is violated. Nothing here is Newtonian — it comes directly from the mixed term $2v\,dr\,dT$ that [PG2](./pg2-where-did-curvature-go.md) identified as the carrier of curvature.

## The horizon is $v=c$

Everything of interest is in the outgoing branch. As long as $v(r)<c$, outgoing light still makes net outward progress: $dr/dT>0$. At the radius where $v(r)=c$ exactly,
$$\left(\frac{dr}{dT}\right)_{\rm out} = c - v = 0:$$
outgoing light is momentarily frozen in areal radius — the river's inward flow exactly cancels the photon's own outward progress relative to it. For $v(r)>c$, even the outgoing branch is negative: light aimed directly away from the center is nonetheless swept inward. No signal, however fast — and nothing is faster than light — can increase its areal radius from inside that surface. That is the sharpest possible operational statement of a horizon: not merely "things falling in keep falling in" (true everywhere gravity acts) but "outward light cannot make outward progress." The criterion is simply
$$\boxed{v(r) = c.}$$

This criterion has a real advantage over the areal-coordinate statement "$A(r)=0$": the PG metric components are smooth and finite right through $v=c$ (recall from [PG1](./pg1-painleve-gullstrand.md) that the whole point of the shift was to remove the $t$-coordinate's blow-up at $A\to0$), so nothing here signals a coordinate breakdown. The light-cone tipping is manifest and unambiguous without any of the "is this just a coordinate artifact?" bookkeeping that areal coordinates force (see [S4](../part2-schwarzschild/s4-singularities.md)).

## Connecting to the family

Since $v_\lambda(r)=c\sqrt{1-A_\lambda(r)}$,
$$v_\lambda(r)=c \iff A_\lambda(r)=0.$$
From [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md): $A_\lambda$ has a finite positive-radius zero, at $r_0=-\lambda r_s$, if and only if $\lambda<0$; for $\lambda\geq0$, $A_\lambda(r)>0$ for every finite $r>0$ ($A_0=e^{-r_s/r}$ and, for $\lambda>0$, the base $1+\lambda r_s/r$ both stay strictly positive). Consequently:

- For $\lambda\geq0$: $v_\lambda(r)<c$ strictly, for *every* finite $r>0$. As $r\to0^+$, $A_\lambda(r)\to0$ and so $v_\lambda(r)\to c$ only in the limit — the river never actually reaches light-speed at any finite radius, so no horizon forms by this test, however small $r$ becomes.
- For $\lambda<0$: $A_\lambda(r_0)=0$ at the finite radius $r_0=-\lambda r_s$, so $v_\lambda(r_0)=c$ exactly — a genuine light-freezing surface at finite radius. Consistent with the book's running restraint (echoed from [ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md)): this identifies the surface as a place where *this operational test* is met; it is not, by itself, a claim about geodesic completeness or global causal structure for $\lambda\neq-1$, which the paper deliberately leaves unclassified.

## Schwarzschild: the horizon lands exactly at $r_s$

For $\lambda=-1$: $v_{-1}(r)=c\sqrt{1-(1-r_s/r)}=c\sqrt{r_s/r}$. Setting $v_{-1}=c$:
$$\sqrt{\frac{r_s}{r}}=1 \;\Longrightarrow\; \frac{r_s}{r}=1 \;\Longrightarrow\; r=r_s.$$
The light-freezing surface sits exactly at $r=r_s=2GM/c^2$ — matching [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md)'s $r_0=-\lambda r_s=r_s$ at $\lambda=-1$, and matching the standard Schwarzschild horizon location established the ordinary way in [S3](../part2-schwarzschild/s3-properties.md). All three routes — the areal-coordinate zero, the PPN/accounting selection of $\lambda=-1$, and this light-cone criterion — agree.

## Simpler on-ramp

Picture swimming in a river that flows toward a waterfall, with the current's speed depending on how close to the falls you are, and suppose you can swim at your own top speed $c$ relative to the water. Far upstream the current is gentle; swimming away from the falls, you make headway. Closer in, the current picks up; at some point it exactly equals your top speed — swim your absolute hardest straight away from the falls, and you go exactly nowhere, treading water in place. Any closer than that, and even your best effort aimed away from the falls is not enough — you get swept backward no matter what. That crossover point, where the current first exactly matches your fastest possible speed, is the horizon. Light plays the swimmer's part, always moving at $c$ relative to the local water; the water's speed is $v(r)$; and $v=c$ is the point of no return.

## Check your understanding

- Why is $dr/dT=-v+c=0$ the right criterion for "light frozen," rather than looking at the ingoing branch (which is never zero for $v\geq0$)?
- Why is $v(r)=c$ a coordinate-regular criterion for a horizon, in contrast to $A(r)=0$ in areal coordinates?
- Why do family members with $\lambda\geq0$ never produce a horizon at any finite radius?
- At what radius does Schwarzschild's river reach $v=c$, and which two earlier results does that match?

**Answers**
- Because it is the outgoing branch that measures whether light can escape; the ingoing branch is already negative everywhere $v\geq0$ and carries no information about escape.
- Because the PG metric components stay smooth and finite through $v=c$ (that was the point of the PG1 shift), whereas $A(r)=0$ coincides with a blow-up of the static time coordinate in areal coordinates, requiring extra care to distinguish coordinate breakdown from physical singularity.
- Because $A_\lambda(r)>0$ for every finite $r>0$ whenever $\lambda\geq0$ (Sec. 3 / ZERO1), so $v_\lambda(r)<c$ strictly at every finite radius; $v_\lambda$ approaches $c$ only in the limit $r\to0$.
- Exactly at $r=r_s=2GM/c^2$, matching both ZERO1's zero location $r_0=-\lambda r_s=r_s$ at $\lambda=-1$ and the standard Schwarzschild horizon of S3.

## What the paper claims here

Grounded in Sec. 6.3: the paper derives $dr/dT=-v\pm c$ directly from $ds^2=0$, notes that at $v=c$ the outgoing rate vanishes and that "For $v>c$ even the outward branch $<0$," explicitly labeling this "NOT Newtonian — from mixed term." It confirms for Schwarzschild that $v^2=2GM/r$ together with $v=c$ gives $r=r_s$, and frames this (Sec. 6.4) as "Michell's equation identif[ying] the horizon radius when interpreted through the independently selected Schwarzschild geometry" — a forward pointer taken up fully in [HIST1](./hist1-michell-laplace.md). The paper's restraint about non-Schwarzschild zeros (Sec. 3: it does "NOT classify local regularity or global causal character" for $\lambda\neq-1$) is preserved here without extension.

---
**Path navigation:** ← [prev: PG3](./pg3-newtonian-infall.md) · [next: HIST1](./hist1-michell-laplace.md) →
**See also:** [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md), [ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md), [S4](../part2-schwarzschild/s4-singularities.md)
