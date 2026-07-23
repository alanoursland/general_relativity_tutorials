# Deriving Schwarzschild the standard way

> **Tutorial `S2`** · Part 2 · **Goal:** Solve $R_{\mu\nu}=0$ for the static, spherically symmetric, asymptotically flat exterior — the honest derivation the paper's shortcut will later be measured against. · **Prereqs:** [S1](./s1-vacuum-einstein.md), [SYM1](../part1-foundations/sym1-static-spherical.md)

**Where this sits in the arc.** This is the "real answer," derived the hard way, so that when Part III builds a whole *family* of metrics from four lightweight postulates, you can see exactly which step the shortcut skips and what it costs. Keep this derivation in mind through `BIRK`, `CORE-CONTRAST`, and beyond.

## Setting up the ansatz

Start from the static, spherically symmetric, asymptotically flat metric (justified in `SYM1`):

$$ds^2 = -A(r)\,c^2 dt^2 + B(r)\,dr^2 + r^2 d\Omega^2, \qquad d\Omega^2 = d\theta^2 + \sin^2\theta\,d\phi^2,$$

with $A, B \to 1$ as $r\to\infty$ (asymptotic flatness) and $A>0$ on the branch we work on. The unknowns are the two functions $A(r)$ and $B(r)$; everything else is fixed by the symmetry.

## The curvature content of the ansatz

Computing the Ricci tensor for this metric is a mechanical (if lengthy) exercise in Christoffel symbols — the same machinery introduced for geodesics in `F5` and curvature in `F7`, just carried through in full for this particular metric. We quote the standard result, as any GR textbook does at this point, and spend our effort on what comes *after*: the nonzero components work out to

$$R_{tt} = \frac{A''}{2B} - \frac{A'}{4B}\left(\frac{A'}{A}+\frac{B'}{B}\right) + \frac{A'}{rB},$$

$$R_{rr} = -\frac{A''}{2A} + \frac{A'}{4A}\left(\frac{A'}{A}+\frac{B'}{B}\right) + \frac{B'}{rB},$$

$$R_{\theta\theta} = 1 - \frac1B + \frac{r}{2B}\left(\frac{A'}{A} - \frac{B'}{B}\right), \qquad R_{\phi\phi} = \sin^2\theta\, R_{\theta\theta},$$

where primes denote $d/dr$. The vacuum condition $R_{\mu\nu}=0$ demands all of these vanish simultaneously.

## Step 1: a combination kills the second derivatives

Rather than attacking each equation separately, form $B\,R_{tt}/A + R_{rr}$. The $A''$ terms cancel between the two (they enter with opposite sign and matching prefactors once you divide the first by $A$ and use $B/A\cdot A/B=1$), leaving

