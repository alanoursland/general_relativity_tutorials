# The Log Variable and the Closure ODE

> **Tutorial `CORE2`** · Part 3 · **Goal:** Introduce $s=\ln A$, derive the chain-rule identity $\Delta V = F'\Delta s + F''(s')^2$ in full, and show that (I4) turns the flux law into $\Delta s = \lambda(s')^2$ with $\lambda = -F''/F'$ a *constant of the closure*. · **Prereqs:** [CORE1](./core1-flux-freedom.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)

**Where this sits in the arc.** [CORE1](./core1-flux-freedom.md) exposed the freedom: the flux law does not fix which $V(A)$ falls off like $1/r$. Here we cash out assumption (I4), the closure that tames that freedom into a single number. The key reveal at the end — that $\lambda$ is a property of the *chosen closure*, not of the geometry — is the same lesson as crux 1, now in a form we can integrate.

## Why the logarithm is the right variable

We want one metric variable in which to write everything, so that the freedom of [CORE1](./core1-flux-freedom.md) shows up as a single visible coefficient. The logarithm

$$s \equiv \ln A, \qquad A = e^{s}, \qquad B = \frac{1}{A} = e^{-s}$$

is the natural choice for three reasons. First, by (I3) the *entire* metric is now a function of the single field $s$: $A = e^s$, $B = e^{-s}$, and the angular part is fixed. Second, $s$ is additive for superposed weak sources (potentials add; and to leading order $s \approx 2\Phi/c^2$, see below), which is exactly what makes the later two-shell energy bookkeeping clean. Third — the technical payoff — writing the flux law in $s$ turns the "which function $V(A)$" freedom into a single number multiplying a squared gradient.

The weak-field value of $s$ follows from (I1). Write $A = 1 + \epsilon$ with $\epsilon$ small; then $s = \ln(1+\epsilon) = \epsilon + O(\epsilon^2)$. Since $A = 1 + 2\Phi/c^2 + \dots = 1 - r_s/r + \dots$, we get $\epsilon = 2\Phi/c^2 + \dots = -r_s/r + \dots$, so

$$s = \frac{2\Phi}{c^2} + \dots = -\frac{r_s}{r} + \dots \qquad (\text{weak field}).$$

## The chain-rule identity, derived in full

The flux law of (I2) says some monotonic potential variable $V = F(s)$ (a fixed function $F$ of $s$) satisfies $\Delta V = 0$. We need $\Delta V$ in terms of $s$. Recall that acting on a radial function the flux operator is

$$\Delta V = \frac{1}{r^2}\frac{d}{dr}\!\left(r^2 \frac{dV}{dr}\right) = V'' + \frac{2}{r}V',$$

where $' = d/dr$. (The second form comes from expanding the product: $\frac{1}{r^2}(r^2 V')' = \frac{1}{r^2}(2r V' + r^2 V'') = V'' + \frac2r V'$.)

Now $V = F(s(r))$. Differentiate with the chain rule:

$$V' = F'(s)\,s',$$

