# Static, Spherically Symmetric Metrics

> **Tutorial `SYM1`** · Part 1 · **Goal:** understand precisely why staticity and spherical symmetry force the metric into the form $-A(r)c^2dt^2+B(r)dr^2+r^2d\Omega^2$, and pin down "static" and "asymptotically flat" exactly. · **Prereqs:** [F1](./f1-metric.md), [F2](./f2-tensors.md), [F3](./f3-special-relativity.md), [F4](./f4-curvilinear-coordinates.md).

**Where this sits in the arc.** This tutorial *is* the ansatz — the stage on which the entire book plays out. [`CORE0`](../part3-building-the-family/core0-four-assumptions.md) takes this exact form as its starting point and asks what four further assumptions do to the two free functions $A(r)$ and $B(r)$ it contains. Getting precise about what "static," "spherically symmetric," and "asymptotically flat" mean — and about how much freedom remains even after imposing all three — is the whole point here; nothing about a specific solution appears yet.

## Spherical symmetry: coordinates adapted to spheres

"Spherically symmetric" means the geometry looks identical under any rotation about a center — no direction is special. A standard, and here simply assumed, consequence of this symmetry is that you can always choose angular coordinates $\theta,\phi$ and a radial label $r$ (the **areal radius** of [`F4`](./f4-curvilinear-coordinates.md): the sphere at fixed $r$ has area $4\pi r^2$) such that:

- the induced geometry on each sphere of constant $r$ (and, if time-dependent, constant $t$) is exactly $r^2 d\Omega^2$ — no distortion, no preferred latitude or longitude; 
- there are no cross terms mixing an angular coordinate with $t$ or $r$ ($dt\,d\theta$, $dt\,d\phi$, $dr\,d\theta$, $dr\,d\phi$ all absent) — any such term would itself pick out a direction, breaking the assumed symmetry;
- nothing in the metric depends on $\theta$ or $\phi$ — again, dependence on angle would break the symmetry.

What survives is a metric of the form

$$ds^2 = g_{tt}(t,r)\,dt^2 + 2g_{tr}(t,r)\,dt\,dr + g_{rr}(t,r)\,dr^2 + r^2 d\Omega^2,$$

with (at most) three unknown functions of $t$ and $r$ only. Spherical symmetry alone has already done most of the work: it collapses an arbitrary metric's freedom down to a function of two variables, out of four.

## Static: two conditions, not one

"Static" is stronger than merely "time-independent," and it is worth separating the two parts explicitly:

1. **Stationary**: nothing depends on $t$ — $\partial_t g_{\mu\nu}=0$. This alone permits, for instance, a rotating star's exterior, which looks the same at every instant yet still "drags" nearby frames around with it.
2. **No time–space cross term**: $g_{tr}=0$ (and, more generally, no mixed term at all). This is the piece that rules out rotation/dragging-type effects — physically, "not spinning, not collapsing, not expanding." A metric that is stationary but has $g_{tr}\ne0$ (or the rotational analogue) is called merely *stationary*, not *static*; the distinction matters elsewhere in GR (e.g. rotating black holes) but is bracketed here — the paper's construction is explicitly for the static case only.

Imposing both conditions on the spherically symmetric form above removes the $t$-dependence and the cross term, leaving

$$ds^2 = -A(r)\,c^2dt^2 + B(r)\,dr^2 + r^2\,d\Omega^2,$$

where $g_{tt}\equiv -A(r)c^2$ and $g_{rr}\equiv B(r)$ are now functions of $r$ **alone** — this is the metric ansatz used throughout the entire book. We work on the **static branch** $A>0$ (formally, $A$ could reach zero somewhere; what that would mean is deliberately deferred to [`ZERO1`](../part4-family-structure/zero1-finite-radius-zeros.md)/[`ZERO2`](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) rather than assumed away or asserted here).

## Asymptotic flatness, precisely

Far from an isolated source, spacetime should approach the flat Minkowski geometry of [`F3`](./f3-special-relativity.md) — no other masses, no residual curvature "at infinity." Precisely:

$$A(r) \to 1, \qquad B(r) \to 1, \qquad \text{as } r\to\infty.$$

This is what licenses matching to the Newtonian limit at large $r$ ([`F6`](./f6-newtonian-limit.md)) and normalizing integration constants later ([`CORE4`](../part3-building-the-family/core4-classification-theorem.md)): without it, $A(r)$ and $B(r)$ could differ from $1$ arbitrarily far away, and there would be no well-defined sense in which $r_s=2GM/c^2$ measures "the" mass of an isolated source.

## What remains: two free functions, and nothing more yet

