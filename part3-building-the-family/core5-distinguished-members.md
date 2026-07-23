# Distinguished Members and Shuler's Metrics

> **Tutorial `CORE5`** · Part 3 · **Goal:** Catalogue the members $\lambda = -1, 0, +1$, show the $\lambda \to 0$ exponential is the *continuous* bridge across the family, and place Shuler's three metrics as points on the continuum via $n = 2\lambda$. · **Prereqs:** [CORE4](./core4-classification-theorem.md), [CORE3](./core3-essential-variable.md)

**Where this sits in the arc.** We have the complete family $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$. Before moving on to *select* a member, it pays to know the terrain: the three cleanest members, how the exponential at $\lambda = 0$ knits them together, and how metrics that appeared in the literature as separate "alternatives" are in fact three samples of one continuum. Recognizing that is a small instance of the book's method — what looked like a menu of rival theories is a single parameterized family.

## The three distinguished members

Each value of $\lambda$ corresponds to a specific *essential variable* $A^{-\lambda}$ — the function of the metric that obeys the plain $1/r$ flux law ([CORE3](./core3-essential-variable.md)). Three values give especially clean essential variables and metrics.

| $\lambda$ | essential (exact-flux) variable | $A_\lambda(r)$ | description |
|---|---|---|---|
| $-1$ | $A$ | $1 - r_s/r$ | **Schwarzschild** — $\Delta A = 0$ |
| $0$ | $\ln A$ | $e^{-r_s/r}$ | **exponential** — $\Delta \ln A = 0$ |
| $+1$ | $1/A$ | $(1 + r_s/r)^{-1}$ | **reciprocal** — $\Delta(1/A) = 0$ |

Reading the table across is worthwhile. At $\lambda = -1$ the flux law is applied to $A$ itself, and the metric coefficient $g_{tt}$ falls off like a plain Newtonian potential, $1 - r_s/r$ — this is Schwarzschild in areal coordinates, and it is the "obvious" choice most simple derivations make silently ([CORE1](./core1-flux-freedom.md)). At $\lambda = 0$ the flux law is applied to $\ln A$; there is no nonlinear term at all, and $A = e^{-r_s/r}$. At $\lambda = +1$ the flux law is applied to $1/A$, giving the reciprocal member. These are the same three "guesses" we met by hand in [CORE1](./core1-flux-freedom.md) — now understood as the three integer-labeled points $\lambda \in \{-1, 0, +1\}$ of a continuum.

Every member shares $A_\lambda = 1 - r_s/r + O(x^2)$ ([WEAK1](./weak1-weak-field-degeneracy.md)), so all three agree at Newtonian order and differ only at $O(x^2)$, where the coefficient $\frac{1+\lambda}{2}$ takes the values $0$, $\tfrac12$, $1$.

## The exponential as the continuous bridge

It is easy to picture $\lambda = 0$ as an awkward special case (the exponent $-1/\lambda$ blows up). The opposite is true: $A_0 = e^{-r_s/r}$ is the **hinge that makes the family one connected object** rather than two disconnected halves. Recall from [CORE4](./core4-classification-theorem.md) that

$$\lim_{\lambda\to 0}\left(1 + \lambda\frac{r_s}{r}\right)^{-1/\lambda} = e^{-r_s/r},$$

so the curve passes *smoothly* from negative $\lambda$ to positive $\lambda$ through the exponential. This continuity is not cosmetic; it carries real structure:

- **Sign of the zero.** For $\lambda < 0$ the member has a finite-radius zero at $r = -\lambda r_s$; for $\lambda > 0$ it has none; the exponential $\lambda = 0$ is the boundary case, positive for all finite $r > 0$ but approaching zero as $r \to 0$. The exponential is exactly where the horizon-type zero is about to appear (Part 4).
- **Nonlinear coefficient.** The $O(x^2)$ coefficient $\frac{1+\lambda}{2}$ passes through $\tfrac12$ at the exponential, interpolating between Schwarzschild's $0$ and the reciprocal's $1$.
- **PPN parameter.** Later we find $\beta = \lambda + 2$, so the exponential sits at $\beta = 2$, midway in the observationally relevant range and exactly the value $\beta = 2$ below which finite-radius zeros exist ([PPN7](../part6-ppn-observation/ppn7-beta-and-horizon.md)).

So $\lambda = 0$ is not a member to be embarrassed about; it is the axle the family turns on. Whenever you are tempted to think of Schwarzschild ($\lambda=-1$) and the reciprocal ($\lambda=+1$) as opposite species, remember they are joined by a single smooth arc through $e^{-r_s/r}$.

## Shuler's three metrics as points on the continuum

Shuler (2018) presented Schwarzschild together with two alternative static metrics in a common parameterized form,

$$g_{tt} = -\left(1 + n\,\frac{GM}{rc^2}\right)^{-2/n},$$

treating them as three candidate exteriors. We can show these are simply three members of *our* family, and read off the dictionary. Use $\frac{GM}{rc^2} = \frac{r_s}{2r} = \frac{x}{2}$ (since $r_s = 2GM/c^2$), so Shuler's form is

$$-g_{tt} = \left(1 + \frac{n}{2}x\right)^{-2/n}.$$

