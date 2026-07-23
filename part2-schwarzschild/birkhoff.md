# Birkhoff's theorem

> **Tutorial `BIRK`** · Part 2 · **Goal:** State Birkhoff's theorem precisely, and show exactly why a one-parameter *family* of exteriors does not contradict it. · **Prereqs:** [S2](./s2-deriving-schwarzschild.md), [S1](./s1-vacuum-einstein.md)

**Where this sits in the arc.** This is the single most important piece of backdrop for the whole book. Part III will build a *complete one-parameter family* of static spherical exteriors — and a reader who half-remembers "Birkhoff's theorem says the vacuum spherical solution is unique" will reasonably suspect the paper has made an error. It hasn't. Understanding precisely why requires knowing exactly what Birkhoff's theorem assumes, and exactly which assumption Part III replaces. Get this tutorial solid before `CORE0`.

## The theorem, precisely

**Birkhoff's theorem.** Any spherically symmetric solution of the vacuum Einstein equations $R_{\mu\nu}=0$ is, in the region outside any matter, isometric to the Schwarzschild metric

$$ds^2 = -\left(1-\frac{r_s}{r}\right)c^2dt^2 + \left(1-\frac{r_s}{r}\right)^{-1}dr^2 + r^2 d\Omega^2$$

for some constant $r_s=2GM/c^2$. In particular the solution is automatically *static* (admits a timelike Killing vector, up to the region where $r<r_s$) — staticity does not need to be assumed; spherical symmetry plus the vacuum field equations forces it.

`S2` derived Schwarzschild under the *added* assumption of staticity, which made the algebra tractable: with $A,B$ functions of $r$ alone, $R_{\mu\nu}=0$ reduced to a short ODE system. Birkhoff's theorem is the stronger statement that this restriction cost nothing — even if you allow $A$ and $B$ to depend on time, vacuum plus spherical symmetry forces you back to the static Schwarzschild answer. For the purposes of this book, what matters most is the *narrower* corollary already visible in `S2`: **given** staticity, spherical symmetry, and $R_{\mu\nu}=0$, Schwarzschild is the *unique* solution (up to the value of $M$) — full stop, no family, no extra parameter.

## Why time-dependence doesn't help (a sketch)

It's worth seeing why staticity is automatic, since it is the part most readers take on faith. Allow the metric functions to depend on both coordinates, $ds^2 = -A(r,t)c^2dt^2 + B(r,t)dr^2 + r^2d\Omega^2$ (spherical symmetry is used up front to eliminate off-diagonal angular terms and fix the angular part to $r^2d\Omega^2$ in these "areal" coordinates). Working out the Ricci tensor for this more general ansatz, the mixed component $R_{tr}$ turns out to be proportional to $\partial B/\partial t$ divided by $r$ and $B$:

$$R_{tr} \propto \frac{1}{rB}\frac{\partial B}{\partial t}.$$

Vacuum forces $R_{tr}=0$, and since $r,B\neq0$ in the exterior, this forces $\partial B/\partial t = 0$: $B$ cannot depend on time at all. The remaining vacuum equations then reduce, exactly as in `S2`, to $(AB)'=1$-type relations at each instant of time, except now $A(r,t)$ is still allowed an arbitrary overall time-dependent rescaling, $A(r,t) = f(t)\cdot\big(1-r_s/r\big)$ for some function $f(t)$. But an overall rescaling of $A$ by $f(t)$ is exactly compensated by redefining the time coordinate, $d\tilde t = \sqrt{f(t)}\,dt$ — a coordinate relabeling, not a new physical solution. Once you make that relabeling, $A$ has no time dependence left. So spherical symmetry and $R_{\mu\nu}=0$ force staticity; nothing has to be assumed about it.

## Does this contradict a one-parameter family?

No — and the reason is worth stating with precision, because it is the sharpest way to see what the paper's construction actually is.

Birkhoff's theorem is a uniqueness theorem for one specific system of equations: $R_{\mu\nu}=0$, the vacuum Einstein field equations from `S1`. Its hypotheses are: (a) spherical symmetry, (b) vacuum — $R_{\mu\nu}=0$ — and its conclusion follows for the class of metrics satisfying both. Nothing in the theorem says anything about metrics that fail hypothesis (b).

Part III's family is built by explicitly **not imposing $R_{\mu\nu}=0$**. In its place stands postulate (I2): a monotonic potential variable $V(A)$ obeys an *exact vacuum flux law* $\Delta V = 0$, where $\Delta = \frac1{r^2}\frac{d}{dr}\!\left(r^2\frac{d}{dr}\right)$ is the ordinary flat-space radial flux operator on the areal coordinate $r$ — explicitly *not* the covariant Laplace–Beltrami operator built from the curved metric, and explicitly *not* a component of $R_{\mu\nu}$. It looks like a vacuum field equation (a Gauss-law statement, "flux through any sphere is conserved"), and it reduces to the correct leading Newtonian behavior, but it is a different equation from $R_{\mu\nu}=0$ for every choice of $V$ except one.

