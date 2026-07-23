# Perihelion Precession & the Numbers

> **Tutorial `PPN5`** · Part 6 · **Goal:** Derive the $(2-\lambda)/3$ precession factor and reproduce the family's precession table, then show the Sec. 4 accounting interval is falsified by Mercury · **Prereqs:** [PPN4](./ppn4-classical-tests.md)

**Where this sits in the arc.** This is where the two selectors of the book actually collide. Part V's accounting bound, $\lambda\in[-\tfrac14,\tfrac14]$, was the best a convention-bound energy argument could do, and it excluded Schwarzschild. This tutorial shows precisely what that interval predicts for Mercury's perihelion — and that Mercury's observed precession rules it out. Observation, not accounting, gets to keep Schwarzschild.

## From $(2+2\gamma-\beta)/3$ to $(2-\lambda)/3$

`PPN4` quoted the standard PPN result that the perihelion precession per orbit, relative to the GR value, is rescaled by
$$\frac{2+2\gamma-\beta}{3}.$$
`PPN3` established $\gamma=1$ for every member of the family, so this becomes
$$\frac{2+2(1)-\beta}{3} = \frac{4-\beta}{3}.$$
Now substitute the family's identity $\beta=\lambda+2$:
$$\frac{4-(\lambda+2)}{3} = \boxed{\frac{2-\lambda}{3}}.$$
This is the factor by which a member's predicted precession differs from GR's. At $\lambda=-1$ (Schwarzschild) the factor is $(2-(-1))/3 = 1$: no rescaling, exactly the GR value — as it must be, since Schwarzschild's $\beta=1$ is GR's own value.

## Reproducing the table

Taking $43.0''$/century as the GR (Schwarzschild) value of Mercury's anomalous perihelion precession, each member's predicted precession is $43.0''\times\frac{2-\lambda}{3}$:

| $\lambda$ | $\beta=\lambda+2$ | factor $\frac{2-\lambda}{3}$ | precession (''/century) |
|---|---|---|---|
| $-1$ | $1$ | $1$ | $43.0$ |
| $-1/2$ | $3/2$ | $5/6$ | $35.8$ |
| $-1/4$ | $7/4$ | $3/4$ | $32.3$ |
| $0$ | $2$ | $2/3$ | $28.7$ |
| $+1/4$ | $9/4$ | $7/12$ | $25.1$ |
| $+1/2$ | $5/2$ | $1/2$ | $21.5$ |
| $+1$ | $3$ | $1/3$ | $14.3$ |

Working two of these explicitly: at $\lambda=-\tfrac12$, factor $=\tfrac{2-(-1/2)}{3}=\tfrac{5/2}{3}=\tfrac56$, and $43.0\times\tfrac56 = 35.83\ldots\approx35.8$. At $\lambda=+1$, factor $=\tfrac{2-1}{3}=\tfrac13$, and $43.0\times\tfrac13=14.33\ldots\approx14.3$. Every other row is the same one-line arithmetic: multiply $43.0$ by $(2-\lambda)/3$.

Two features of the table matter. First, the factor is *monotonically decreasing* in $\lambda$ — larger $\lambda$ predicts a *smaller* precession than GR, and the predictions fan out roughly threefold across the range shown ($43.0''$ down to $14.3''$), a spread far larger than any realistic observational uncertainty on Mercury's precession. Second, Shuler's two extra members sit exactly at $\lambda=\pm\tfrac12$ in this table, predicting $35.8''$ and $21.5''$ respectively — both clearly and individually distinguishable from $43.0''$ given the precision of modern Mercury orbit data.

## The Sec. 4 interval is falsified

