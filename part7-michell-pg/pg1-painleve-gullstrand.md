# PG1 — Painlevé–Gullstrand coordinates & the river model

> **Tutorial `PG1`** · Part VII · **Goal:** Derive the Painlevé–Gullstrand time shift for the *whole* $\lambda$-family and show it produces flat spatial slices plus the "river of space" picture. · **Prereqs:** [F3](../part1-foundations/f3-special-relativity.md), [F4](../part1-foundations/f4-curvilinear-coordinates.md), [CORE4](../part3-building-the-family/core4-classification-theorem.md), [S4](../part2-schwarzschild/s4-singularities.md)

**Where this sits in the arc.** The family is built (Part III), its causal structure is sharpened by the sign of $\lambda$ (Part IV), and two selectors have already been tried — energy accounting (Part V) and PPN observation (Part VI). This part supplies the *third* selector, and it starts here: a new time coordinate that rewrites every family member's metric in a strikingly simple "flowing space" form, setting up the exact-infall condition that will finally pin $\lambda=-1$ from kinematics alone.

## The problem with the static time coordinate

Every member of the family, in areal coordinates, reads
$$ds^2 = -A(r)c^2dt^2 + \frac{dr^2}{A(r)} + r^2d\Omega^2,$$
using only the reciprocal condition (I3), $B=1/A$ — nothing here depends on which flux law selected $A_\lambda$. This form is built around observers who sit still at fixed $r$ ("static observers"), and it shows its age when $A\to0$: the $dr^2/A$ term blows up and $t$ becomes a bad coordinate, even though (as later tutorials on curvature invariants establish) nothing physically pathological need be happening there. We would like a time coordinate adapted to a different, better-behaved family of observers — ones who fall freely, so that nothing blows up when $A\to0$.

## Constructing the shift

Try a new time coordinate $T$ related to $t$ by a radius-dependent shift:
$$dt = dT - h(r)\,dr$$
for a function $h(r)$ to be chosen. Substituting $dt^2 = dT^2 - 2h\,dr\,dT + h^2 dr^2$ into the metric:
$$ds^2 = -Ac^2\big(dT^2 - 2h\,dr\,dT + h^2dr^2\big) + \frac{dr^2}{A} + r^2d\Omega^2$$
$$= -Ac^2\,dT^2 + 2Ac^2h\,dr\,dT + \left(\frac{1}{A}-Ac^2h^2\right)dr^2 + r^2d\Omega^2.$$

Choose $h(r)$ so the coefficient of $dr^2$ becomes exactly $1$ — i.e., so the radial part of a constant-$T$ slice looks Euclidean:
$$\frac1A - Ac^2h^2 = 1 \;\Longrightarrow\; Ac^2h^2 = \frac{1-A}{A} \;\Longrightarrow\; h(r) = \frac{\sqrt{1-A}}{cA}.$$
This is exactly the boxed shift of the source: $dt = dT - \dfrac{\sqrt{1-A}}{cA}\,dr$. Notice the derivation only used $B=1/A$; it works verbatim for *every* $\lambda$, not just Schwarzschild.

## The result: flat slices, one velocity function

With $h$ fixed, the cross term becomes $2Ac^2h = 2c\sqrt{1-A}$. Define
$$\boxed{v(r) \equiv c\sqrt{1-A(r)}}.$$
Then $2Ac^2h = 2v$, and the $dT^2$ coefficient rearranges as $-Ac^2 = -c^2 + c^2(1-A) = -c^2+v^2$. Collecting terms:
$$ds^2 = -(c^2-v^2)\,dT^2 + 2v\,dr\,dT + dr^2 + r^2d\Omega^2 = -c^2dT^2 + \big(dr + v\,dT\big)^2 + r^2d\Omega^2.$$
(The second form follows by expanding $(dr+v\,dT)^2 = dr^2+2v\,dr\,dT+v^2dT^2$ and checking it reproduces the first.) Set $dT=0$: the constant-$T$ slice is
$$d\ell^2 = dr^2 + r^2d\Omega^2,$$
exactly flat Euclidean 3-space in spherical coordinates — for *every* member of the family, since only (I3) was used. Flatness of the spatial slices is a generic feature of this coordinate choice, not a special property of Schwarzschild.

## The river picture — and its caveat

Hamilton and Lisle's "river model" (2008) reads $v(r)$ as the speed at which space itself flows radially inward, like a current. A photon aimed outward moves at $c$ *relative to the river*, but the river carries it inward at $v$; its net rate of change of areal radius is $dr/dT = -v+c$ (worked out fully in [PG4](./pg4-horizons-light-cones.md)). This is a genuinely useful mental picture: it makes the coordinate velocity look Newtonian, and it will do real work below.

