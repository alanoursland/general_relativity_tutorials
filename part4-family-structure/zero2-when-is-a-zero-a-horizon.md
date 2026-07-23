# When is a zero a horizon?

> **Tutorial `ZERO2`** · Part 4 · **Goal:** Establish, with full rigor, that a vanishing $g_{tt}$ is necessary but not sufficient for a horizon — and apply that restraint honestly to the $\lambda$-family. · **Prereqs:** [ZERO1](./zero1-finite-radius-zeros.md), [S4](../part2-schwarzschild/s4-singularities.md)

**Where this sits in the arc.** `ZERO1` found *where* $A_\lambda$ vanishes and for which sign of $\lambda$. This tutorial asks the harder question the paper deliberately leaves open for every member except Schwarzschild: is that zero actually a horizon, in the full physical sense — a smooth, geodesically traversable null surface — or could it be a genuine curvature singularity, or something the construction simply hasn't told us enough to classify? This is exactly the discipline the book commits to never violating: never call a zero of $g_{tt}$ a horizon without the invariant check.

## Necessary, not sufficient

`S4` established the criterion in the one case we can fully verify: at Schwarzschild's $r_s$, the Kretschmann scalar $K(r_s)=48G^2M^2/(c^4r_s^6)$ is finite, and regular coordinates (Painlevé–Gullstrand, `PG1`; Eddington–Finkelstein) extend smoothly across it — so $r_s$ is a coordinate artifact marking a genuine, physically unremarkable horizon, not a place where the geometry itself breaks down.

Nothing about *that* argument follows automatically from the mere fact $A(r_0)=0$. Vanishing $g_{tt}$ tells you only that a particular coordinate component of a particular representation of the metric happens to be zero at $r_0$ — exactly the kind of representation-dependent statement `F2` and `S4` warn against over-reading. To promote "$A_\lambda(r_0)=0$" to "there is a horizon at $r_0$," you need independent evidence of at least two further things:

1. **Local regularity** — a coordinate-independent curvature invariant (Kretschmann or otherwise) stays finite at $r_0$, and a regular chart exists there, the way `S4` verified explicitly for Schwarzschild.
2. **Global causal structure** — the surface at $r_0$ actually behaves as a one-way membrane for light and matter (an honest event horizon), not, say, a naked singularity, a throat connecting to another region, or some other causal structure that a bare zero of $g_{tt}$ is equally compatible with.

A finite-radius zero is therefore a *necessary* condition for a horizon (`ZERO1` already used this direction: no zero at all, as for $\lambda\ge0$, is sufficient on its own to rule a horizon out) but it is not *sufficient*: finding a zero only opens the question, it does not close it.

## What can actually be said about $\lambda\neq-1$ members

For $\lambda<0$, $\lambda\neq-1$, `ZERO1` located a zero at $r_0=-\lambda r_s$. What is its status? Here the honest answer is that the construction in `CORE0`–`CORE4` simply does not supply enough information to say. Recall the reason (`BIRK`, negative-space fact 1): only the $\lambda=-1$ member is Ricci-flat — a genuine solution of $R_{\mu\nu}=0$. Every other member solves the postulated flux law $\Delta(A^{-\lambda})=0$ instead, which is not a covariant field equation at all (`BIRK`), and feeding $A_\lambda$ with $\lambda\neq-1$ into the real Einstein tensor produces a nonzero $G_{\mu\nu}$ — an effective stress–energy that the construction never specified anything about. Nothing in (I1)–(I4) constrains that effective source's energy conditions, its behavior near $r_0$, or whether it is even physically reasonable. Classifying $r_0$ for these members is therefore not a matter of finishing an easy computation the paper skipped for space — it requires committing to a specific interpretation of what the "vacuum" flux postulate implies about curvature there, which the four postulates simply don't supply.

This is why the correct, restrained statement is: **for $\lambda\neq-1$, $A_\lambda$ has a zero of the metric time-coefficient at $r_0=-\lambda r_s$; whether that zero is a horizon, a curvature singularity, or something else is not established by (I1)–(I4) and is not classified here.** Anything stronger would be an overclaim the construction does not support.

## Beyond the paper: what would it take to find out?

*Beyond the paper:* the paper deliberately brackets this question (negative-space fact 5 — geodesic completeness, energy conditions, and the causal character of the $r_0$ surfaces for $\lambda\neq-1$ are explicitly left open). It is worth being precise about *why* this is hard, rather than treating it as a mere omission.

To settle it for a specific $\lambda$, you would need to compute a genuine curvature invariant — Kretschmann or otherwise — for the metric $A_\lambda,B_\lambda=A_\lambda^{-1}$ and evaluate it at $r_0$. Two structural facts make this a real (not automatic) computation, and caution against guessing the answer by analogy with Schwarzschild:

