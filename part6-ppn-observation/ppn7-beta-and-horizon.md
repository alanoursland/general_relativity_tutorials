# $\beta < 2$ and the Horizon

> **Tutorial `PPN7`** · Part 6 · **Goal:** Fuse the sign-of-$\lambda$ structure of the family with the PPN identity $\lambda=\beta-2$, and state precisely what the same measurement that selects Schwarzschild implies about the existence of a finite-radius zero · **Prereqs:** [PPN6](./ppn6-reading-constraints.md), [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md)

**Where this sits in the arc.** This tutorial closes Part VI by connecting back to Part IV. `ZERO1` showed that the sign of $\lambda$ alone decides whether $A_\lambda$ has a finite positive-radius zero. `PPN3`–`PPN6` showed that solar-system observation, run entirely at weak field far from any such zero, pins down $\lambda$ (via $\beta$) to high precision. Putting the two together: the very same weak-field measurement that selects Schwarzschild also tells us, via nothing but the sign of a number, whether a finite-radius zero exists at all — provided the family's closure structure is trusted to extend that far, a proviso this tutorial states explicitly.

## Recalling the zero, in $\lambda$

`ZERO1` showed that $A_\lambda(r) = (1+\lambda r_s/r)^{-1/\lambda}$ vanishes at a finite positive radius
$$r_0 = -\lambda r_s$$
if and only if $\lambda<0$; for $\lambda\geq0$ the function stays strictly positive for every finite $r>0$. So the existence of a zero is controlled purely by the *sign* of $\lambda$, and its location, when it exists, is controlled by the *magnitude* of $\lambda$ relative to $r_s$.

## Translating through $\beta=\lambda+2$

`PPN3` gave the exact identity $\lambda=\beta-2$. Substituting directly into the zero condition:
$$\lambda < 0 \iff \beta - 2 < 0 \iff \boxed{\beta < 2}.$$
And the zero's location, expressed in terms of $\beta$:
$$r_0 = -\lambda r_s = -(\beta-2)r_s = (2-\beta)r_s.$$
Check this against Schwarzschild directly: the measured value is $\beta\simeq1$ (from `PPN6`), so $r_0 = (2-1)r_s = r_s$ — exactly the Schwarzschild horizon, recovered purely from substituting the observed $\beta$ into a formula that came from the *sign-and-magnitude* structure of the family, with no separate appeal to the vacuum Einstein equations at all.

## The same measurement does both jobs

This is the fusion this tutorial is named for. A single number — $\beta$, measured entirely through weak-field solar-system data (light bending confirming $\gamma=1$, Mercury's perihelion pinning $\beta$ to $\lambda+2$, `PPN5`–`PPN6`'s honest order-of-magnitude bound $|\beta-1|\lesssim10^{-4}$) — simultaneously:

1. selects, to that same precision, which member of the family is realized ($\lambda\simeq-1$, Schwarzschild), *and*
2. determines, via the sign condition $\beta<2$, that a finite-radius zero of $A(r)$ exists at all, and (via $r_0=(2-\beta)r_s$) very nearly at $r_s$.

These look like two separate facts — one about which curve in a one-parameter family nature picked, one about the qualitative shape of that curve — but they come from exactly the same measured quantity. There is no second, independent observation needed to learn that a zero exists; it falls straight out of the same $\beta$ that Mercury's orbit supplies.

## What this does *not* establish — the extrapolation caveat

It is essential to be precise about the logical status of this conclusion, in the spirit the paper insists on throughout. The measurement of $\beta$ is a *weak-field* measurement: Mercury orbits at roughly $0.3$ AU, a distance enormously larger than $r_s$ for the Sun ($\sim3\,\mathrm{km}$), and every number in `PPN5`–`PPN6` comes from data taken at $r \gg r_s$, where $x=r_s/r \ll 1$. The formula $A_\lambda(r) = (1+\lambda r_s/r)^{-1/\lambda}$, with the *same constant* $\lambda$ all the way down to $r=r_0$, is a feature of the closure assumption (I4) — a constant nonlinear coefficient, imposed once, everywhere — not something the weak-field measurement independently verifies at strong field. Concluding "therefore a zero exists near $r_s$" is only valid *conditional on* trusting that (I1)–(I4) continue to hold, with the same $\lambda$, all the way into the strong-field regime — an extrapolation, not a direct strong-field observation.

