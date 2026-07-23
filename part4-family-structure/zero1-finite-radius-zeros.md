# Finite-radius zeros and the sign of $\lambda$

> **Tutorial `ZERO1`** · Part 4 · **Goal:** Derive exactly when $A_\lambda$ has a finite-radius zero, and show that the sign of $\lambda$ alone decides it. · **Prereqs:** [CORE4](../part3-building-the-family/core4-classification-theorem.md), [CORE5](../part3-building-the-family/core5-distinguished-members.md)

**Where this sits in the arc.** This is the "sign switch" step of the book's spine: a single sign, buried in a parameter that started life as nothing more than a choice of which potential variable closes a flux law (`CORE2`), silently decides whether the resulting geometry has any special radius at all. Nothing here yet says whether that radius is a *horizon* — that restraint is enforced in `ZERO2`. This tutorial only establishes *where* a zero occurs and *for which $\lambda$*.

## Setting up the question

The family from `CORE4` is

$$A_\lambda(r) = \left(1+\lambda\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda = A_\lambda^{-1}, \qquad r_s = \frac{2GM}{c^2},$$

defined for $\lambda\neq0$, with the $\lambda\to0$ limit understood as the exponential $A_0=e^{-r_s/r}$ from `CORE3`. We ask: for which $r>0$, if any, does $A_\lambda(r)=0$?

## Solving for the zero

$A_\lambda$ is a power of the base $1+\lambda r_s/r$; a nonzero base raised to any finite exponent is nonzero, so $A_\lambda(r)=0$ can only happen where the base itself vanishes:

$$1+\lambda\frac{r_s}{r} = 0.$$

Solve for $r$:

$$\lambda\frac{r_s}{r} = -1 \quad\Longrightarrow\quad r = -\lambda r_s.$$

Call this candidate radius $r_0$:

$$\boxed{r_0 = -\lambda\, r_s.}$$

This is the entire computation — but its content is in what it says about sign, not its algebra.

## Sign of $\lambda$ controls existence

We need $r_0$ to be a genuine *positive*, finite radius for it to be a candidate physical zero in the exterior region $r>0$ (recall $r_s=2GM/c^2>0$ for ordinary positive mass). Since $r_0=-\lambda r_s$ and $r_s>0$:

$$r_0 > 0 \iff -\lambda > 0 \iff \lambda < 0.$$

So the existence of a finite-radius zero is governed entirely by the **sign** of $\lambda$:

$$\boxed{A_\lambda \text{ has a finite positive-radius zero} \iff \lambda < 0.}$$

## The two cases in full

**$\lambda<0$:** a zero exists at $r_0=-\lambda r_s$, and its location scales linearly with $|\lambda|$: smaller $|\lambda|$ pushes the zero in closer to $r=0$; $|\lambda|=1$ puts it at exactly $r_s$. For example, $\lambda=-1$ gives $r_0=r_s$ (Schwarzschild's horizon, `S3`); $\lambda=-1/4$ gives $r_0=r_s/4$, a zero four times closer to the center.

**$\lambda\ge0$:** the base $1+\lambda r_s/r$ is a sum of two positive terms ($1$ and $\lambda r_s/r\ge0$ for $r>0$), so it is strictly positive for every finite $r>0$, and no finite power of a positive number is zero. $A_\lambda(r)>0$ for all finite $r>0$: no zero exists at any finite radius. (The boundary case $\lambda=0$ needs separate confirmation since the formula for $A_\lambda$ isn't directly evaluated there: $A_0=e^{-r_s/r}$ is an exponential of a real number, hence always strictly positive for finite $r>0$ — consistent with the general $\lambda\ge0$ pattern by continuity.) Members with $\lambda\geq0$ are, in this precise sense, **horizonless**: since a finite-radius zero is a *necessary* condition for a horizon (established carefully in `ZERO2`), the complete absence of any zero for $\lambda\ge0$ is already enough, on its own, to rule a horizon out entirely for these members — no invariant computation is even needed to reach that particular conclusion, because there is no candidate radius to examine in the first place.

## The qualitative picture (Fig. 1 of the paper, in words)

Picture $A_\lambda(r)$ plotted against $r$ for a handful of representative values, $\lambda\in\{-1,-1/4,0,+1\}$, all sharing the same asymptotic behavior $A_\lambda\to1$ as $r\to\infty$ and the same leading approach $A_\lambda\approx1-r_s/r$ for $r\gg r_s$ (`WEAK1`). Moving inward from large $r$, the two negative-$\lambda$ curves ($\lambda=-1$ and $\lambda=-1/4$) both descend from $1$ toward $0$, reaching zero exactly at their respective $r_0=-\lambda r_s$ — the $\lambda=-1$ curve reaching zero at $r_s$, the $\lambda=-1/4$ curve reaching zero sooner, at the smaller radius $r_s/4$, then (formally) continuing to negative values for smaller $r$ still, which is outside the domain where this branch of the metric applies. The two non-negative-$\lambda$ curves ($\lambda=0$ and $\lambda=+1$) instead flatten out and approach $0$ only asymptotically as $r\to0$ (in the exponential case) or approach a strictly positive floor and never reach zero at all for any finite $r$ — they never cross the axis.

## Why this matters going forward

$\lambda$ was introduced purely as the constant nonlinear coefficient closing an otherwise-underdetermined flux law (`CORE2`) — a fact about which potential variable you chose to make exact, not (yet) a fact with any obvious physical meaning. This tutorial is the first place that abstract choice visibly controls something dramatic: whether the resulting spacetime has anything resembling a horizon at all. That is exactly the kind of silent, high-stakes consequence of a "mere" representation choice that this book keeps returning to (`EPI1`). It is also the direct bridge to observation: `PPN3` shows $\lambda=\beta-2$, so this entire existence question restates as a question about the measurable PPN parameter $\beta$ — worked out precisely in `PPN7`, where "$\beta<2$" turns out to be exactly the same condition as "$\lambda<0$" derived here.

## Simpler on-ramp

Think of $A_\lambda(r)$ as measuring "how much of the flat, far-away metric is left" at radius $r$ — starting at $1$ far away and shrinking as you move inward. For $\lambda<0$ that shrinking eventually reaches all the way down to zero at some specific finite radius $r_0$, the same way a linearly decreasing quantity eventually crosses zero if you extrapolate it far enough. For $\lambda\ge0$, the shrinking instead levels off — like an exponential decay, or a curve approaching a floor — and gets arbitrarily close to zero only in the unreachable limit $r\to0$, never actually touching it at any finite distance from the center. The entire question "does this family member have a special radius where its time-coefficient vanishes" reduces to nothing more exotic than: does a simple algebraic expression, linear in $1/r$, cross zero for some positive $r$? And that is decided purely by whether the coefficient in front of $1/r$ (which is $\lambda r_s$) is negative.

## Check your understanding

- Why does the existence of a finite-radius zero depend only on the *sign* of $\lambda$, not on its magnitude?
- Why is $\lambda\ge0$ enough, by itself, to conclude "no horizon," without needing any curvature-invariant computation?
- How does $r_0$ scale with $|\lambda|$ for negative $\lambda$, and what does that say about how "close to Schwarzschild" a small negative $\lambda$'s zero sits?
- What later tutorial turns this sign condition into a statement about a measurable quantity, and what is that translation?

**Answers**
- Because $r_0=-\lambda r_s$ is only positive (i.e., a genuine radius in the physical domain $r>0$) when $-\lambda>0$; the magnitude of $\lambda$ only affects *where* the zero sits once it exists, not *whether* it exists.
- Because a horizon requires a candidate radius where $g_{tt}$ vanishes as a necessary precondition; for $\lambda\ge0$ there is no such radius at any finite $r$ at all, so there is nothing left to examine — the invariant check in `ZERO2` is only needed to adjudicate cases where a zero *does* exist.
- $r_0=-\lambda r_s$ is directly proportional to $|\lambda|$ for negative $\lambda$; smaller $|\lambda|$ pushes the zero closer to the center ($r_0\to0$), while $|\lambda|\to1$ recovers exactly Schwarzschild's $r_0=r_s$.
- `PPN7`, via the identity $\lambda=\beta-2$ derived in `PPN3`: the condition $\lambda<0$ translates directly into the observationally meaningful condition $\beta<2$.

## What the paper claims here

This tutorial grounds §3 of the paper directly. The paper states the result in essentially the same steps: "for $\lambda<0$, $1+\lambda r_s/r=0$ at $r_0=-\lambda r_s$, positive iff $\lambda<0$... For $\lambda\geq0$, positive for all finite $r>0$." It explicitly restricts its own claim to Schwarzschild for the word "horizon": "Schwarzschild $\lambda=-1$: $r_0=r_s$, the standard horizon. For other negative $\lambda$, zero at $-\lambda r_s$ but the paper does NOT classify local regularity or global causal character — refers to them only as zeros of the static time coefficient." This tutorial inherits that restraint exactly: it establishes only *where* a zero occurs and for which sign of $\lambda$, deliberately stopping short of calling any $r_0$ other than Schwarzschild's a horizon. That further step belongs to `ZERO2`.

---
**Path navigation:** ← [prev in default path](../part3-building-the-family/core-contrast.md) · [next](./zero2-when-is-a-zero-a-horizon.md) →
**See also:** [CORE2](../part3-building-the-family/core2-log-variable-closure.md), [CORE5](../part3-building-the-family/core5-distinguished-members.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [PPN7](../part6-ppn-observation/ppn7-beta-and-horizon.md)