But be precise about what $v(r)$ *is*: it is the off-diagonal metric coefficient (the "shift," in the language of a 3+1 split) produced by one particular, freely chosen function $h(r)$ — equivalently, one particular family of observers (those adapted to falling inward). There is no substance streaming through space; nothing is measured, locally, as a flow of $c\sqrt{1-A}$ meters per second past a fixed post. Choosing the opposite sign of $h(r)$ gives an equally valid *outgoing* PG coordinate with the river flowing the other way, describing the *same* spacetime. "River of space" is a physical analogy laid over a coordinate choice, not a claim that general relativity contains a literal fluid.

## The family profile

Since $v(r)=c\sqrt{1-A(r)}$ and $A_\lambda(r) = (1+\lambda r_s/r)^{-1/\lambda}$, every family member gets its own river profile:
$$v_\lambda(r) = c\sqrt{1-\left(1+\lambda\frac{r_s}{r}\right)^{-1/\lambda}}.$$
All members share the flat-slice, shifted-time *structure* derived above; they differ only in the shape of the one function $v_\lambda(r)$. That difference is where the next two tutorials do their work: [PG2](./pg2-where-did-curvature-go.md) asks where the curvature went if the slices are flat, and [PG3](./pg3-newtonian-infall.md) asks which $v_\lambda(r)$ matches Newtonian free-fall exactly.

## Simpler on-ramp

Think of $t$ as a clock reading assigned to observers who hover in place, and $T$ as a *different* clock reading, assigned observers who let themselves fall. Switching from $t$ to $T$ is just re-labeling which "now" you use at each point in space — it changes nothing physical, the way choosing a different reference frame in signal processing doesn't change the signal, only how convenient it is to read off certain features. The payoff of this particular re-labeling is that the *spatial* part of the description becomes as simple as possible (flat, ordinary 3D space) at the cost of introducing one new ingredient, $v(r)$, that couples space and time together. Nothing was flattened out of existence — it just moved into a different slot in the metric, ready to be accounted for in the next tutorial.

## Check your understanding

- Why does the shift $dt = dT - h(r)\,dr$ work for *every* member of the $\lambda$-family, not only Schwarzschild?
- If a colleague says "$v(r)$ is literally how fast space is moving," what is the precise correction?
- Does the derivation touch the angular part $r^2d\Omega^2$ of the metric at all?
- Is there only one valid choice of sign for $h(r)$, or does the construction admit an "outgoing" counterpart?

**Answers**
- Because the derivation used only $B=1/A$ (condition I3), which every member of the family satisfies by construction — none of the flux-law details that distinguish members entered the calculation.
- $v(r)$ is the off-diagonal ("shift") term produced by one particular choice of time coordinate adapted to freely-falling observers; it is not a measured material current. A different sign choice for $h(r)$ gives an equally valid, differently-flowing "river" describing the same spacetime.
- No — the shift only mixes $dt$ and $dr$; $r^2d\Omega^2$ is carried through unchanged.
- No: $h(r)=+\sqrt{1-A}/(cA)$ gives the ingoing (ordinary, black-hole-adapted) PG form used here; the opposite sign gives the outgoing (white-hole-adapted) form. Both are valid coordinate choices on the same underlying geometry.

## What the paper claims here

Grounded in Sec. 6.1: the paper derives $dt=dT-\frac{\sqrt{1-A}}{cA}dr$ starting from $ds^2=-Ac^2dt^2+dr^2/A+r^2d\Omega^2$, obtains $ds^2=-c^2dT^2+[dr+v(r)dT]^2+r^2d\Omega^2$ with $v(r)=c\sqrt{1-A(r)}$, and notes explicitly that the constant-$T$ slice $d\ell^2=dr^2+r^2d\Omega^2$ is flat. It attributes the "river of space" language to Hamilton & Lisle (2008) and is explicit that $v$ is "a representation of coordinate shift, not material velocity." The paper also gives the family profile $v_\lambda = c\sqrt{1-(1+\lambda r_s/r)^{-1/\lambda}}$ and states plainly that PG form *alone* does not select a member — that selection is the subject of the next tutorial's sequel, [PG3](./pg3-newtonian-infall.md).

---
**Path navigation:** ← [prev: PPN7](../part6-ppn-observation/ppn7-beta-and-horizon.md) · [next: PG2](./pg2-where-did-curvature-go.md) →
**See also:** [CORE4](../part3-building-the-family/core4-classification-theorem.md), [S4](../part2-schwarzschild/s4-singularities.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md)