That one exception is exactly $\lambda=-1$: choosing $V=A$ itself makes the flux postulate $\Delta A = 0$, and working through `S2`'s algebra shows this coincides with the vacuum Einstein content for this ansatz once $AB=1$ is imposed — so the $\lambda=-1$ member of the family *is* the genuine vacuum-Einstein solution. Every other member, $\lambda\neq-1$, solves $\Delta(A^{-\lambda})=0$ instead — a different differential equation, true for a different function of $A$. Feed one of these metrics into the real $R_{\mu\nu}$ and it will not vanish: the "exterior" quietly carries a nonzero effective stress–energy, even though nothing in the paper's four postulates ever mentioned matter. (This is the companion negative-space fact to this one — see `CORE-CONTRAST` and `GRSOL`.)

So there is no contradiction because Birkhoff's theorem and the paper's classification theorem (`CORE4`) are uniqueness statements for *two different systems of equations*. Birkhoff answers "what solves $R_{\mu\nu}=0$, given spherical symmetry?" — answer: Schwarzschild, uniquely. The paper answers "what solves $\Delta V(A)=0$ for *some* monotonic $V$, given (I1), (I3), (I4)?" — answer: the whole family $A_\lambda$, of which Schwarzschild is one member. Both theorems can be true, and are, simultaneously, because they are theorems about different hypotheses.

## Naming the dropped hypothesis

If you want one sentence that pins down exactly what happens: **the paper's construction evades Birkhoff's theorem by dropping and replacing its vacuum-field-equation hypothesis.** Not spherical symmetry — the paper keeps that (it's built into the ansatz from the start). Not asymptotic flatness — kept. Not even staticity, really — kept as an assumption in both places (Birkhoff proves it is unnecessary to *assume*; the paper's ansatz assumes it directly, same as `S2`). The one hypothesis of Birkhoff's theorem that is missing from the paper's four postulates (I1)–(I4) is "$R_{\mu\nu}=0$" itself — the actual Einstein field equations — replaced by the strictly weaker, coordinate-dependent flux postulate (I2). A weaker hypothesis has a larger solution set; that is not a paradox, it is what "weaker" means.

## Simpler on-ramp

Imagine a uniqueness theorem in a different setting: "any function $f$ satisfying $f'' = 0$ and $f(0)=0, f(1)=1$ is the straight line $f(x)=x$ — uniquely." That's true and easy to prove. Now suppose someone builds a *family* of functions satisfying instead $f''=\lambda (f')^2$ with the same boundary conditions, for a free constant $\lambda$, and shows the family includes the straight line as one member ($\lambda=0$) among infinitely many curved options. Is the first uniqueness theorem "wrong"? No — the family solves a different, weaker equation that only *coincides* with $f''=0$ at $\lambda=0$. Birkhoff and the paper's family stand in exactly this relation: same boundary behavior at infinity, same symmetry, but a different differential law in the interior, and it's precisely the swapped law that opens the door to more than one answer.

## Check your understanding

- Which of Birkhoff's hypotheses does the paper's construction keep, and which does it drop?
- Why is it not a contradiction that $R_{\mu\nu}=0$ has a unique spherical vacuum solution while $\Delta V(A)=0$ has a whole family of them?
- Why does only $\lambda=-1$ among the family members actually satisfy the real vacuum Einstein equations?
- Birkhoff's theorem shows staticity is a *consequence* of spherical symmetry plus vacuum, not an extra assumption. Does the paper's construction get staticity for free the same way?

**Answers**
- Kept: spherical symmetry, asymptotic flatness, staticity (assumed directly, not derived). Dropped and replaced: the vacuum Einstein field equations $R_{\mu\nu}=0$, swapped for the weaker flux postulate (I2).
- Because they are uniqueness theorems for two different equations. $\Delta V(A)=0$ is not $R_{\mu\nu}=0$ except in the one special case where $V=A$; a weaker constraint simply admits more solutions, which is expected, not paradoxical.
- Because choosing $V=A$ (the $\lambda=-1$ closure) makes the flux postulate reduce, after imposing $AB=1$, to the same condition that `S2` derives directly from $R_{\theta\theta}=0$ — the one point where the postulated flux law and the true field equation happen to agree.
- No. The paper simply *assumes* staticity as part of the ansatz (as `S2` also does); it never proves staticity is forced, because it never uses the vacuum Einstein equations at all — that particular derivation (from `S1`'s and `S2`'s tools) isn't available to a construction that has replaced $R_{\mu\nu}=0$ with (I2).

## What the paper claims here

Birkhoff's theorem is not discussed explicitly in the paper's text, but it is the sharpest available diagnostic for what the paper's whole construction is: this tutorial supplies the exact reasoning that the paper's own restraint requires. The paper is careful to call (I2) "a postulate, not a covariant field equation and not a consequence of the Einstein equations" (§2, discussing I2) — language that is exactly the dropped-hypothesis point made precise here. The paper's own scope discipline (§1, §8) — "(I1)–(I4) build the family but don't select $\lambda=-1$," "unique" always means "unique within this family" — is the surface expression of the same fact this tutorial names directly: Birkhoff's uniqueness theorem for $R_{\mu\nu}=0$ is simply not in force once (I2) has replaced the field equations it would otherwise need to invoke.

---
**Path navigation:** ← [prev in default path](./s2-deriving-schwarzschild.md) · [next](./s3-properties.md) →
**See also:** [S1](./s1-vacuum-einstein.md), [S2](./s2-deriving-schwarzschild.md), [CORE4](../part3-building-the-family/core4-classification-theorem.md), [CORE-CONTRAST](../part3-building-the-family/core-contrast.md), [GRSOL](../part5-energy-accounting/grsol-are-these-gr-solutions.md)
