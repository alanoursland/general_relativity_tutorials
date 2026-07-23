# The Four Assumptions in Common Language

> **Tutorial `CORE0`** · Part 3 · **Goal:** State the four assumptions that build the metric family as a *specification*, not a derivation, and set up the "characterize the solution set" mindset. · **Prereqs:** [SYM1](../part1-foundations/sym1-static-spherical.md), [F6](../part1-foundations/f6-newtonian-limit.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)

**Where this sits in the arc.** This is the top of the spine. Everything downstream is *build the family → watch a sign switch → watch energy accounting fail to pick a member → watch observation succeed → explain Michell*. Before any of that we have to be exact about what we are assuming. The single most important reframing in the whole book happens right here: we are not going to *derive Schwarzschild*. We are going to write down a **specification** — four requirements — and then characterize the **entire set** of metrics that satisfy it. Schwarzschild will turn out to be one point in that set.

## From "exhibit a solution" to "characterize the solution set"

A physicist asked to find the metric outside a spherical mass usually *exhibits a solution*: writes an ansatz, imposes the vacuum Einstein equations, turns a crank, and out comes Schwarzschild. That is a fine thing to do (we do it honestly in [S2](../part2-schwarzschild/s2-deriving-schwarzschild.md)), but it answers a narrow question: *is Schwarzschild consistent with these equations?* Yes.

The paper asks a wider, more revealing question. Many "simple derivations" of Schwarzschild in the literature do not use the full Einstein equations. They use a handful of physically motivated shortcuts. So the honest question is: **what do those shortcuts, by themselves, actually pin down?** If several famous shortcuts each "derive Schwarzschild," but the shortcuts differ, then something is being smuggled in. The clean way to expose the smuggling is to write the common assumptions as a specification and ask for its *complete* solution set.

The reader from a CS background has met this move before. It is the difference between "here is a program that satisfies the spec" and "here is a characterization of *every* program the spec allows." The second is far more informative — it tells you exactly how much freedom the spec leaves, which is exactly what a later, stronger condition must remove.

## The ansatz we are specifying over

By staticity and spherical symmetry (developed in [SYM1](../part1-foundations/sym1-static-spherical.md)), and choosing the **areal radius** $r$ (a sphere at fixed $r$ has area $4\pi r^2$), the metric can always be written

$$ds^2 = -A(r)\,c^2 dt^2 + B(r)\,dr^2 + r^2\, d\Omega^2, \qquad d\Omega^2 = d\theta^2 + \sin^2\theta\, d\phi^2 .$$

We work on the **static branch** $A>0$ and require **asymptotic flatness**: $A, B \to 1$ as $r \to \infty$. Two unknown functions, $A(r)$ and $B(r)$. The four assumptions are conditions on these two functions.

## The four assumptions

**(I1) Newtonian weak-field limit.** Far from the mass, a slowly moving test particle must feel Newtonian gravity with potential $\Phi = -GM/r$. As shown in [F6](../part1-foundations/f6-newtonian-limit.md), matching the geodesic equation to Newton's second law forces

$$A = 1 + \frac{2\Phi}{c^2} + O\!\left(\frac{\Phi^2}{c^4}\right) = 1 - \frac{2GM}{rc^2} + O(r^{-2}).$$

Define the **gravitational radius** $r_s \equiv 2GM/c^2$ and the dimensionless $x \equiv r_s/r$, so $A = 1 - x + O(x^2)$. This fixes the mass scale and the *leading* term of $A$. It says **nothing** about the nonlinear ($x^2$ and higher) terms.

**(I2) Areal-coordinate flux law.** There exists a monotonic function $V(A)$ of the metric that obeys an exact source-free Gauss law in the flat radial operator,

$$\Delta V \equiv \frac{1}{r^2}\frac{d}{dr}\!\left(r^2 \frac{dV}{dr}\right) = 0 .$$

This is the assumption that mimics "field lines spread over $4\pi r^2$, so flux is conserved." Two cautions the paper is emphatic about, and we inherit: (a) $\Delta$ is the **flat-space radial flux operator** built from the areal $r$ — *not* the Laplace–Beltrami operator of the curved spatial slice, and *not* the wave operator; (b) this flux law is a **postulate**, not a covariant field equation and not a consequence of the Einstein equations. Its coordinate-dependence is precisely why it is a postulate ([GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)).

**(I3) Reciprocity, $AB = 1$.** The time and radial metric coefficients are locked together: $A(r)B(r) = 1$, i.e. $g_{tt}g_{rr} = -1$, so $B = 1/A$. Schwarzschild satisfies this. It is *not* a consequence of static spherical symmetry alone; in simple derivations it enters as an added assumption or from an auxiliary argument. Geometrically it says the gravitational slowing of clocks, $d\tau = \sqrt{A}\,dt$, is accompanied by exactly the inverse stretching of radial proper distance, $d\ell = \sqrt{B}\,dr = dr/\sqrt{A}$. This cuts the unknowns from two functions to one, but by itself cannot select a member.