Moreover, recall `ZERO1` and `ZERO2`'s own restraint: even granting the extrapolation, a zero of $A(r)$ is not automatically a *horizon* in the full geometric sense — that requires the additional invariant check (finite curvature invariants, correct causal structure) that `ZERO2` supplies, and which the source paper explicitly performs only for Schwarzschild ($\lambda=-1$), declining to classify the regularity of zeros for other negative $\lambda$. So the precise, careful statement is: *weak-field observation selects $\beta\simeq1$ (hence $\lambda\simeq-1$) to high precision, and the sign of that same $\beta$ (via $\beta<2$) is exactly the condition under which the family, extrapolated with a constant closure coefficient, predicts a finite-radius zero of $g_{tt}$ — and for the selected value $\lambda=-1$ specifically, that zero is independently known (by the ordinary vacuum-Schwarzschild analysis of Part II) to be a genuine, regular-at-the-horizon event horizon.* What the weak-field measurement alone does *not* do is directly observe the strong-field region or independently confirm the zero's causal character; that confirmation, for Schwarzschild, comes from elsewhere (`S3`, `S4`), not from the perihelion data itself.

## Simpler on-ramp

Picture a graph of $A(r)$ falling as $r$ decreases from far away, for some particular member of the family. Far from the mass — where Mercury actually orbits — the curve looks almost identical for every member; that's the whole reason the family survived so long (`PPN4`). What `PPN3`–`PPN6` show is that measuring the curve's *bend* in that far region (via $\beta$) is enough to know, with good confidence, which specific curve you're on. What this tutorial adds is a bonus: knowing which curve you're on, from the far-away bend alone, also tells you — by nothing more than checking whether a single number is less than 2 — whether that same curve, followed all the way in, would hit zero at some finite radius. It's a bit like inferring, from a chart of a mountain's slope near its base, both *which specific mountain* you're looking at and *whether that mountain has a summit at all* — a genuinely useful inference, but one that still assumes the mountain keeps the same overall shape all the way to the top, which you haven't actually walked up to check.

## Check your understanding

- Why does $\beta<2$ translate exactly to $\lambda<0$, with no extra assumption beyond the identity $\lambda=\beta-2$ itself?
- What, precisely, would have to fail for the "$\beta$ measurement implies a zero near $r_s$" conclusion to be wrong, even if $\beta$ were measured perfectly?
- Why does confirming a zero of $A(r)$ near $r_s$ still fall short of confirming a horizon, on this book's own standards?
- In what sense is this tutorial's central claim a genuinely new synthesis, rather than just restating `ZERO1` or `PPN3` separately?

**Answers**
- Because the translation is pure algebra: $\lambda=\beta-2$ is an identity (`PPN3`), so $\lambda<0$ and $\beta<2$ are, by substitution, literally the same statement about the same number — no additional physical assumption is needed for that step alone.
- The closure assumption (I4) — that $\lambda$ stays exactly constant, unchanged, all the way from the weak-field region where it's measured down to $r_0\sim r_s$ where the zero would occur — would have to hold; if the real nonlinear coefficient varies with field strength (which (I4) explicitly rules out by construction, but which a *real* theory of gravity need not respect), the extrapolation breaks and the zero's existence/location is no longer guaranteed by the weak-field $\beta$.
- Because a zero of $g_{tt}$ is a coordinate-dependent statement (`ZERO2`); calling it a horizon requires checking curvature invariants stay finite there and that the causal structure is the standard one, which the paper performs only for Schwarzschild via the independently known vacuum solution, not via the weak-field $\beta$ measurement itself.
- `ZERO1` is a purely structural fact about the family (sign of $\lambda$ controls zero existence), established with no reference to observation at all; `PPN3` is a purely PPN fact (the identity $\beta=\lambda+2$), established with no reference to zeros at all. This tutorial's contribution is noting that the *one number* measured in `PPN6` simultaneously feeds both facts, so a single weak-field measurement carries information about both "which member" and "does a zero exist" — a connection neither earlier tutorial states on its own.

## What the paper claims here

Grounded in Sec. 5.5: "Sec 3: zero iff $\lambda<0$; with $\lambda=\beta-2$, condition is $\beta<2$. Measured $\beta\simeq1$ far from $\beta=2$. Weak-field $\beta$ determines whether $A_\lambda$ has a finite-radius zero." The paper states this connection at exactly this level — a weak-field number determining, via sign, the existence of a zero — without further claiming a strong-field confirmation. It also preserves, throughout Sec. 3, the restraint that a zero is "called a horizon only for Schwarzschild," and that the paper does "NOT classify local regularity or global causal character" of zeros for other negative $\lambda$ — restraints this tutorial repeats in full rather than relaxing.

---
**Path navigation:** ← [prev in default path](./ppn6-reading-constraints.md) · [next](../part7-michell-pg/pg1-painleve-gullstrand.md) →
**See also:** [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md), [ZERO2](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md), [S4](../part2-schwarzschild/s4-singularities.md)