Part V's accounting theorem (`ACC4`) constrained $\lambda\in[-\tfrac14,\tfrac14]$ under its stated matter-convention assumptions, corresponding to $\beta\in[\tfrac74,\tfrac94]$. Reading the table at its two endpoints: $\lambda=-\tfrac14$ predicts $32.3''$/century, and $\lambda=+\tfrac14$ predicts $25.1''$/century. So the *entire* accounting-allowed interval predicts a perihelion precession somewhere in roughly $25''$–$32''$ per century — nowhere near the observed value of approximately $43''$/century. Since Mercury's precession is measured far more precisely than the roughly $8''$ spread of this range, the entire Sec. 4 interval is observationally excluded, not merely disfavored. This is the sharp version of the tension flagged in `ACC4`: the interval that follows from a seemingly reasonable (if convention-bound) energy-accounting argument does not contain the value nature actually exhibits. Schwarzschild ($\lambda=-1$), which the accounting argument places *outside* its allowed interval entirely (needing an $f=-\tfrac32$ that falls outside the assumed convex range $[0,1]$; see `ACC4`), is exactly the value the perihelion data select.

## Simpler on-ramp

Every member of the family makes the *same* prediction for how much light bends and how long radar echoes are delayed (`PPN4`) — but they make *different* predictions for how much an elliptical orbit's long axis slowly rotates over centuries, and the rotations differ enough to be told apart with existing measurement precision. Plugging in the interval that a plausible-looking energy-accounting argument (Part V) allowed produces predictions clustered around $25''$–$32''$ per century; nature's answer is close to $43''$ per century. It's as if a theoretical argument, built from what looked like reasonable bookkeeping principles, confidently pointed to the wrong answer, while a comparatively simple orbital observation pointed to the right one. The lesson is not that energy accounting was wrong about *conservation* — the total assembly energy really is $-U$, unambiguously — but that turning a conserved total into a claim about $\lambda$ required an extra convention that, it turns out, nature does not respect.

## Check your understanding

- Why does $(2+2\gamma-\beta)/3$ collapse to a function of $\lambda$ alone for this family?
- Why is the factor equal to $1$ specifically at $\lambda=-1$, and is that a coincidence?
- What does it mean, precisely, for the Sec. 4 interval to be "falsified" rather than merely "not confirmed"?
- Why can Shuler's two extra members ($\lambda=\pm\tfrac12$) be observationally distinguished from Schwarzschild using only this one test?

**Answers**
- Because $\gamma=1$ is fixed (not a free parameter) for every member of the family, the only freedom left in $(2+2\gamma-\beta)/3$ is $\beta$, and $\beta=\lambda+2$ turns that residual freedom directly into a function of $\lambda$.
- Not a coincidence: $\lambda=-1$ is precisely the Schwarzschild member, whose $\beta=1$ is by definition GR's own predicted value, so the "rescaling relative to GR" must come out to exactly $1$ there — the table is built to reproduce GR at that one point.
- "Not confirmed" would mean the data simply hadn't been precise enough to rule the interval in or out; "falsified" means the interval's entire predicted range ($\approx25''$–$32''$) lies outside the measured value ($\approx43''$) by far more than the measurement's uncertainty, so every value in the interval is individually excluded, not merely unconfirmed.
- Because their predicted precessions ($35.8''$ and $21.5''$) both differ from the observed $\approx43''$ by amounts much larger than Mercury's orbital precession is known to that precision — one test, applied to a sufficiently precise orbit, is already enough to exclude both alternatives.

## What the paper claims here

Grounded in Sec. 5.3: the factor $(2+2\gamma-\beta)/3=(2-\lambda)/3$ and the reproduced table using $43.0''$/century as the GR value, explicitly stating "all non-Schwarzschild members incompatible with observed Mercury precession," and "Sec 4 interval $[-1/4,1/4]\to\beta\in[7/4,9/4]\to\approx25''$–$32''$, not $\approx43''$." The paper does not re-derive the $(2+2\gamma-\beta)/3$ formula from orbital mechanics — it is used as a standard, citable PPN result — and this tutorial follows that same scope, deriving only the algebraic collapse to $(2-\lambda)/3$ and the arithmetic of the table, not the underlying orbital-mechanics derivation of the precession formula itself.

---
**Path navigation:** ← [prev in default path](./ppn4-classical-tests.md) · [next](./ppn6-reading-constraints.md) →
**See also:** [ACC4](../part5-energy-accounting/acc4-matter-conventions-bound.md), [ACC5](../part5-energy-accounting/acc5-factor-of-four.md), [PPN3](./ppn3-gamma-beta.md)