**(I4) Constant nonlinear coefficient.** When the flux law is rewritten in a fixed metric variable, the coefficient of its nonlinear (squared-gradient) term is a **constant of the theory**, not a function of local field strength. This is the *closure*: it forbids that coefficient from drifting with position. It permits the value zero (no nonlinearity at all); it forbids only that the coefficient be a function $\lambda(A)$ rather than a number $\lambda$. Everything we prove is **complete relative to (I1)–(I4)** — no more, no less.

## What kind of object we have built

We now have a specification, not a solution. (I1) fixes the leading behavior; (I3) removes one of the two unknown functions; (I2) plus (I4) constrain the nonlinear part. The natural next questions — and the plan of Part 3 — are:

- Do (I1)–(I3) *close* the system, i.e. force a unique $A(r)$? (No — that is the crux, [CORE1](./core1-flux-freedom.md).)
- What does adding (I4) leave? (A one-parameter family, [CORE2](./core2-log-variable-closure.md)–[CORE4](./core4-classification-theorem.md).)
- Where do the members differ, and which real condition finally selects one? (Later parts.)

Keep the discipline the paper models: at each step, mark whether a condition **builds** the family or **selects** within it, and name exactly what it adds.

## Simpler on-ramp

Think of the four assumptions as four constraints on a curve $A(r)$ that starts at $A=1$ far away and dips as you approach the mass.

- (I1) says: *near the far end, the curve must start dropping with a specific slope* — the Newtonian slope set by the mass. It pins the beginning of the dip, nothing else.
- (I2) says: *some rescaled version of the curve must fall off exactly like $1/r$*, the way a flux-conserving field does. But it pointedly does **not** say which rescaling — the curve itself? its logarithm? its reciprocal?
- (I3) says: *the radial-distance stretching is exactly the reciprocal of the time-slowing*, so once you know $A$ you know $B$. One function to find, not two.
- (I4) says: *the "strength of nonlinearity" is one fixed number, the same everywhere*, not something that changes as gravity gets stronger.

The surprise, coming next, is that (I1)–(I3) leave the middle of the curve genuinely free, and (I4) tames that freedom down to a single knob $\lambda$.

## Check your understanding

1. Why is "characterize the solution set" a stronger result than "exhibit Schwarzschild"?
2. Which assumption reduces the two unknown functions $A,B$ to one? Does it, by itself, determine $A(r)$?
3. The operator $\Delta$ here looks like a Laplacian. What is it *not*, and why does that matter?
4. (I4) permits $\lambda = 0$. In words, what physical situation is $\lambda = 0$?

<details>
<summary>Answers</summary>

- **1.** It tells you *everything* the assumptions allow, hence exactly how much freedom remains — which is precisely what a later selecting condition must remove. Exhibiting one solution hides that freedom.
- **2.** (I3), $AB=1$, gives $B=1/A$. No: it only ties $B$ to $A$; the single remaining function $A(r)$ is still unconstrained in its nonlinear part.
- **3.** It is the *flat-space radial flux operator* in the areal coordinate, not the Laplace–Beltrami operator of the curved slice and not the wave operator. This is why (I2) is a coordinate-dependent postulate, not a covariant field equation.
- **4.** No nonlinear self-strengthening of the field: the flux law holds exactly for $\ln A$, giving the exponential member $A_0 = e^{-r_s/r}$.

</details>

## What the paper claims here

Grounds: §1 and §2.1. The paper lists exactly these ingredients — (I1) Newtonian weak-field limit; (I2) a monotonic static potential variable obeying an exact vacuum Gauss law in areal coordinates; (I3) $g_{tt}g_{rr}=-1$; (I4) constant nonlinear squared-gradient coefficient — and frames the whole exercise as asking *"what a specified common construction determines before any selection."* The paper is explicit that (I2) is a **postulate, not the Einstein vacuum equation**, that $\Delta$ is the ordinary radial flux operator, and that (I3) does **not** follow from static spherical symmetry alone. It does **not** claim these assumptions select Schwarzschild; that is the entire point of what follows.

---
**Path navigation:** ← [prev in default path](../part2-schwarzschild/s4-singularities.md) · [next](./core1-flux-freedom.md) →
**See also:** [SYM1](../part1-foundations/sym1-static-spherical.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md), [EPI3](../part8-synthesis/epi3-build-vs-select.md)
