# The invariant assembly energy: the one number that is not a convention

> **Tutorial `ACC2`** · Part 5 · **Goal:** Compute the two-shell interaction energy by a convention-free winch argument, get $E_{\rm int}=-U$ with $U\equiv Gm_1m_2/b$, and see why two shells isolate the interaction term. · **Prereqs:** [ACC1](acc1-circularity.md), [ENE1](../part1-foundations/ene1-self-energy.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)

**Where this sits in the arc.** [ACC1](acc1-circularity.md) showed that reading the field energy off the equation is circular; to constrain $\lambda$ we need an energy fixed *independently*, by a measurable work budget. This tutorial builds exactly that: a quantity that any bookkeeper computes the same way, because it is defined by the work a winch extracts. It is the fixed anchor against which the field cross-term of [ACC3](acc3-field-cross-term.md) will be compared.

## Localization is a convention; total work is not

Recall the miniature ambiguity from [ENE1](../part1-foundations/ene1-self-energy.md). In Newtonian gravity the same total energy can be written as an integral of two *different* local densities:
$$u_{\rm field} = -\frac{|\nabla\Phi|^2}{8\pi G} \qquad\text{or}\qquad u_{\rm matter} = \tfrac12\,\rho\,\Phi.$$
They agree on the *total* (integrate one, integrate by parts, use $\nabla^2\Phi=4\pi G\rho$, drop a boundary term, and you get the other) but disagree on *where the energy sits*. One puts energy throughout the field; the other puts it only where matter is. Neither is "correct" — it is a choice of accounting. In full GR the ambiguity is deeper still: gravitational energy has no unique local density at all ([ACC6](acc6-energy-localization.md)).

So *localization* is a convention. But there is a quantity immune to it: **the total work exchanged with the outside world while you build the configuration.** You can measure it at the winch. Whatever story you tell about where the energy "is," the crank turns the same number of times. This is the anchor we want.

## The two-shell thought experiment

Take two concentric thin spherical shells, masses $m_1$ and $m_2$, at areal radii $a<b$. Work in the weak field, where Newtonian gravity is the leading description. We assemble the pair in two stages and track only what crosses the boundary.

**Stage 0 — the pre-built shells, far apart.** Imagine each shell already assembled (each held rigidly at its own fixed radius and mass) but sitting at *mutual* infinite separation, so they exert no force on each other. Call this the reference configuration.

**Stage 1 — lower the outer shell.** Hold the inner shell $m_1$ fixed at radius $a$. Bring the outer shell $m_2$ in from infinity and lower it quasi-statically until it sits at radius $b$. "Quasi-statically" means arbitrarily slowly, always in near-equilibrium, so no kinetic energy is generated and no energy is radiated: every bit of work goes onto (or comes off) the winch cable.

By the **shell theorem** (see [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)), a spherical shell produces, everywhere *outside* itself, exactly the field of a point mass at its center. Throughout the lowering, the outer shell sits at radius $R\ge b>a$, so it is always entirely outside $m_1$ and feels the potential
$$\Phi_1(R) = -\frac{Gm_1}{R} \qquad (R\ge a),$$
per unit mass. The potential energy of $m_2$ in this field, as a function of where we have lowered it to, is $m_2\Phi_1(R)=-Gm_1m_2/R$. As $R$ goes from $\infty$ to $b$, gravity does positive work on the shell; because we move quasi-statically, the winch must *resist* and thereby **extract** that work:
$$W \;=\; -\big[\,m_2\Phi_1(b) - m_2\Phi_1(\infty)\,\big] \;=\; -\Big(-\frac{Gm_1m_2}{b} - 0\Big) \;=\; \frac{Gm_1m_2}{b}.$$
The winch reels up energy $W=Gm_1m_2/b$, which leaves the system.

**Energy bookkeeping.** Energy conservation for the system-plus-winch: the interaction energy now stored in the final configuration equals the reference energy (zero, by construction, for the interaction) minus what we removed:
$$E_{\rm int} \;=\; 0 - W \;=\; -\frac{Gm_1m_2}{b}.$$
Define the positive quantity
$$\boxed{\,U \equiv \frac{Gm_1m_2}{b} > 0\,}, \qquad\text{so}\qquad \boxed{\,E_{\rm int} = -U\,}.$$
The interaction energy is *negative*: the pair is bound, and you had to carry off positive energy to assemble it. This matches the general fact that gravitational binding energy is negative.

Crucially, **$-U$ is convention-independent.** We never decided where the energy lives; we only counted turns of the winch. Any localization scheme — field density, matter density, or a GR pseudotensor — must reproduce this same total, because it is the operational work budget. This is the "energy determined independently" that [ACC1](acc1-circularity.md) demanded.

## Why *two* shells, and why the self-energies drop out

A natural worry: doesn't each shell also have a *self-energy* (the energy to assemble that shell from its own dispersed dust), and don't those swamp the interaction? Here is why the two-shell setup cleanly isolates the interaction term $-U$ and nothing else.