- $B_\lambda=A_\lambda^{-1}$ diverges at $r_0$ exactly as Schwarzschild's $B$ diverges at $r_s$ — so the same *kind* of coordinate blow-up is present for every member. That alone tells you nothing about curvature; it only reproduces the situation `S4` had to look past for Schwarzschild.
- But curvature invariants are built from derivatives of $A_\lambda$ and $B_\lambda$, and those derivatives depend on $\lambda$ in a way that does not obviously mirror Schwarzschild's cancellation. Schwarzschild's finiteness at $r_s$ is not a generic feature of "having $B=1/A$ with a zero of $A$" — it is a specific fact about the particular function $A=1-r_s/r$, tied to it being the genuine vacuum solution. There is no available argument, from the four postulates alone, that this finiteness survives for $A^{-\lambda}$ with $\lambda\neq-1$.

So the honest position is: it is a well-posed, answerable question for each specific $\lambda$, but answering it requires curvature-tensor work the paper's four postulates do not perform and do not license inferring by analogy. This tutorial stops exactly where the paper stops — flagging the question precisely rather than resolving it by extrapolation.

## The contrast this sets up

Framed against `ZERO1`: that tutorial showed the sign of $\lambda$ is a fact you can read off from elementary algebra on $A_\lambda$ alone. *This* tutorial shows that "is it a horizon" is not that kind of question — it requires the heavier machinery of `F7`/`S4` (curvature invariants) applied member-by-member, and for the family's construction as given, that work has not been done and cannot be shortcut. The only member for which the full answer is actually known is Schwarzschild itself, precisely because it alone is *also* a solution of the real field equations (`BIRK`), which is where the entire supporting apparatus of standard GR — geodesic completeness theorems, energy conditions, the Penrose singularity theorems — becomes available to invoke.

## Simpler on-ramp

Suppose you're told a function crosses zero at some point, and you're asked whether that crossing point is a "smooth dip through zero" (like $\sin x$ at $x=\pi$) or a place where the function is actually undefined or badly behaved (like $1/x$ blowing up as $x\to0$, or a genuine kink). Just knowing "it equals zero here" doesn't tell you which — you have to look at more than the one data point; you have to check the behavior around it with tools that don't care how you've labeled the axis. That is exactly what "vanishing $g_{tt}$" versus "genuine horizon" comes down to. Schwarzschild is the one case in this book where we've actually done that extra check (`S4`) and gotten a clean answer: it's a smooth crossing. For every other family member with a zero, nobody in this construction has done the check yet — so the honest answer is "we don't know," not "probably yes" or "probably no."

## Check your understanding

- Why is "$A_\lambda(r_0)=0$" not, by itself, enough to justify calling $r_0$ a horizon?
- What two things would you need to verify to promote a bare zero to a genuine horizon?
- Why can't Schwarzschild's finiteness of $K$ at $r_s$ be assumed to carry over automatically to other $\lambda$'s zero at $r_0=-\lambda r_s$?
- Why does the paper's restraint here differ for $\lambda=-1$ versus every other negative $\lambda$?

**Answers**
- Because vanishing $g_{tt}$ is a statement about one component of the metric in one coordinate system — a necessary condition for a horizon, as established in `ZERO1`'s discussion of $\lambda\ge0$, but not sufficient; it says nothing yet about whether curvature invariants stay finite there or about the global causal structure.
- Local regularity (a coordinate-independent curvature invariant stays finite there, and a regular coordinate chart exists across it) and global causal structure (the surface genuinely behaves as a one-way membrane, as opposed to a singularity, throat, or other structure).
- Because Schwarzschild's finiteness is a specific fact about the function $A=1-r_s/r$ tied to its being the actual vacuum-Einstein solution (`BIRK`), not a generic consequence of "$B=1/A$ has a pole where $A$ has a zero"; other members solve a different equation entirely and their derivatives near $r_0$ need not reproduce the same cancellation.
- Because Schwarzschild alone is Ricci-flat (`BIRK`), which brings the full toolkit of standard GR — geodesic completeness results, energy conditions, singularity theorems — to bear on it; the other members solve only the postulated flux law, which carries no such guarantees, so their $r_0$ surfaces remain genuinely unclassified by this construction.

## What the paper claims here

This tutorial grounds §3's explicit caveat and negative-space fact 5. The paper states plainly: "Schwarzschild $\lambda=-1$: $r_0=r_s$, the standard horizon. For other negative $\lambda$, zero at $-\lambda r_s$ but the paper does NOT classify local regularity or global causal character of the corresponding surfaces — refers to them only as zeros of the static time coefficient." The paper's own scope discipline is explicit that "$\lambda$ controls both first nonlinear correction AND existence of a zero; [its physical character is] left undetermined." This tutorial does not go further than that caveat permits: the "Beyond the paper" section above explains *why* the question is hard rather than supplying an answer the paper itself withholds, which is the correct way to extend a scrupulously scoped result without violating its restraint.

---
**Path navigation:** ← [prev in default path](./zero1-finite-radius-zeros.md) · [next](../part5-energy-accounting/acc0-the-question.md) →
**See also:** [F7](../part1-foundations/f7-curvature.md), [S4](../part2-schwarzschild/s4-singularities.md), [BIRK](../part2-schwarzschild/birkhoff.md)