$$V'' = \frac{d}{dr}\big(F'(s)\,s'\big) = F''(s)\,(s')^2 + F'(s)\,s''.$$

Assemble $\Delta V = V'' + \frac2r V'$:

$$\Delta V = F''(s)(s')^2 + F'(s)\,s'' + \frac{2}{r}F'(s)\,s' = F''(s)(s')^2 + F'(s)\left(s'' + \frac{2}{r}s'\right).$$

The parenthesis is exactly $\Delta s$. Hence the **chain-rule identity**:

$$\boxed{\;\Delta V = F'(s)\,\Delta s + F''(s)\,(s')^2\;}$$

This is the engine of the whole construction. It splits the flux operator acting on the *potential variable* into a linear piece (the flux operator acting on $s$) plus a nonlinear piece (a squared gradient of $s$). Read it slowly: the *only* place nonlinearity can enter is the $F''(s')^2$ term, and its size is governed entirely by $F''$, a property of the closure function $F$.

## Imposing the flux law: the effective coefficient

The flux law is $\Delta V = 0$. Set the left side to zero and divide by $F'$, which is nonzero because $V(A)$ (equivalently $F(s)$) is monotonic:

$$0 = F'\,\Delta s + F''(s')^2 \;\Longrightarrow\; \Delta s = -\frac{F''(s)}{F'(s)}\,(s')^2.$$

Define the **effective nonlinear coefficient**

$$\lambda(s) \equiv -\frac{F''(s)}{F'(s)}.$$

So *any* monotonic potential variable $F(s)$ turns the flux law into $\Delta s = \lambda(s)\,(s')^2$ — a nonlinear equation for $s$, with a coefficient $\lambda(s)$ that in general varies with the field. This is [CORE1](./core1-flux-freedom.md)'s freedom made quantitative: different choices of $F$ give different functions $\lambda(s)$, hence different metrics.

## What (I4) buys: a constant, and a linear ODE for $F$

Assumption (I4) is precisely the statement that this coefficient is a **constant of the theory**, not a function of local field strength:

$$\lambda(s) = \lambda = \text{const} \quad\Longleftrightarrow\quad -\frac{F''}{F'} = \lambda \quad\Longleftrightarrow\quad \boxed{\,F'' = -\lambda F'\,}.$$

Two things happen at once. On the *metric* side, the flux law collapses to a clean closed equation for $s$:

$$\boxed{\;\Delta s = \lambda\,(s')^2\;}, \qquad \Delta s = s'' + \frac{2}{r}\,s'.$$

On the *closure* side, $F'' = -\lambda F'$ is a constant-coefficient linear ODE that pins down which potential variable is allowed, up to two integration constants. Solving it (next tutorial, [CORE3](./core3-essential-variable.md)) gives $V \propto A^{-\lambda}$, and integrating $\Delta s = \lambda(s')^2$ (in [CORE4](./core4-classification-theorem.md)) gives the family $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$.

## The key reveal: $\lambda$ belongs to the closure, not the geometry

Here is the point to carry forward. In $\Delta s = \lambda(s')^2$, the term $(s')^2$ is tempting to read as an *energy density* of the gravitational field — the field's own gradient sourcing more field, "gravity gravitating." If that reading were forced, $\lambda$ would be a fact about how strongly gravity self-couples, i.e. a fact about *nature*.

It is not forced. We derived $\lambda = -F''/F'$ purely from the **choice of potential variable $F(s)$** in which we chose to write the flux law. Nothing physical selected $F$; [CORE1](./core1-flux-freedom.md) showed every monotonic $F$ is equally legal. So at this stage $\lambda$ is a bookkeeping constant recording *which representation we closed the system in* — a property of the closure, not of the spacetime. Only under the *additional* assumptions of the energy-accounting section (Part 5) can $(s')^2$ be promoted to a genuine energy density and $\lambda$ read as a self-energy weight — and even then the promotion is convention-bound, as [ACC1](../part5-energy-accounting/acc1-circularity.md) shows. This is the same warning as crux 1, and it is the seed of the book's throughline; see [EPI1](../part8-synthesis/epi1-representation-vs-fact.md).

## Simpler on-ramp

Forget metrics; think of a change of variables. You have a flux law that wants *some* quantity $V$ to be "harmonic" (to obey $\Delta V = 0$). You decide to express $V$ as a function $F$ of a more convenient variable $s = \ln A$. When you push $\Delta$ through the substitution, calculus hands you two pieces:

$$\Delta V = \underbrace{F'\,\Delta s}_{\text{linear}} + \underbrace{F''\,(s')^2}_{\text{nonlinear}}.$$

The first piece is "$s$ obeys the same kind of law"; the second is a correction whose strength is set by the curvature $F''$ of the relabeling function. Demanding $\Delta V = 0$ then says $s$ obeys a law with a *nonlinear* term whose coefficient is $-F''/F'$. Assumption (I4) is just "make that coefficient one fixed number $\lambda$." That single demand both fixes the shape of the relabeling ($F''=-\lambda F'$) and hands us a tidy equation $\Delta s = \lambda(s')^2$ to solve. The number $\lambda$ came from *how we chose to relabel*, which is why we keep insisting it is not (yet) a fact about gravity.

## Check your understanding

1. Reproduce $\Delta V = F'\Delta s + F''(s')^2$ from $V = F(s(r))$, stating where each term comes from.
2. Why are we allowed to divide by $F'$?
3. What does (I4) forbid, exactly — and what does it still permit (name the special value)?
4. Why is it *wrong*, at this stage, to call $\lambda$ the strength of gravitational self-coupling?

<details>
<summary>Answers</summary>

- **1.** $V' = F' s'$; $V'' = F''(s')^2 + F' s''$; then $\Delta V = V'' + \frac2r V' = F''(s')^2 + F'(s'' + \frac2r s') = F'\Delta s + F''(s')^2$. The nonlinear term is the $(s')^2$ from differentiating $F'(s)$; the linear term repackages $s''+\frac2r s' = \Delta s$.
- **2.** $V(A)$ is required monotonic in (I2), so $F'(s)\neq 0$ everywhere.
- **3.** It forbids $\lambda$ from being a function $\lambda(s)$ of local field strength; it requires a single constant. It still permits $\lambda = 0$ (no nonlinearity — the flux law holds exactly for $\ln A$).
- **4.** Because $\lambda = -F''/F'$ was determined by the *choice of potential variable* $F$, which the physical assumptions never fixed. Reading $(s')^2$ as energy density is an extra, convention-dependent step (Part 5), not something the flux law entails.

</details>

## What the paper claims here

Grounds: §2.2 and §2.3. The paper defines $s = \ln A$ (so $A = e^s$, $B = e^{-s}$), derives $\Delta V = F'(s)\Delta s + F''(s)(s')^2$, divides by $F'$ to get $\Delta s = -\frac{F''}{F'}(s')^2$, defines the effective coefficient $\lambda(s) = -F''/F'$, and imposes (I4) as $\lambda = \text{const}$, yielding both $F'' = -\lambda F'$ and the boxed closure $\Delta s = \lambda(s')^2$. The paper explicitly cautions that *"interpreting $(s')^2$ as energy density requires the choices"* of the later energy-accounting section — i.e. $\lambda$ is, here, a coefficient of the closure, not yet a physical self-energy weight.

---
**Path navigation:** ← [prev in default path](./core1-flux-freedom.md) · [next](./core3-essential-variable.md) →
**See also:** [CORE3](./core3-essential-variable.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md), [ACC1](../part5-energy-accounting/acc1-circularity.md)