Take stock of exactly how much this tutorial has bought, and — just as importantly — how much it has *not*: starting from a wholly general metric (ten independent components, each potentially depending on all four coordinates), spherical symmetry plus staticity plus the areal-radius coordinate choice have reduced everything to **two** unknown functions of one variable, $A(r)$ and $B(r)$, subject only to $A,B\to1$ at infinity and $A>0$ on the branch considered. That is a large reduction — but it is a reduction of the *space of unknowns*, not yet a solution. Nothing said so far ties $A$ to $B$, nothing has fixed either function's numerical shape, and nothing here has invoked the Einstein field equations at all.

Worth flagging explicitly, because it is easy to smuggle in without noticing: the further condition $A(r)B(r)=1$ (i.e. $g_{tt}g_{rr}=-1$) — used throughout the rest of this book as assumption (I3) — is **not** a consequence of staticity and spherical symmetry alone. It is Schwarzschild's own relation, and it holds for every member of the later family, but deriving it here would be circular; [`CORE0`](../part3-building-the-family/core0-four-assumptions.md) introduces it explicitly as an *additional* assumption, with its own physical content (the gravitational slowing of clocks, $d\tau=\sqrt{A}\,dt$, exactly compensated by an inverse stretching of radial proper distance, $d\ell=\sqrt{B}\,dr$).

This is precisely the "characterize what a specification allows, not what one example satisfies" habit the book asks throughout ([`CORE0`](../part3-building-the-family/core0-four-assumptions.md)): this tutorial has characterized *the space of static, spherically symmetric, asymptotically flat exteriors* — a two-function family — and stops there, deliberately, before adding anything that would narrow it further.

## Simpler on-ramp

"Spherically symmetric" is like a snow globe with all the internal shaking removed — turn it any way you like about its center and it looks identical, so nothing in its description can depend on which way you're facing, only on how far out you are. "Static" adds a second condition on top of "unchanging in time": think of the difference between a perfectly still pond (static) and a whirlpool that maintains an unchanging *pattern* while the water inside it keeps circulating (stationary but not static) — a whirlpool looks the same at every instant, yet something is still moving, and that residual motion shows up exactly as the kind of cross term ($g_{tr}\ne0$) that "static" specifically forbids. "Asymptotically flat" just says: far enough from the pond, the water is undisturbed.

## Check your understanding

1. What is the difference between "stationary" and "static," and which metric component does the difference show up in?
2. After imposing spherical symmetry, staticity, and asymptotic flatness, how many free functions remain, and of how many variables?
3. Is $A(r)B(r)=1$ a consequence of the assumptions in this tutorial? If not, what kind of assumption is it?
4. Why does "areal radius" need to be chosen explicitly as part of this ansatz, rather than being automatic?

<details>
<summary>Answers</summary>

- **1.** "Stationary" only requires no $t$-dependence in the metric components; "static" additionally requires no $g_{tr}$ (time–space) cross term. The difference shows up exactly in whether $g_{tr}=0$ — a rotating source can be stationary (unchanging pattern) without being static (frame-dragging, encoded in a nonzero cross term).
- **2.** Two free functions, $A(r)$ and $B(r)$, each depending on the single variable $r$ only.
- **3.** No — it is not implied by staticity, spherical symmetry, or asymptotic flatness alone. It is a genuinely additional assumption (I3 in the book's numbering), introduced separately in [`CORE0`](../part3-building-the-family/core0-four-assumptions.md).
- **4.** Because spherical symmetry alone only guarantees that *some* radial label exists making the angular part proportional to (that label)$^2$; choosing that label to specifically match the sphere's actual area ($4\pi r^2$) is an extra, convenient convention — a coordinate choice — not something forced by symmetry by itself. A different radial label (e.g. isotropic, [`PPN2`](../part6-ppn-observation/ppn2-areal-isotropic.md)) is equally consistent with the same symmetry.

</details>

## What the paper claims here

Grounds §2 directly, quoting closely: "Metric (areal coords): $ds^2 = -A(r)c^2dt^2 + B(r)dr^2 + r^2 d\Omega^2$... $r$ = areal radius (sphere at fixed $r$ has area $4\pi r^2$). Static branch $A>0$; asymptotic flatness $A,B\to1$ as $r\to\infty$." The paper treats this as the starting ansatz — a specification of the space of exteriors under consideration — and is explicit throughout that later assumptions like $AB=1$ are additional constraints on top of it, "not a consequence of static spherical symmetry alone."

---
**Path navigation:** ← [prev in default path](./f6-newtonian-limit.md) · [next: F7 — Curvature, briefly](./f7-curvature.md) →
**See also:** [CORE0](../part3-building-the-family/core0-four-assumptions.md), [S1](../part2-schwarzschild/s1-vacuum-einstein.md)
