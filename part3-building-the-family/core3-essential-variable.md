# Solving the Closure: the Essential Variable $A^{-\lambda}$

> **Tutorial `CORE3`** · Part 3 · **Goal:** Solve $F'' = -\lambda F'$ to show the allowed potential variable is $V \propto A^{-\lambda}$ (and $V \propto \ln A$ at $\lambda = 0$), with the integration constants being mere shift and normalization. · **Prereqs:** [CORE2](./core2-log-variable-closure.md)

**Where this sits in the arc.** [CORE2](./core2-log-variable-closure.md) reduced assumption (I4) to the closed equation $\Delta s = \lambda(s')^2$ *and* to a linear ODE $F'' = -\lambda F'$ for the potential variable itself. This short tutorial solves that ODE. The payoff is a single clean object — the **essential variable** $A^{-\lambda}$ — which is what actually obeys a plain $1/r$ flux law, and which we integrate in [CORE4](./core4-classification-theorem.md) to get the family.

## The ODE and its solution ($\lambda \neq 0$)

We must solve

$$F''(s) = -\lambda\, F'(s), \qquad \lambda = \text{const}.$$

This is a constant-coefficient linear ODE, and the cleanest route is to name the derivative. Let $G(s) \equiv F'(s)$. Then the equation is first-order in $G$:

$$G'(s) = -\lambda\, G(s).$$

This is exponential decay/growth in $s$: separating, $\frac{dG}{G} = -\lambda\,ds$, so $\ln G = -\lambda s + \text{const}$, hence

$$G(s) = F'(s) = c_1\, e^{-\lambda s},$$

for some constant $c_1 \neq 0$ (nonzero because $F$ is monotonic). Integrate once more to recover $F$:

$$F(s) = \int c_1 e^{-\lambda s}\, ds = -\frac{c_1}{\lambda}\, e^{-\lambda s} + C_0 = C_0 + C_1\, e^{-\lambda s},$$

where we absorbed $-c_1/\lambda$ into a new constant $C_1$. Now translate back from $s = \ln A$ to $A$. Since $e^{-\lambda s} = e^{-\lambda \ln A} = A^{-\lambda}$,

$$\boxed{\;F(s) = C_0 + C_1\, A^{-\lambda}\;}\qquad (\lambda \neq 0).$$

## Reading the two constants: shift and normalization

The general potential variable that closes the system is $V = C_0 + C_1 A^{-\lambda}$. The two integration constants are not physics — they are the freedom to shift and rescale a potential, exactly as an electrostatic potential is defined up to an additive constant and a choice of units:

- $C_0$ is an **additive shift**: adding a constant to $V$ does not change $\Delta V = 0$, because $\Delta(\text{const}) = 0$. It just sets the zero of the potential.
- $C_1$ is an **overall normalization**: multiplying $V$ by a nonzero constant does not change the *equation* $\Delta V = 0$ either (it is linear and homogeneous). It sets the units of $V$.

Neither constant can affect $A(r)$, because both are removed the moment we impose $\Delta V = 0$ and then match to the Newtonian boundary data. What survives, the part that carries all the information, is the function it multiplies. We call

$$\boxed{\;V \propto A^{-\lambda}\;}$$

the **essential variable**: the specific function of the metric that obeys a plain, source-free, *linear* $1/r$ flux law. All the nonlinearity of the metric has been pushed into the single exponent $-\lambda$.

This is a satisfying inversion of [CORE1](./core1-flux-freedom.md). There we saw the freedom "which function of $A$ obeys the flux law" as a liability — an unremovable ambiguity. Now (I4) has converted that ambiguity into a labeled one-parameter menu: for each constant $\lambda$, the function that obeys the flux law is $A^{-\lambda}$. The representation freedom did not vanish; it got *coordinatized* by $\lambda$.

## The special case $\lambda = 0$

The solution above divided by $\lambda$, so we treat $\lambda = 0$ separately. When $\lambda = 0$ the ODE is simply

$$F''(s) = 0 \;\Longrightarrow\; F(s) = C_0 + C_1 s = C_0 + C_1 \ln A.$$

So at $\lambda = 0$ the essential variable is

$$\boxed{\;V \propto \ln A\;}\qquad (\lambda = 0),$$

which is precisely the "$V = \ln A$" choice we met by hand in [CORE1](./core1-flux-freedom.md). It is the potential variable with *no* nonlinear term at all: $\Delta s = 0 \cdot (s')^2 = 0$, i.e. $s = \ln A$ is itself harmonic.

This case is not an outlier bolted onto the family; it is its continuous center. Notice $A^{-\lambda} = e^{-\lambda \ln A} = 1 - \lambda \ln A + O(\lambda^2)$, so as $\lambda \to 0$ the essential variable $\frac{1 - A^{-\lambda}}{\lambda} \to \ln A$ smoothly. The exponent form and the logarithm form are the two faces of one continuous construction. We will see the same continuity at the level of the metric in [CORE4](./core4-classification-theorem.md), where $A_\lambda \to e^{-r_s/r}$ as $\lambda \to 0$, and again in [CORE5](./core5-distinguished-members.md), where $\lambda = 0$ is the bridge between the negative-$\lambda$ and positive-$\lambda$ members.

## Simpler on-ramp

We asked: *which function of $A$ is allowed to be the "$1/r$ potential"?* Assumption (I4) said the nonlinear coefficient $-F''/F'$ must be a fixed number $\lambda$. That is a differential equation for the function $F$, and it is one of the friendliest ones in all of calculus: "the second derivative is a constant multiple of the first." Its solutions are exponentials. Undoing the logarithm ($s = \ln A$), the exponential in $s$ becomes a **power of $A$**: the allowed potential is $A^{-\lambda}$, plus a harmless choice of zero-point and units. When $\lambda = 0$ there is no exponential at all and the allowed potential is just $\ln A$. So the entire content of (I4) is: *the thing that falls off like $1/r$ is $A^{-\lambda}$* (or $\ln A$ when $\lambda = 0$). One power, one number, and we are ready to integrate.

## Check your understanding

1. Solve $F'' = -\lambda F'$ by substituting $G = F'$. Why must $c_1 \neq 0$?
2. Show that neither $C_0$ nor $C_1$ can influence $A(r)$.
3. Why is $\lambda = 0$ handled separately, and what is the essential variable there?
4. In what sense does $A^{-\lambda}$ *coordinatize* the representation freedom of [CORE1](./core1-flux-freedom.md)?

<details>
<summary>Answers</summary>

- **1.** With $G = F'$, $G' = -\lambda G \Rightarrow G = c_1 e^{-\lambda s}$, then $F = C_0 + C_1 e^{-\lambda s} = C_0 + C_1 A^{-\lambda}$. $c_1 \neq 0$ because $F' \neq 0$ (monotonicity of the potential variable).
- **2.** $\Delta V = 0$ is linear and homogeneous, so adding $C_0$ (killed by $\Delta$) or rescaling by $C_1$ leaves the equation unchanged; imposing the flux law and matching Newtonian boundary data removes both. Only the function $A^{-\lambda}$ carries information.
- **3.** The general solution divided by $\lambda$; at $\lambda = 0$ the ODE is $F'' = 0$, giving $F = C_0 + C_1 \ln A$, so the essential variable is $\ln A$ — the no-nonlinearity member.
- **4.** The freedom "which monotonic $F(A)$ obeys the flux law" becomes, under (I4), a one-parameter list indexed by $\lambda$: for each $\lambda$ the answer is $A^{-\lambda}$. The ambiguity is now a labeled coordinate, not an open-ended choice.

</details>

## What the paper claims here

Grounds: §2.3. The paper solves $F'' = -\lambda F'$ to get, for $\lambda \neq 0$, $F(s) = C_0 + C_1 e^{-\lambda s} = C_0 + C_1 A^{-\lambda}$, states that *"constants are shift/normalization"* and that the **essential variable is $V \propto A^{-\lambda}$**; and for $\lambda = 0$, $F'' = 0 \Rightarrow F = C_0 + C_1 s$, so the essential variable is $V \propto \ln A$. Nothing beyond this is claimed here; the boundary conditions and the resulting metric family are the subject of [CORE4](./core4-classification-theorem.md).

---
**Path navigation:** ← [prev in default path](./core2-log-variable-closure.md) · [next](./core4-classification-theorem.md) →
**See also:** [CORE1](./core1-flux-freedom.md), [CORE4](./core4-classification-theorem.md), [CORE5](./core5-distinguished-members.md)
