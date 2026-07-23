# PG3 — The unique Newtonian infall profile

> **Tutorial `PG3`** · Part VII · **Goal:** Derive that the river velocity $v_\lambda(r)$ matches the Newtonian free-fall speed *at every radius* only for $\lambda=-1$, and show this is a strictly stronger condition than the Newtonian limit itself. · **Prereqs:** [PG1](./pg1-painleve-gullstrand.md), [F6](../part1-foundations/f6-newtonian-limit.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [CORE5](../part3-building-the-family/core5-distinguished-members.md)

**Where this sits in the arc.** This is the third and final selector, and the one this book's title arc has been building to: after energy accounting (Part V) gave an interval that *excludes* Schwarzschild, and PPN observation (Part VI) gave a measurement that *selects* it, this tutorial shows a third, independent route to exactly the same answer, $\lambda=-1$ — this time from an exact kinematic identity, not a measurement. It is the crux the rest of Part VII (the horizon reading, and the Michell history) depends on.

## The Newtonian infall speed

Consider a test particle released from rest at infinity in a Newtonian potential $\Phi=-GM/r$. Energy conservation (kinetic plus potential energy is constant, and both vanish at $r=\infty$ where the particle starts at rest) gives
$$\frac12v_N^2 + \Phi(r) = 0 \quad\Longrightarrow\quad \frac12 v_N^2 = \frac{GM}{r}\quad\Longrightarrow\quad v_N^2 = \frac{2GM}{r}.$$
Writing this with $r_s=2GM/c^2$:
$$\frac{v_N^2}{c^2} = \frac{2GM}{rc^2} = \frac{r_s}{r} = x.$$
This is a purely Newtonian statement — no metric, no relativity, just $F=ma$ integrated once.

## The PG side

From [PG1](./pg1-painleve-gullstrand.md), every family member's river velocity is $v_\lambda(r)=c\sqrt{1-A_\lambda(r)}$, so
$$\frac{v_\lambda^2}{c^2} = 1-A_\lambda(r).$$
Demanding *exact* agreement with the Newtonian profile at *every* radius $r$ means demanding
$$1-A_\lambda(r) = x \quad\text{for all } r>0,$$
i.e., $A_\lambda(r)=1-x=1-r_s/r$ identically — not just approximately, and not just for large $r$. This is a functional equation on the whole curve $A_\lambda(r)$, not a single-point condition.

## Only $\lambda=-1$ survives

Recall the weak-field expansion from [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md):
$$A_\lambda(r) = 1 - x + \frac{1+\lambda}{2}x^2 + O(x^3).$$
Every family member already agrees with $A=1-x$ at first order in $x$ — that agreement is forced by the Newtonian limit (I1) built into every member, and so it distinguishes nothing. The members first differ at the *next* order, where
$$1-A_\lambda(r) = x - \frac{1+\lambda}{2}x^2 + O(x^3).$$
For this to equal $x$ exactly — for the quadratic term to vanish, and (as we check below) for every higher-order term to vanish too — requires
$$\frac{1+\lambda}{2}=0 \quad\Longrightarrow\quad \lambda=-1.$$

This is not merely a leading-order coincidence: plug $\lambda=-1$ into the exact closed form,
$$A_{-1}(r) = \left(1+(-1)\frac{r_s}{r}\right)^{-1/(-1)} = \left(1-\frac{r_s}{r}\right)^{1} = 1-\frac{r_s}{r},$$
which is *exactly* $1-x$ — a finite polynomial in $x$, with no $O(x^2)$, $O(x^3)$, or any further terms at all. So
$$1-A_{-1}(r) = \frac{r_s}{r} = x \quad\text{exactly, for every } r>0,$$
and therefore
$$\boxed{v_{-1}(r) = c\sqrt{x} = \sqrt{\frac{2GM}{r}}}$$
holds exactly, all the way from $r\to\infty$ down to $r=r_s$ (and, by continuation, beyond, on the extended Schwarzschild coordinates). For every other $\lambda\neq-1$, the quadratic (and higher) corrections are nonzero, so $v_\lambda(r)$ departs from the Newtonian curve as soon as $x$ is no longer small — the two curves are tangent at $r\to\infty$ but do not coincide.

## Why this is stronger than "the Newtonian limit"

Every member of the family already satisfies the Newtonian limit by construction (I1): as $r\to\infty$ (equivalently $x\to0$), $v_\lambda^2/c^2 \to x + O(x^2) \to v_N^2/c^2$, for *every* $\lambda$. That is a statement about weak fields only, and it distinguishes nothing — it is automatically true of the whole family. What has just been shown is qualitatively different: requiring the Newtonian-looking relation $\tfrac12v^2=GM/r$ to hold *exactly*, at *every* radius, including deep in the strong field near $r=r_s$ where $x\sim1$, is an extra, global condition — and it happens to be satisfiable by exactly one member. This is a genuine, additional selector on the family, arrived at purely from infall kinematics in PG coordinates, entirely independent of the energy-accounting argument (Part V) and the PPN measurement of $\beta$ (Part VI) — yet it lands on the same $\lambda=-1$.

## Picturing the family of profiles

Picture a plot of $v_\lambda/c=\sqrt{1-A_\lambda}$ against $r$ (or, equivalently, against $x=r_s/r$), with the Newtonian curve $\sqrt{x}$ drawn alongside for comparison. Far from the source (large $r$, small $x$), every family member's curve hugs the Newtonian curve tightly — they are visually indistinguishable there, exactly as the weak-field argument predicts. Moving inward, the curves begin to fan out. The Schwarzschild curve ($\lambda=-1$) stays locked exactly on top of the Newtonian curve all the way down, reaching $v/c=1$ precisely at $x=1$, i.e., at $r=r_s$. The other members bend away from the Newtonian curve once $x$ stops being small, bowing above or below it depending on the sign of $1+\lambda$; those with $\lambda\geq0$ never actually reach $v/c=1$ at any finite radius (their curves asymptote toward it only as $r\to0$), while other negative-$\lambda$ members do cross $v/c=1$, but at their own zero radius $r_0=-\lambda r_s$ rather than at $r_s$ — a mismatch between "where Newtonian free-fall would say light-speed is reached" and "where that member's own metric actually vanishes," except in the one case where the two coincide.

## Simpler on-ramp

Think of it like fitting curves to data: many different curves can share the same starting slope near one end and look nearly identical there — that's all "agreeing with the Newtonian limit" requires, and it's cheap; every family member does it automatically. But requiring two curves to coincide *exactly, point for point, everywhere* — not just near the start, but all the way to the far end where things get extreme — is a much stronger demand, one that (generically) only a single, very particular curve can meet. That's the difference between two songs that happen to start on the same note and two recordings that are, note for note, the identical performance.

## Check your understanding

- Why does matching the weak-field limit ($x\to0$) fail to distinguish any family member from any other?
- Which coefficient in the weak-field expansion of $A_\lambda$ must vanish for exact Newtonian agreement, and for which value of $\lambda$?
- Is $v_{-1}=\sqrt{2GM/r}$ only a weak-field approximation, or an exact statement for all $r>0$?
- If someone claims "PG shows GR reduces to Newton for infall," what is the more precise statement this tutorial supports?

**Answers**
- Because (I1) already forces every member to agree with the Newtonian potential to first order in $x$; that agreement is built into the family's construction, not a discriminating test.
- The coefficient of $x^2$, namely $(1+\lambda)/2$, must vanish, which happens only for $\lambda=-1$.
- It is exact, for all $r>0$ down to (and, in extended coordinates, through) $r=r_s$ — not an approximation valid only for large $r$.
- Only Schwarzschild's PG shift exactly reduces to the Newtonian free-fall speed at every radius; that is a much stronger and more special fact than the generic weak-field agreement every family member shares, and it is a genuine (if unconventional) selector, not a restatement of the Newtonian limit.

## What the paper claims here

Grounded in Sec. 6.2: the paper derives $v_N^2/c^2=r_s/r$ from Newtonian free-fall, states $v_\lambda^2/c^2=1-A_\lambda$ from the PG form, and shows exact agreement requires $A_\lambda=1-r_s/r$, i.e. $\lambda=-1$, giving $v_{-1}=\sqrt{2GM/r}$ exactly "throughout the Schwarzschild exterior." It explicitly frames the requirement as "a dynamical/slicing condition STRONGER than the Newtonian limit (imposes Newtonian velocity at EVERY radius, not just $r_s/r\ll1$)." Figure 3 of the paper depicts exactly the family-of-profiles comparison described above; the paper's own caveat is that PG form *alone*, without this exact-agreement condition, does not select a member — the selection comes specifically from insisting on the Newtonian relation at every radius, not from the PG coordinate transformation by itself.

---
**Path navigation:** ← [prev: PG2](./pg2-where-did-curvature-go.md) · [next: PG4](./pg4-horizons-light-cones.md) →
**See also:** [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [CORE5](../part3-building-the-family/core5-distinguished-members.md), [PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md), [PPN6](../part6-ppn-observation/ppn6-reading-constraints.md)
