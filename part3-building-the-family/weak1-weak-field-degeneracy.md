# Weak-Field Degeneracy

> **Tutorial `WEAK1`** · Part 3 · **Goal:** Derive $A_\lambda = 1 - x + \frac{1+\lambda}{2}x^2 + O(x^3)$, show the members first differ at $O(x^2)$, note that Schwarzschild's quadratic coefficient vanishes (a coordinate statement), and describe the family-curve figure. · **Prereqs:** [CORE4](./core4-classification-theorem.md)

**Where this sits in the arc.** We have the family $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$. Now we ask the observational question that governs everything in Parts 6–7: *how far in do you have to probe before two members visibly differ?* The answer — they are identical at Newtonian order and first split at second order in $x = r_s/r$ — is why the family survived undetected for a century, and it foreshadows the PPN parameters $\gamma$ and $\beta$.

## The weak-field expansion, derived in full

Write $x \equiv r_s/r$ and expand $A_\lambda = (1 + \lambda x)^{-1/\lambda}$ for small $x$. The exponent $-1/\lambda$ makes a raw binomial expansion awkward, so we go through the logarithm — a method that also makes the $\lambda\to0$ limit transparent.

Take the log and use $\ln(1+u) = u - \tfrac12 u^2 + \tfrac13 u^3 - \dots$ with $u = \lambda x$:

$$\ln A_\lambda = -\frac{1}{\lambda}\ln(1+\lambda x) = -\frac{1}{\lambda}\left(\lambda x - \frac{\lambda^2 x^2}{2} + \frac{\lambda^3 x^3}{3} - \dots\right) = -x + \frac{\lambda}{2}x^2 - \frac{\lambda^2}{3}x^3 + \dots$$

Note the $1/\lambda$ has cancelled, so the expansion is regular at $\lambda = 0$. Now exponentiate, $A_\lambda = e^{\ln A_\lambda}$, using $e^{y} = 1 + y + \tfrac12 y^2 + \dots$ with $y = -x + \frac{\lambda}{2}x^2 + \dots$. Keep terms through $x^2$:

$$y = -x + \frac{\lambda}{2}x^2 + O(x^3), \qquad y^2 = x^2 + O(x^3),$$

$$A_\lambda = 1 + \left(-x + \frac{\lambda}{2}x^2\right) + \frac{1}{2}\left(x^2\right) + O(x^3) = 1 - x + \frac{\lambda}{2}x^2 + \frac{1}{2}x^2 + O(x^3).$$

Collecting the $x^2$ terms:

$$\boxed{\;A_\lambda(r) = 1 - x + \frac{1+\lambda}{2}\,x^2 + O(x^3), \qquad x = \frac{r_s}{r}.\;}$$

(As a sanity check, the exponential member $\lambda = 0$ gives $A_0 = e^{-x} = 1 - x + \tfrac12 x^2 - \dots$, matching coefficient $\tfrac12 = (1+0)/2$; the reciprocal $\lambda = +1$ gives $(1+x)^{-1} = 1 - x + x^2 - \dots$, matching $(1+1)/2 = 1$; Schwarzschild $\lambda = -1$ gives $1 - x$ with coefficient $(1-1)/2 = 0$.)

## What the expansion says

**First-order term is $\lambda$-independent.** Every member has $A_\lambda = 1 - x + \dots$, i.e. the same $-x = -r_s/r$ leading correction. This is just (I1) reappearing: the Newtonian limit was *imposed*, so all members share it identically. Consequently **no leading-order observation can determine $\lambda$**: the leading gravitational redshift, the Newtonian orbit, the mass — all fixed by the $-x$ term, hence blind to which member you are in.

**Members first differ at $O(x^2)$**, with coefficient $\frac{1+\lambda}{2}$. This is the earliest place the parameter shows up. The differences are genuine (different curvature, different strong-field fate) but *quadratically suppressed*: at $r = 10\,r_s$, $x^2 = 0.01$, and the fractional split between two members is of that order. This suppression is exactly why the family hid in plain sight — the classical tests that see $O(x)$ physics cannot feel it, and only a test sensitive to the $O(x^2)$ time–time structure can. That test is perihelion precession, and the parameter it reads is the post-Newtonian $\beta$, tied to our $\lambda$ by $\beta = \lambda + 2$ (Part 6). The quadratic coefficient here, $\frac{1+\lambda}{2}$, is the same object that will become $a_2 = \frac{1+\lambda}{2}$ in the PPN transformation.

**Schwarzschild's quadratic coefficient vanishes — but that is a coordinate statement.** At $\lambda = -1$ the coefficient $\frac{1+\lambda}{2} = 0$, and in fact $A_{-1} = 1 - x$ *exactly*: the expansion terminates at first order. It is tempting to read this as "Schwarzschild is the simplest / least nonlinear member." Resist that reading. The termination is a property of $g_{tt}$ *in areal coordinates*, not an invariant. Schwarzschild is richly curved and strongly nonlinear; the exact $1 - r_s/r$ is an artifact of writing it in this particular coordinate and metric variable. In isotropic coordinates the same spacetime has an infinite series in the potential. The lesson — a running theme, see [EPI1](../part8-synthesis/epi1-representation-vs-fact.md) — is that "the series stops" is a fact about the representation, whereas "the members differ at second order" (a statement about *differences* that survives coordinate matching, cf. the PPN $\beta$) is closer to physical.

## Members do not first diverge *beyond* first post-Newtonian order

