# The Flux Law and the Freedom in the Potential Variable

> **Tutorial `CORE1`** · Part 3 · **Goal:** Show that (I1)–(I3) do *not* close the system — you are free to choose *which* function $V(A)$ obeys the Gauss law, and different choices give different nonlinear metrics that agree at Newtonian order. · **Prereqs:** [CORE0](./core0-four-assumptions.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md), [F6](../part1-foundations/f6-newtonian-limit.md)

**Where this sits in the arc.** This is **crux 1**, the conceptual center of the whole construction. Almost everything downstream is mechanical once you *feel* this one thing: a vacuum Gauss law plus $AB=1$ plus the Newtonian limit **does not determine the metric**. There is a genuine, honest, un-removable freedom in which potential variable the flux law acts on, and that freedom is what the whole family lives in. If you internalize nothing else from Part 3, internalize this.

## The flux law fixes a function — but not *which* function

Assumption (I2) says: there is *some* monotonic $V(A)$ with $\Delta V = 0$, where $\Delta = \frac{1}{r^2}\frac{d}{dr}(r^2\frac{d}{dr})$. Let us solve that equation once and for all, because it is easy. $\Delta V = 0$ means $r^2 V'(r)$ is constant:

$$\frac{d}{dr}\!\left(r^2 V'\right) = 0 \;\Rightarrow\; r^2 V' = -K \;\Rightarrow\; V'(r) = -\frac{K}{r^2} \;\Rightarrow\; V(r) = V_\infty - \frac{K}{r}.$$

So the flux law forces $V$ to be *linear in $1/r$*. That is the entire content of (I2): the chosen potential variable falls off like a Newtonian $1/r$ field. Using asymptotic flatness and the Newtonian match ([F6](../part1-foundations/f6-newtonian-limit.md)) to fix the constants, we normalize

$$V(r) = 1 - \frac{r_s}{r} + \dots$$

Now here is the hinge. **The flux law tells us $V$ as a function of $r$. It says nothing about how $V$ depends on $A$.** And $A$ is the physics — $A$ is what appears in the metric, what redshifts clocks, what bends orbits. Knowing $V(r)$ pins $A(r)$ *only if we have already decided what function $V(A)$ is*. (I2) does not decide that. It just asserts that *some* monotonic $V(A)$ works.

## Feel the freedom: three legal choices, three different metrics

Suppose we guess $V = A$ itself. Then $\Delta A = 0$, so $A = 1 - r_s/r$ directly:

$$\text{(choice } V=A\text{)}\qquad A(r) = 1 - \frac{r_s}{r}. \qquad\text{(Schwarzschild)}$$

Now suppose instead $V = \ln A$. Then $\Delta(\ln A) = 0$, so $\ln A = -r_s/r$, giving

$$\text{(choice } V=\ln A\text{)}\qquad A(r) = e^{-r_s/r} = 1 - \frac{r_s}{r} + \frac{1}{2}\frac{r_s^2}{r^2} - \dots$$

Now suppose $V = 1/A$. Then $\Delta(1/A) = 0$, so $1/A = 1 + r_s/r$ (the constant fixed by the Newtonian match), giving

$$\text{(choice } V=1/A\text{)}\qquad A(r) = \left(1 + \frac{r_s}{r}\right)^{-1} = 1 - \frac{r_s}{r} + \frac{r_s^2}{r^2} - \dots$$

Look at these three. **Every one of them satisfies (I1), (I2), and (I3).**

- (I2) holds by construction: each has *some* monotonic function of $A$ obeying the exact flux law. For the first it is $A$; for the second $\ln A$; for the third $1/A$. All three are perfectly legitimate monotonic potential variables.
- (I1) holds: expanding each in $x = r_s/r$ gives $A = 1 - x + O(x^2)$. **They are identical at Newtonian order.** The leading redshift, the far-field orbit, the mass — all the same.
- (I3) holds: set $B = 1/A$ in each.

Yet they are **different spacetimes**. They differ starting at $O(x^2)$: the $x^2$ coefficients are $0$, $\tfrac12$, and $1$ respectively. Different curvature, different strong-field behavior, different answer to "is there a horizon." One metric per choice of potential variable, and nothing in (I1)–(I3) prefers one choice over another.

That is the freedom. It is not a gap in our cleverness that a harder calculation would close. It is a real degree of freedom that the assumptions *leave open*.

## Why this is exactly a representation / gauge freedom

For a CS-trained reader the shape of this is familiar. We have an equation (the flux law) that is invariant under a huge group of reparameterizations of the field: any monotonic relabeling $A \mapsto V(A)$ produces an equally valid "potential" for which the *same* $1/r$ solution is legitimate. The physics we care about is $A$; the flux law is written in a *representation* $V$; and the map between representation and physics — the function $V(A)$ — is not fixed by the equation. Choosing $V(A)$ is a **closure choice** or a **regularization choice**: an extra stipulation, external to the flux law, that makes an underdetermined system determinate.

Three ways to say the same warning:

- **Underdetermination.** "$\Delta V = 0$ for some $V(A)$" has infinitely many solutions for $A(r)$, one per monotonic $V(A)$.
- **Question-begging.** "Just apply Gauss's law to the potential" quietly assumes you have already named the potential. Which function of the metric *is* the potential? That naming is the entire content that (I1)–(I3) fail to supply.
- **Gauge.** The nonlinear structure of the metric is pure gauge with respect to the flux law: you can dial it continuously without leaving the solution set of (I1)–(I3).

The reason so many "simple derivations" each confidently produce Schwarzschild is that each one silently picks the representation $V = A$ (apply the flux law to $g_{tt}$ directly). That is *a choice*, not a consequence. Pick $\ln A$ or $1/A$ instead and you derive a different metric with equal right.

## What tames it: (I4) is the closure

An infinite freedom is unwieldy, and (I2)+(I3) alone give literally one metric per monotonic function — far too much. Assumption (I4) is the closure that collapses this to a *one-parameter* family. Instead of leaving the potential variable arbitrary, (I4) demands that when the flux law is rewritten in a *fixed* metric variable, the nonlinear coefficient be a single constant $\lambda$. The three choices above are then just $\lambda = -1$ ($V=A$), $\lambda = 0$ ($V=\ln A$), and $\lambda = +1$ ($V=1/A$) — the endpoints and midpoint of a continuum. The next tutorial, [CORE2](./core2-log-variable-closure.md), builds that continuum. But keep sight of the moral: **$\lambda$ is a leftover of a representation choice that the physical assumptions never nailed down.** It is a property of the closure, not of gravity.

## Simpler on-ramp

Here is the whole idea with no metric at all.

Gauss's law for a point source says a field spreads over spheres, so *something* falls off like $1/r$. Fine. But suppose I only tell you "*some monotonic function of the temperature* falls off like $1/r$." Is the temperature itself $1 - r_s/r$? Or is $\ln(\text{temperature})$ the thing that goes like $1/r$? Or $1/\text{temperature}$? Each gives a *different* temperature profile, and all three have the same far-away behavior. You cannot recover the temperature from "some function of it obeys the law" — you also need to be told *which* function.

In our problem the "temperature" is $A$, the metric coefficient that does the real physical work, and the "some function" is the potential variable $V(A)$. The flux law constrains $V$, but the physics lives in $A$, and the dictionary between them is a free choice. That free choice is the parameter $\lambda$.

## Check your understanding

1. Solve $\Delta V = 0$ from scratch. What is the most general solution, and why does (I2) therefore *only* say "$V$ is affine in $1/r$"?
2. The three sample metrics ($V=A$, $\ln A$, $1/A$) all satisfy (I1). At what order in $x=r_s/r$ do they first disagree, and what does that tell you about which observations can see the difference?
3. In what precise sense is the choice of potential variable a "gauge" or "representation" freedom rather than a physical fact?
4. Why does adding (I4) not eliminate the freedom entirely, but only reduce it to one number?

<details>
<summary>Answers</summary>

- **1.** $r^2 V' = \text{const} \Rightarrow V = V_\infty - K/r$. So (I2) forces $V$ (whatever function of $A$ it is) to be affine in $1/r$; it constrains $V(r)$, never $V(A)$.
- **2.** They agree through $O(x)$ (all give $1 - x$) and first differ at $O(x^2)$, with coefficients $0, \tfrac12, 1$. So any purely Newtonian-order observation (leading redshift, far-field orbits) is *blind* to the difference; you need a nonlinear-order test.
- **3.** The flux law is invariant under any monotonic relabeling $A\mapsto V(A)$: each relabeling yields a legitimate potential with the same $1/r$ solution. The map $V(A)$ — hence the nonlinear metric — is not determined by the equation, exactly like a gauge choice.
- **4.** (I4) does not name the representation; it only demands the nonlinear coefficient be *constant* in a fixed variable. Constancy is one condition, leaving one free number, the constant itself: $\lambda$.

</details>

## What the paper claims here

Grounds: §2.1 (I2) and §2.2. The paper states directly that *"the flux law does not specify which function of $A$ plays the role of $V$,"* and that an exact flux law **for $A$, for $\ln A$, or for $1/A$ gives different nonlinear metrics though all agree at Newtonian order.** It stresses that $\Delta$ is the ordinary radial flux operator (not Laplace–Beltrami, not the wave operator) and that the flux law is a **postulate, not a covariant field equation and not a consequence of the Einstein equations**. The paper does **not** claim (I1)–(I3) close the system — it says the opposite, and introduces (I4) precisely to supply the missing closure.

---
**Path navigation:** ← [prev in default path](./core0-four-assumptions.md) · [next](./core2-log-variable-closure.md) →
**See also:** [CORE2](./core2-log-variable-closure.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md), [PG2](../part7-michell-pg/pg2-where-did-curvature-go.md)