$$\frac{R_{tt}}{A} + \frac{R_{rr}}{B} = \frac{A'B+AB'}{rAB^2} = \frac{(AB)'}{rAB^2}.$$

Since both $R_{tt}$ and $R_{rr}$ vanish in vacuum, the left side is zero, forcing

$$(AB)' = 0 \quad\Longrightarrow\quad AB = \text{const}.$$

Asymptotic flatness ($A,B\to1$ as $r\to\infty$) fixes that constant to $1$:

$$\boxed{AB = 1}, \qquad B = \frac1A.$$

This is worth pausing on. In the paper's construction, $AB=1$ is *assumed* outright as postulate (I3) — one of four independent ingredients fed in by hand. Here, solving the actual vacuum field equations, the very same relation falls out as a *consequence* of $R_{tt}=R_{rr}=0$ plus asymptotic flatness. It costs nothing extra: it is not an assumption but a theorem. This is the first concrete place where "characterize the full solution set of the real equations" and "postulate convenient-looking conditions" visibly diverge — flagged again in `CORE-CONTRAST`.

## Step 2: integrating the remaining equation

With $B=1/A$, substitute into $R_{\theta\theta}=0$. Using $B'/B = -A'/A$, the bracket becomes $A'/A - B'/B = 2A'/A$, so

$$R_{\theta\theta} = 1 - A + \frac{r}{2}A\cdot\frac{2A'}{A} = 1 - A + rA' = 0.$$

Rearranging, $rA' + A = (rA)' $, wait — check directly: $\dfrac{d}{dr}(rA) = A + rA'$. So $R_{\theta\theta}=0$ reads

$$\frac{d}{dr}(rA) = 1.$$

Integrate once:

$$rA(r) = r + C \quad\Longrightarrow\quad A(r) = 1 + \frac{C}{r},$$

for some integration constant $C$. Asymptotic flatness is already satisfied for any $C$ (since $C/r\to0$). To fix $C$, match the weak-field limit worked out in `F6`: $A = 1 - r_s/r + O(r^{-2})$ with $r_s = 2GM/c^2$. Comparing term by term, $C = -r_s$. Hence

$$\boxed{A(r) = 1 - \frac{r_s}{r}}, \qquad B(r) = \frac{1}{A(r)} = \left(1-\frac{r_s}{r}\right)^{-1}.$$

This is the Schwarzschild metric:

$$ds^2 = -\left(1-\frac{r_s}{r}\right)c^2dt^2 + \left(1-\frac{r_s}{r}\right)^{-1}dr^2 + r^2 d\Omega^2, \qquad r_s = \frac{2GM}{c^2}.$$

## Step 3: consistency, not new information

Two equations, $R_{tt}=0$ and $R_{rr}=0$, were used only in the combination that produced $AB=$ const; you might worry we never separately verified them. Substituting the solved $A(r)$, $B(r)$ back in, both do vanish identically — but this is not a coincidence requiring luck. It is a structural fact about the Einstein equations: the contracted Bianchi identity guarantees $\nabla^\mu G_{\mu\nu}\equiv0$ automatically, which makes the four field equations along any one coordinate direction linearly dependent on the others. Concretely here, once $R_{\theta\theta}=0$ and $(AB)'=0$ hold, $R_{tt}=0$ and $R_{rr}=0$ are guaranteed for free. This redundancy is a general feature of solving Einstein's equations, not special to the vacuum spherical case.

## What this derivation used — and what it didn't assume

Notice what never had to be postulated: the reciprocal relation $AB=1$ was *derived*; the mass parameter $r_s$ entered only once, as a single integration constant fixed by matching a known weak-field limit; and no separate rule about "how the field falls off" (a flux law) was needed — $R_{\theta\theta}=0$ *is* the vacuum field equation in this component, not a substitute for it. There is exactly one undetermined constant in the whole derivation, and it gets fixed by the Newtonian limit. There is no leftover freedom analogous to the paper's $\lambda$ — full vacuum Einstein gravity in this ansatz has a unique solution up to the value of $M$. That uniqueness, and its precise scope, is the subject of `BIRK`.

## Simpler on-ramp

Think of it as solving a jigsaw with three separate pieces of information — one equation for the $tt$ part, one for the $rr$ part, one for the angular part — that all have to fit the same two unknown functions $A(r)$ and $B(r)$ at once. It turns out two of the three pieces combine algebraically to say "$A$ and $B$ are reciprocals of each other" (no integration needed), and the third piece, once you substitute that in, becomes a one-line ordinary differential equation you can integrate immediately: $\frac{d}{dr}(rA)=1$. The one leftover constant of integration is exactly the total mass, read off by comparing to Newton's law far from the source. Nothing else is free — that's the whole content of "solving vacuum Einstein's equations here has a unique answer."

## Check your understanding

- Why does asymptotic flatness alone fix the constant in $AB=$const, but a *different* physical input (the Newtonian limit) is needed to fix the constant in $A=1+C/r$?
- What role does the contracted Bianchi identity play in this derivation, practically?
- If you dropped the assumption $A,B\to1$ at infinity, would $AB=1$ still follow? What would change?
- Why is it significant that $AB=1$ came out as a *theorem* here rather than an assumption?

**Answers**
- $AB=$const is fixed by a boundary condition alone (what value the product approaches far away); $C$ in $A=1+C/r$ is a genuinely different piece of information — the *strength* of the field — which only the weak-field/Newtonian correspondence can supply, since flatness at infinity says nothing about how fast you approach it.
- It guarantees that having imposed $R_{\theta\theta}=0$ and $(AB)'=0$, the remaining components $R_{tt}=0,R_{rr}=0$ are automatically satisfied — so you never have an over-determined system with no solution, and you never need to check redundant equations by brute force.
- $(AB)'=0$ still follows from $R_{tt}=R_{rr}=0$ regardless of boundary conditions — that step only used the field equations. But without asymptotic flatness the constant in $AB=$const would be some other value, rescaling time; conventionally you'd absorb it into a redefinition of $t$.
- It shows that a condition the paper must postulate by hand (I3) is, for the actual physical theory, not an independent assumption at all — it is forced by the dynamics. This sharpens exactly how much lighter the paper's four postulates are than solving Einstein's equations.

## What the paper claims here

The paper does not present this derivation — it is deliberately absent from the paper's method, which replaces the vacuum field equations with the flux postulate (I2) precisely to *avoid* this machinery. This tutorial exists so the contrast is concrete: `CORE-CONTRAST` lines this derivation up side-by-side with `CORE0`–`CORE5`. The paper's own framing (§2.5) simply notes that Schwarzschild, $A=1-r_s/r$, is the $\lambda=-1$ member obtained from *its* construction (exact flux law for the variable $A$ itself, $\Delta A = 0$) — it does not claim to have solved $R_{\mu\nu}=0$; that correspondence is a fact about General Relativity that this tutorial supplies as background, not a claim made in the paper's own argument.

---
**Path navigation:** ← [prev in default path](./s1-vacuum-einstein.md) · [next](./birkhoff.md) →
**See also:** [F5](../part1-foundations/f5-geodesics.md), [F7](../part1-foundations/f7-curvature.md), [CORE4](../part3-building-the-family/core4-classification-theorem.md), [CORE-CONTRAST](../part3-building-the-family/core-contrast.md)
