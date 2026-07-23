# Integration and the Classification Theorem

> **Tutorial `CORE4`** · Part 3 · **Goal:** Integrate $\Delta(A^{-\lambda}) = 0$ with the boundary conditions to obtain $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$, handle the $\lambda\to 0$ exponential limit, and state precisely what the classification theorem does and does not claim. · **Prereqs:** [CORE3](./core3-essential-variable.md), [CORE0](./core0-four-assumptions.md)

**Where this sits in the arc.** This is the destination of the "build" half of the book: the four assumptions, made precise in [CORE0](./core0-four-assumptions.md)–[CORE3](./core3-essential-variable.md), produce a **complete one-parameter family**. After this, every remaining part of the book is about *selecting* a member. The theorem we state here is the exact statement the rest of the book leans on — including its careful scope words, which we will honor everywhere.

## Integrating the essential variable

From [CORE3](./core3-essential-variable.md), the essential variable $W \equiv A^{-\lambda}$ obeys the plain linear flux law $\Delta W = 0$. This is the same equation we already solved in [CORE1](./core1-flux-freedom.md): $\Delta W = 0$ forces $r^2 W'$ constant, so

$$\frac{d}{dr}(r^2 W') = 0 \;\Rightarrow\; r^2 W' = C_1 \;\Rightarrow\; W' = \frac{C_1}{r^2} \;\Rightarrow\; W(r) = C_0 + \frac{C_1}{r}.$$

So $A^{-\lambda} = C_0 + C_1/r$. Two constants, fixed by two pieces of boundary data.

**Asymptotic flatness** fixes $C_0$. As $r \to \infty$, $A \to 1$, hence $A^{-\lambda} \to 1$. From $W = C_0 + C_1/r$ we get $W(\infty) = C_0$, so

$$C_0 = 1.$$

**The Newtonian limit (I1)** fixes $C_1$. We know $A = 1 - r_s/r + O(r^{-2})$. Raise to the power $-\lambda$ and expand with the binomial series $(1+u)^{-\lambda} = 1 - \lambda u + O(u^2)$, here with $u = -r_s/r$:

$$A^{-\lambda} = \left(1 - \frac{r_s}{r}\right)^{-\lambda} = 1 + \lambda\frac{r_s}{r} + O(r^{-2}).$$

Match to $W = 1 + C_1/r$: the $1/r$ coefficients must agree, so

$$C_1 = \lambda\, r_s.$$

Therefore $A^{-\lambda} = 1 + \lambda r_s/r$, and solving for $A$:

$$\boxed{\;A_\lambda(r) = \left(1 + \lambda\,\frac{r_s}{r}\right)^{-1/\lambda}, \qquad B_\lambda = A_\lambda^{-1}, \qquad r_s = \frac{2GM}{c^2}.\;}$$

This is the family. One number $\lambda$ selects a member; $r_s$ (hence $M$) sets the scale.

## The $\lambda = 0$ member as a continuous limit

At $\lambda = 0$ the exponent $-1/\lambda$ is undefined, so we treat it two ways and check they agree.

**Directly.** At $\lambda = 0$ the closure is $\Delta s = 0$ with $s = \ln A$ ([CORE3](./core3-essential-variable.md)). So $s$ obeys the plain flux law: $s = c_0 + c_1/r$. Asymptotic flatness ($s\to 0$) gives $c_0 = 0$; the Newtonian value $s = -r_s/r + \dots$ gives $c_1 = -r_s$. Hence $s = -r_s/r$ exactly, and

$$A_0(r) = e^{-r_s/r}.$$

**As a limit.** Take the logarithm of the general member and let $\lambda \to 0$:

$$\ln A_\lambda = -\frac{1}{\lambda}\ln\!\left(1 + \lambda\frac{r_s}{r}\right) = -\frac{1}{\lambda}\left(\lambda\frac{r_s}{r} - \frac{1}{2}\lambda^2\frac{r_s^2}{r^2} + \dots\right) = -\frac{r_s}{r} + \frac{\lambda}{2}\frac{r_s^2}{r^2} - \dots$$

As $\lambda \to 0$ this tends to $-r_s/r$, so $A_\lambda \to e^{-r_s/r} = A_0$. The two routes agree: **the family is continuous through $\lambda = 0$**, and we adopt $A_0 = e^{-r_s/r}$ as the member there by continuity. There is no seam.

## The classification theorem

We can now state the result cleanly, in both directions.

**Classification theorem.** *Consider a connected, static, spherically symmetric, asymptotically flat exterior on the branch $A > 0$, in areal coordinates, satisfying (I1)–(I4). Then the closure reduces to $\Delta s = \lambda(s')^2$ for a single constant $\lambda$, and the metric is a member of the one-parameter family*

$$A_\lambda(r) = \left(1 + \lambda\frac{r_s}{r}\right)^{-1/\lambda}, \quad B_\lambda = A_\lambda^{-1},$$

*with $A_0 = e^{-r_s/r}$ understood by continuity. Conversely, every constant-$\lambda$ member of this family satisfies (I1)–(I4).*

The forward direction is what we built across [CORE0](./core0-four-assumptions.md)–[CORE3](./core3-essential-variable.md): the assumptions *force* this form. The converse is a quick check — plug $A_\lambda$ back in and verify (I1) (Newtonian leading term), (I2) (the essential variable $A^{-\lambda} = 1 + \lambda r_s/r$ is manifestly affine in $1/r$, so $\Delta(A^{-\lambda}) = 0$), (I3) ($B = 1/A$ by definition), and (I4) ($\lambda$ is a constant). Both directions together mean the assumptions and the family are *equivalent*: the family is exactly the solution set.

## Reading the scope words exactly

The theorem's power is entirely in its precision, so we state what its words mean and — just as important — what they do not.

- **"Complete"** means: *relative to (I1)–(I4)*, there are **no other** solutions. Every metric meeting the four assumptions is some $A_\lambda$. It does **not** mean complete relative to general relativity; the members with $\lambda \neq -1$ are *not* vacuum-Einstein solutions (that is [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md)).
- **"Unique within this family"** is the phrase we use later when a selector picks $\lambda = -1$. It means: unique *given* that we already accept (I1)–(I4). It never means "the unique static spherical exterior" — Birkhoff's theorem gives *that* uniqueness, but only after imposing the full Einstein equations, a stronger hypothesis (see [BIRK](../part2-schwarzschild/birkhoff.md) and [CORE-CONTRAST](./core-contrast.md)).
- **The assumptions do not determine $\lambda$.** This is the crux restated as a theorem: (I1)–(I4) build the whole family but leave $\lambda$ free. Any specific value of $\lambda$ — including the physically correct $\lambda = -1$ — requires **additional input**: energy accounting (Part 5, which fails to select it), PPN observation (Part 6, which succeeds: $\lambda = \beta - 2$), or the Painlevé–Gullstrand infall condition (Part 7).

So the honest summary of the build is: *four physically reasonable-sounding shortcuts do not derive Schwarzschild — they derive a continuum of metrics that all look Newtonian from far away, with Schwarzschild sitting at $\lambda = -1$ and nothing yet distinguishing it.*

## Simpler on-ramp

We had reduced everything to one clean statement: *the quantity $A^{-\lambda}$ falls off like a simple $1/r$ field.* Falling off like $1/r$ means $A^{-\lambda} = 1 + (\text{something})/r$. Two facts fix the pieces: far away $A = 1$, which forces the constant to be exactly $1$; and near-Newtonian behavior forces the $1/r$ coefficient to be $\lambda r_s$. So $A^{-\lambda} = 1 + \lambda r_s/r$, and taking the $-1/\lambda$ power gives the metric member

$$A_\lambda = \left(1 + \lambda\frac{r_s}{r}\right)^{-1/\lambda}.$$

When $\lambda = 0$ the power is ill-defined, but the curve does not misbehave — it smoothly becomes $e^{-r_s/r}$, which you can see by taking a logarithm and letting $\lambda\to 0$. The one-sentence takeaway: the four assumptions do not give *a* metric, they give a dial. Turning the dial to $\lambda = -1$ gives Schwarzschild, but the assumptions never tell you to turn it there.

## Check your understanding

1. Carry out the two boundary matches and get $C_0 = 1$, $C_1 = \lambda r_s$. Which assumption supplies each?
2. Show two independent ways that $A_0 = e^{-r_s/r}$, and explain why "by continuity" is legitimate.
3. State precisely what "complete" and "unique within this family" mean. What does neither word claim?
4. Does the theorem determine $\lambda$? What kinds of input can?

<details>
<summary>Answers</summary>

- **1.** $A^{-\lambda} = C_0 + C_1/r$. Asymptotic flatness ($A\to1$) gives $C_0 = 1$; the Newtonian limit (I1) via $(1-r_s/r)^{-\lambda} = 1 + \lambda r_s/r + \dots$ gives $C_1 = \lambda r_s$.
- **2.** Directly: at $\lambda=0$, $\Delta s = 0 \Rightarrow s = -r_s/r \Rightarrow A_0 = e^{-r_s/r}$. As a limit: $\ln A_\lambda = -\frac1\lambda\ln(1+\lambda r_s/r) \to -r_s/r$. Both give the same function and the family is continuous, so the $\lambda=0$ member is unambiguous.
- **3.** "Complete" = no solutions of (I1)–(I4) outside the family. "Unique within this family" = unique once (I1)–(I4) are granted. Neither claims uniqueness relative to full GR, nor that $\lambda\neq-1$ members solve $G_{\mu\nu}=0$.
- **4.** No — (I1)–(I4) leave $\lambda$ free. Selecting a value needs additional input: energy-accounting conventions (Part 5), the PPN relation $\lambda = \beta-2$ measured by e.g. Mercury (Part 6), or the exact Newtonian infall condition in PG coordinates (Part 7).

</details>

## What the paper claims here

Grounds: §2.4. The paper integrates $\Delta(A^{-\lambda}) = 0$ to $A^{-\lambda} = C_0 + C_1/r$, sets $C_0 = 1$ (asymptotic flatness) and $C_1 = \lambda r_s$ (Newtonian limit), obtaining $A_\lambda = (1+\lambda r_s/r)^{-1/\lambda}$ with $B_\lambda = A_\lambda^{-1}$, and $A_0 = e^{-r_s/r}$ both directly and as $\lim_{\lambda\to0}$. It states the **classification theorem** in both directions and stresses the scope: *"complete relative to these assumptions; they do NOT determine $\lambda$."* Schwarzschild is the member $\lambda = -1$. The paper deliberately does **not** assert these are GR solutions or that any member other than $\lambda=-1$ is physically vetted — those questions are bracketed and taken up later.

---
**Path navigation:** ← [prev in default path](./core3-essential-variable.md) · [next](./weak1-weak-field-degeneracy.md) →
**See also:** [BIRK](../part2-schwarzschild/birkhoff.md), [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md), [CORE-CONTRAST](./core-contrast.md)