A thin shell's self-energy depends only on its own mass and radius. In our process we move the shells *rigidly*: $m_1$ stays at radius $a$, $m_2$ stays a shell of radius $b$; we only change their *separation* (from infinite to concentric). Rigid transport does not deform either shell, so **each shell's self-energy is identical in the reference configuration and the final configuration.** When we take the difference (final minus reference), the two self-energies cancel exactly. What survives is purely the *mutual* interaction — the cross term between $m_1$'s field and $m_2$'s field. That is what the winch measured.

Contrast a single solid ball: compressing or growing it changes its self-energy, entangling "self" and "interaction" contributions and making the isolated interaction hard to read off. The two-shell configuration is chosen precisely so that the only thing that changes is the interaction, and the only thing the winch records is $-U$.

## The claim we can now make

Because the total is fixed, *any* proposed split into a matter piece and a field piece must add up to it. Writing the interaction-level (cross-term) pieces of each,
$$\boxed{\,E_{\rm matter,\,cross} + E_{\rm field,\,cross} = -U\,}. \tag{$\ast$}$$
This single equation is the lever of the whole section. In [ACC3](acc3-field-cross-term.md) we compute $E_{\rm field,\,cross}$ for the gradient-local density and find it equals $4\lambda U$ — carrying the parameter $\lambda$. Then ($\ast$) becomes a relation between $\lambda$ and whatever matter convention we adopt, which is exactly where the conditional bound $\lambda\in[-\tfrac14,\tfrac14]$ comes from ([ACC4](acc4-matter-conventions-bound.md)). The invariant is real; only the way we split it is a choice.

## Simpler on-ramp

You want to know the "cost of togetherness" of two shells — how much energy is stored purely because they are near each other, ignoring what it took to build each one. Trick: build each shell separately, out at infinity where they ignore each other, then just slide them together and *watch the winch*.

As the outer shell descends into the inner shell's gravity, gravity pulls it down and would speed it up — but you lower it on a cable, slowly, so instead of speeding up it turns a generator and hands energy back to you. The energy you collect, $Gm_1m_2/b$, is exactly the "cost of togetherness," now negative in storage: the system is that much *harder to pull back apart*. Because you built each shell first and only slid them, nothing about the shells themselves changed — so the number the winch reads is *only* the togetherness energy, clean. And it is a real, measurable number, not a matter of opinion, because you just counted the energy that came off the cable.

## Check your understanding

1. Why is $-U$ said to be "convention-independent" when the field/matter *density* is a convention?
2. Where in the derivation did the shell theorem do essential work?
3. If we had lowered a solid ball instead of a thin shell, why would isolating the interaction energy be messier?
4. What role will equation ($\ast$) play in the tutorials that follow?

<details>
<summary>Answers</summary>

- **1.** Because $-U$ is defined by the *work extracted at the winch*, an operational quantity. Different localization schemes assign the energy to different places but must all reproduce the same total exchanged with the outside world.
- **2.** It let us treat the inner shell's field, everywhere the outer shell ever sits ($R\ge b>a$), as that of a point mass $-Gm_1/R$; and it guarantees the outer shell feels no force from *inside itself*. Both facts make the potential energy simply $-Gm_1m_2/b$.
- **3.** A solid ball's self-energy changes when you compress or expand it, so moving it around entangles changes in self-energy with the interaction energy. Two rigid shells keep each self-energy fixed, so the difference is purely interaction.
- **4.** It is the fixed constraint $E_{\rm matter,cross}+E_{\rm field,cross}=-U$. Since the field cross-term will turn out to be $4\lambda U$, ($\ast$) converts the invariant into a relation between $\lambda$ and the matter convention — the source of the conditional bound.

</details>

## What the paper claims here

Grounds: **Sec. 4.2** ("Invariant assembly energy"). The paper notes localization is convention-dependent even in Newton ($-|\nabla\Phi|^2/8\pi G$ vs. $\tfrac12\rho\Phi$, up to boundary terms and the field equation) and in GR (pseudotensors, quasi-local energy), but that the *total assembly work is not ambiguous*. It sets up two concentric thin shells $m_1,m_2$ at $a<b$ in the weak field, lowers the outer shell quasi-statically from infinity to $b$ in the inner shell's field, extracts winch work $W=Gm_1m_2/b$, and concludes $E_{\rm int}=-Gm_1m_2/b\equiv -U$, "**independent of division**," so that $E_{\rm matter,cross}+E_{\rm field,cross}=-U$; the two shells isolate the interaction term because the self-energies are unchanged and cancel. What the paper does **not** claim: that this fixes $\lambda$ — the total is only *one* equation, and a further convention is needed before it constrains the parameter.

---
**Path navigation:** ← [prev: ACC1](acc1-circularity.md) · [next: ACC3](acc3-field-cross-term.md) →
**See also:** [ENE1](../part1-foundations/ene1-self-energy.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md), [ACC3](acc3-field-cross-term.md), [ACC6](acc6-energy-localization.md)