A subtle point the paper is careful about. Saying members "first differ at $O(x^2)$" might suggest they agree out to high post-Newtonian order and only split deep in the strong field. Not so: $O(x^2)$ *is* the first post-Newtonian (1PN) order. The members are degenerate only at Newtonian (0PN) order and split as early as 1PN. That is precisely why a 1PN-sensitive measurement — Mercury's precession — can distinguish them, rather than requiring strong-field data.

## Describing Figure 1 (the family curves)

The paper's Figure 1 plots $A_\lambda(r)$ against $r$ for a spread of values, e.g. $\lambda \in \{-1, -\tfrac14, 0, +1\}$. Picture it as follows.

- All curves start at $A = 1$ far to the right ($r \to \infty$) and **fan out only as $r$ decreases**, since they share the same initial slope $-r_s/r$. Near the right edge they are visually indistinguishable — the Newtonian degeneracy made graphical.
- The **negative-$\lambda$ curves bend down and cross zero** at a finite radius. From $A_\lambda = 0 \iff 1 + \lambda r_s/r = 0 \iff r = -\lambda r_s$: the Schwarzschild curve ($\lambda = -1$) hits $A = 0$ at $r = r_s$; the $\lambda = -\tfrac14$ curve hits it at $r = r_s/4$. These are the finite-radius zeros of Part 4.
- The **$\lambda \geq 0$ curves stay strictly positive** for all finite $r > 0$: the exponential $A_0 = e^{-r_s/r}$ approaches zero only as $r \to 0$ but never reaches it at finite $r$, and the $\lambda > 0$ members have base $1 + \lambda r_s/r > 0$ throughout. No horizon-type zero for these members.

So one figure encodes two morals at once: the *degeneracy* (curves indistinguishable far out) and the *sign switch* (only $\lambda < 0$ produces a finite-radius zero) that Part 4 develops.

## Simpler on-ramp

Every member of the family looks *exactly* the same from far away, because we forced them all to match Newton there. The first place they can possibly differ is the next term in the expansion — the $x^2 = (r_s/r)^2$ term — and there the coefficient is $\frac{1+\lambda}{2}$, which does depend on $\lambda$. So:

- Far out, $x$ is tiny and $x^2$ is *tiny-squared*: the differences are invisible to any measurement that only feels the leading pull. This is why nobody noticed a whole family lurking behind Schwarzschild.
- The special member $\lambda = -1$ (Schwarzschild, in these coordinates) has that $x^2$ coefficient equal to zero — its time coefficient is just $1 - r_s/r$ with nothing after it. That looks magically simple, but it is a trick of the coordinates, not a deep truth; write the same spacetime differently and the simplicity disappears.

The takeaway: to tell the members apart you need an experiment that reaches the $x^2$ level of precision. That is perihelion precession, and it is what finally fingers Schwarzschild.

## Check your understanding

1. Reproduce $A_\lambda = 1 - x + \frac{1+\lambda}{2}x^2 + O(x^3)$ via the log–exp route. Why does the $1/\lambda$ cancel?
2. Why can no leading-order (Newtonian) measurement determine $\lambda$?
3. Schwarzschild's expansion stops at first order. Why is that *not* an invariant statement about simplicity?
4. From the figure, which members reach $A = 0$ at finite radius, and where?

<details>
<summary>Answers</summary>

- **1.** $\ln A_\lambda = -\frac1\lambda\ln(1+\lambda x) = -x + \frac\lambda2 x^2 - \dots$ (the $\frac1\lambda$ cancels against the leading $\lambda x$ inside the log, leaving a series regular at $\lambda=0$); exponentiating gives $1 - x + \frac{1+\lambda}2 x^2 + \dots$.
- **2.** All members share the imposed Newtonian term $-x$; they agree identically at $O(x)$, so anything sensitive only to that order is blind to $\lambda$.
- **3.** Termination of $g_{tt} = 1 - r_s/r$ is a property of the areal coordinate/metric variable, not a coordinate-invariant. In isotropic coordinates the same solution is an infinite series; Schwarzschild is not "less nonlinear" in any invariant sense.
- **4.** Only $\lambda < 0$ members: $A_\lambda = 0$ at $r = -\lambda r_s$ (Schwarzschild at $r_s$, $\lambda=-\tfrac14$ at $r_s/4$). The $\lambda \geq 0$ members stay positive for all finite $r>0$.

</details>

## What the paper claims here

Grounds: §2.6 and Figure 1. The paper gives $A_\lambda = 1 - x + \frac{1+\lambda}{2}x^2 + O(x^3)$, notes the first-order term $-x$ is $\lambda$-independent, that members first differ at $O(x^2)$ with coefficient $(1+\lambda)/2$ vanishing for $\lambda = -1$, and explicitly flags that *"Schwarzschild's expansion terminating at first order is a coordinate-dependent statement."* It states that leading redshift cannot determine $\lambda$, that (I3) gives $\gamma = 1$ so light bending and radar delay do not distinguish members, that the freedom appears in $\beta$, and that **members do not first diverge beyond 1PN**. Figure 1: $A_\lambda$ for $\lambda \in \{-1,-\tfrac14,0,+1\}$; negative-$\lambda$ curves reach $A=0$ at $r = -\lambda r_s$; $\lambda \geq 0$ stay positive.

---
**Path navigation:** ← [prev in default path](./core4-classification-theorem.md) · [next](./core5-distinguished-members.md) →
**See also:** [PPN3](../part6-ppn-observation/ppn3-gamma-beta.md), [ZERO1](../part4-family-structure/zero1-finite-radius-zeros.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md)