Compare with our member $A_\lambda = (1 + \lambda x)^{-1/\lambda}$. Matching the **coefficient inside the parenthesis** requires $\frac{n}{2} = \lambda$, and matching the **exponent** requires $-\frac{2}{n} = -\frac{1}{\lambda}$; both give the same relation. Hence

$$\boxed{\,n = 2\lambda\,}, \qquad \lambda = \frac{n}{2}.$$

Shuler's three choices $n = -2, -1, +1$ therefore correspond to

$$n = -2 \;\to\; \lambda = -1 \ (\text{Schwarzschild}), \qquad n = -1 \;\to\; \lambda = -\tfrac12, \qquad n = +1 \;\to\; \lambda = +\tfrac12.$$

So what Shuler offered as three separate metrics are three points $\lambda \in \{-1, -\tfrac12, +\tfrac12\}$ of the single continuous class. This is the recurring pattern of the paper's synthesis (see [SYN1](../part8-synthesis/syn1-century-of-shortcuts.md)): apparent rivals in the literature are members of one family, and the interesting question is not "which of these three?" but "what condition selects a point on the whole continuum?" Kassner (2019) supplies one such condition — a standard relativistic generalization of Newton's law — which among Shuler's picks Schwarzschild ($\lambda = -1$); but that is a *selecting* input added on top of the family, not something the family itself provides.

The two half-integer members $\lambda = \pm\tfrac12$ are physically live, not curiosities: they give $\beta = \tfrac32$ and $\tfrac52$, distinguishable from Schwarzschild's $\beta = 1$ by perihelion precession ([PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md)). They agree with Schwarzschild only at Newtonian order and in the leading $\gamma$-controlled effects (light bending, Shapiro delay), and part company at the $\beta$-sensitive level.

## Simpler on-ramp

Think of $\lambda$ as a slider from left to right.

- Slide to $\lambda = -1$: the metric is the plain Schwarzschild $1 - r_s/r$. It hits zero at $r = r_s$.
- Slide to $\lambda = 0$: the metric is $e^{-r_s/r}$, the exponential. It is the smooth middle of the slider — the point where the "hits zero at finite radius" behavior switches off.
- Slide to $\lambda = +1$: the metric is $1/(1 + r_s/r)$, the reciprocal. It never hits zero.

Nothing jumps as you move the slider; the exponential in the middle glues the two ends into one continuous track. And several metrics that appeared in older papers as *separate* proposals — Shuler's three — are just three stops along this same slider, once you translate his label $n$ into ours with $n = 2\lambda$. There was never a menu of competing theories; there was one dial and different people had grabbed it at different settings.

## Check your understanding

1. For each of $\lambda = -1, 0, +1$, name the essential variable and the resulting $A_\lambda$.
2. Why is the $\lambda = 0$ exponential better described as a "bridge" than as a special case?
3. Derive $n = 2\lambda$ from Shuler's $g_{tt} = -(1 + nGM/(rc^2))^{-2/n}$, and map his $n = -2, -1, +1$.
4. In what sense does treating Shuler's metrics as "three alternatives" mislead?

<details>
<summary>Answers</summary>

- **1.** $\lambda=-1$: variable $A$, metric $1 - r_s/r$ (Schwarzschild). $\lambda=0$: variable $\ln A$, metric $e^{-r_s/r}$. $\lambda=+1$: variable $1/A$, metric $(1+r_s/r)^{-1}$.
- **2.** The family is continuous through it: $\lim_{\lambda\to0}(1+\lambda r_s/r)^{-1/\lambda} = e^{-r_s/r}$. It joins the negative-$\lambda$ (zero-having) and positive-$\lambda$ (zero-free) halves smoothly, and marks the switch in zero-existence, in the $O(x^2)$ coefficient, and in $\beta = 2$.
- **3.** Using $GM/(rc^2) = x/2$, Shuler's form is $(1 + \tfrac n2 x)^{-2/n}$; matching to $(1+\lambda x)^{-1/\lambda}$ gives $\tfrac n2 = \lambda$, i.e. $n = 2\lambda$. So $n=-2\to\lambda=-1$, $n=-1\to\lambda=-\tfrac12$, $n=+1\to\lambda=+\tfrac12$.
- **4.** They are not distinct theories but three points of one continuous family; the real question is which *added* condition selects a member, not which of the three is right. (Kassner 2019 supplies such a condition and picks $\lambda=-1$.)

</details>

## What the paper claims here

Grounds: §2.5. The paper's table lists $\lambda = -1$ (variable $A$, $1 - r_s/r$, Schwarzschild), $\lambda = 0$ (variable $\ln A$, $e^{-r_s/r}$, exponential), $\lambda = +1$ (variable $1/A$, $(1+r_s/r)^{-1}$, reciprocal). It records Shuler (2018), $g_{tt} = -(1 + nGM/(rc^2))^{-2/n}$ with $n = 2\lambda$, so his $n = -2, -1, +1$ map to $\lambda = -1, -\tfrac12, +\tfrac12$, and notes Kassner (2019): only Schwarzschild satisfies a standard relativistic generalization of Newton's law — a *selecting* condition applied to the family, not part of building it.

---
**Path navigation:** ← [prev in default path](./weak1-weak-field-degeneracy.md) · [next](./core-contrast.md) →
**See also:** [CORE4](./core4-classification-theorem.md), [SYN1](../part8-synthesis/syn1-century-of-shortcuts.md), [PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md)
