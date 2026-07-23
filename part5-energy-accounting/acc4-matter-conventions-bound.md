# Matter conventions and the conditional bound

> **Tutorial `ACC4`** · Part 5 · **Goal:** Combine the invariant $-U$ with the field cross-term $4\lambda U$ under a family of matter conventions to get $\lambda=\frac{2f-1}{4}$, hence $\lambda\in[-\tfrac14,\tfrac14]$ — and see honestly that $0\le f\le1$ is an *assumption*, not a theorem. · **Prereqs:** [ACC3](acc3-field-cross-term.md), [ACC2](acc2-invariant-assembly-energy.md), [ACC1](acc1-circularity.md)

**Where this sits in the arc.** This is where energy accounting produces its actual output — an interval $[-\tfrac14,\tfrac14]$ that *excludes* Schwarzschild's $\lambda=-1$ — and where crux 3 of the book bites: the total energy is invariant, but the interval is only as strong as a modeling choice about how to split it. Getting the theorem's *conditionality* exactly right is the point; the interval is less important than the fine print.

## The one equation, two unknowns

From [ACC2](acc2-invariant-assembly-energy.md) the invariant interaction energy is $-U$; from [ACC3](acc3-field-cross-term.md) the gradient-local field carries $E_{\rm field,cross}=4\lambda U$. The invariant demands the pieces sum to the total:
$$E_{\rm matter,\,cross} + 4\lambda U = -U. \tag{$\ast$}$$
One equation, two unknowns ($\lambda$ and $E_{\rm matter,cross}$). To solve for $\lambda$ we must say how much interaction energy the *matter* ledger carries — and that is a **convention**, a choice of how to count a mass's energy when it sits in a potential. We consider two natural endpoints and then interpolate.

## Convention A — local rest energy ($f=0$)

Count each shell's energy as its **local rest energy** $\rho c^2$, with no correction for sitting in the other's potential. Then the matter ledger records *no* interaction energy:
$$E_{\rm matter,\,cross} = 0.$$
The field must carry the whole interaction. Plug into ($\ast$):
$$0 + 4\lambda U = -U \quad\Longrightarrow\quad 4\lambda = -1 \quad\Longrightarrow\quad \boxed{\lambda = -\tfrac14}.$$

## Convention B — asymptotic (redshift) energy ($f=1$)

Count each shell's energy as **measured from infinity**, i.e. including the gravitational redshift correction from the other shell's potential. Shell 1 in shell 2's potential contributes $m_1\Phi_2=-Gm_1m_2/b=-U$; shell 2 in shell 1's potential contributes $m_2\Phi_1=-U$. Summing *once per matter element* gives
$$E_{\rm matter,\,cross} = -2U.$$
A word of care: the *physical* mutual interaction is $-U$, not $-2U$ — this convention **double-enters** the interaction, charging it once to each mass. That is a legitimate bookkeeping choice provided the field piece compensates, which it does. Plug into ($\ast$):
$$-2U + 4\lambda U = -U \quad\Longrightarrow\quad 4\lambda = 1 \quad\Longrightarrow\quad \boxed{\lambda = +\tfrac14}.$$
Check the ledger: matter $-2U$ plus field $4(\tfrac14)U=+U$ gives $-U$, the invariant. Balanced.

## Interpolating: the interval

Parametrize the whole convex family between these endpoints by a single dial $f$:
$$E_{\rm matter,\,cross} = -2f\,U, \qquad f=0\ \text{(local)},\quad f=1\ \text{(asymptotic)}.$$
Substitute into ($\ast$):
$$-2f\,U + 4\lambda U = -U \quad\Longrightarrow\quad -2f + 4\lambda = -1 \quad\Longrightarrow\quad 4\lambda = 2f-1,$$
$$\boxed{\;\lambda = \frac{2f-1}{4}\;}.$$
As $f$ runs over the convex interval $[0,1]$:
$$0\le f\le 1 \quad\Longrightarrow\quad \boxed{-\tfrac14 \le \lambda \le \tfrac14}.$$
The midpoint $f=\tfrac12$ gives $\lambda=0$, the linear (exponential) member. So under *any* mixture of the local and asymptotic matter conventions, the gradient-local accounting confines $\lambda$ to $[-\tfrac14,\tfrac14]$ — and **Schwarzschild's $\lambda=-1$ is not in it.**

## Where Schwarzschild lands, and why the invariant can't exclude it

Set $\lambda=-1$ and solve for the required dial:
$$-1 = \frac{2f-1}{4} \quad\Longrightarrow\quad 2f-1 = -4 \quad\Longrightarrow\quad f = -\tfrac32.$$
Schwarzschild demands $f=-\tfrac32$, i.e.
$$E_{\rm matter,\,cross} = -2fU = +3U, \qquad E_{\rm field,\,cross} = 4\lambda U = -4U, \qquad \text{total} = +3U-4U = -U.$$
The total is still exactly the invariant $-U$ — **nothing is violated.** Schwarzschild is excluded from the interval not because it breaks the energy budget, but because $f=-\tfrac32$ lies *outside* the convex range $[0,1]$ we chose to allow. The invariant $-U$ constrains only the *sum*; it says nothing about whether a given decomposition has $f\in[0,1]$. Schwarzschild simply splits the (correct, invariant) total differently than the adopted convention permits: a large positive matter interaction ($+3U$) canceling a large negative field interaction ($-4U$).

## The honest caveat — crux 3

Here is the disciplined reading, the one an author-level understanding requires.

> **The restriction $0\le f\le1$ is part of the theorem's *assumptions*, not one of its *conclusions*.** The invariant assembly energy fixes the total at $-U$; it does **not** prove that every physically admissible matter–field decomposition has its dial in $[0,1]$. "$0\le f\le1$" is a modeling choice — a stipulation that the matter energy be counted somewhere between its purely local value and its purely asymptotic value. It is reasonable, but it is a *choice*, and Schwarzschild's $f=-\tfrac32$ shows a member can sit outside it while keeping the total perfectly correct.

So the bound $\lambda\in[-\tfrac14,\tfrac14]$ is **conditional**, and it inherits *all* of its exclusionary power from the convention, not from any invariant. Hold the two facts in one hand at once, the way you would hold a gauge-dependent quantity next to a gauge-invariant one:

- **Invariant / real:** the total interaction energy is $-U$, in every member and every convention.
- **Convention / gauge-like:** the split into matter and field, hence the value of $f$, hence the interval $[-\tfrac14,\tfrac14]$ and the exclusion of Schwarzschild.

This is why energy accounting is the selector that *fails*: it does not actually forbid $\lambda=-1$; it forbids $\lambda=-1$ *relative to a bookkeeping stipulation* that $\lambda=-1$ happens to violate. And, as Part 6 will show, observation places $\lambda$ at $-1$ — which means the real lesson is that the stipulation $0\le f\le1$ is *false of nature*, not that Schwarzschild is.

## The conditional theorem, stated cleanly

Collecting the hypotheses so the scope is unmistakable:

> **Conditional static-accounting bound (paper §4.5).** Assume
> (1) the one-parameter family of §2 with constant coefficient $\lambda$;
> (2) the gradient-local field density $u_{\rm field}=\lambda\frac{c^4|\nabla s|^2}{8\pi G}$;
> (3) a matter convention $E_{\rm matter,cross}=-2fU$ with $0\le f\le1$;
> (4) the invariant assembly energy $E_{\rm int}=-U$.
> Then $\lambda=\frac{2f-1}{4}$ and $-\tfrac14\le\lambda\le\tfrac14$, so Schwarzschild ($\lambda=-1$) is excluded. The result concerns the *split* of the energy, not energy conservation.

Every clause is load-bearing. Drop (2) for a different localization and the field cross-term changes; drop (3)'s range and the exclusion vanishes; (4) is the only genuinely invariant input.

## Simpler on-ramp

We know the two shells' total "togetherness energy" is exactly $-U$ (a hard fact). We also chose to say the field carries $4\lambda U$. Subtract: the matter must carry the rest, $-U-4\lambda U$. So the field share and the matter share trade off along a single dial.

Now, *how* should we count the matter's share? Two honest bookkeepers disagree. One says "count each mass by its plain local weight, so matter carries no togetherness energy" — that forces $\lambda=-\tfrac14$. The other says "count each mass by its energy as seen from far away, including how the other mass reddens its clocks" — that forces $\lambda=+\tfrac14$. Every bookkeeper in between lands $\lambda$ somewhere in $[-\tfrac14,\tfrac14]$.

Schwarzschild ($\lambda=-1$) would need a bookkeeper who does something stranger: charge the matter a *large positive* togetherness energy ($+3U$) and the field an even larger negative one ($-4U$). The two still sum to the correct $-U$ — so Schwarzschild doesn't break any law of energy. It just refuses to be booked by any of the "reasonable" bookkeepers we allowed. The bound excludes it only because we drew the circle of "reasonable" too small — and nature, it turns out, lives outside that circle.

## Check your understanding

1. Under the local convention, why does *all* the interaction energy fall on the field, and what value of $\lambda$ does that force?
2. The asymptotic convention gives $E_{\rm matter,cross}=-2U$, but the physical mutual energy is $-U$. Why is the factor-of-two not a contradiction?
3. Schwarzschild needs $f=-\tfrac32$. In what precise sense is it "excluded," and in what sense is it *not*?
4. Why is it correct to call the bound $[-\tfrac14,\tfrac14]$ *conditional* rather than a theorem about gravity?

<details>
<summary>Answers</summary>

- **1.** The local convention counts matter by its bare rest energy with no potential correction, so $E_{\rm matter,cross}=0$; the invariant $-U$ must then be entirely the field's, giving $4\lambda U=-U$, i.e. $\lambda=-\tfrac14$.
- **2.** It is a bookkeeping double-entry: the asymptotic convention charges the mutual interaction once to each of the two masses, giving $-2U$ in the matter ledger, which the field ledger ($+U$) compensates so the invariant total stays $-U$. The *physical* interaction is still $-U$.
- **3.** It is excluded from the interval because $f=-\tfrac32$ falls outside the *assumed* range $0\le f\le1$. It is **not** excluded by the invariant: with $E_{\rm matter,cross}=+3U$ and $E_{\rm field,cross}=-4U$ the total is exactly $-U$, so no conservation law is broken.
- **4.** Because its only exclusionary power comes from the stipulation $0\le f\le1$, a modeling choice, not from any invariant. The invariant fixes only the total; change the admissible conventions and the interval changes. So it constrains our bookkeeping, not gravity itself.

</details>

## What the paper claims here

Grounds: **Sec. 4.4–4.5**. The paper derives $E_{\rm matter,cross}+4\lambda U=-U$; the local convention ($E_{\rm matter,cross}=0$) giving $\lambda=-\tfrac14$; the asymptotic convention ($E_{\rm matter,cross}=-2U$, explicitly flagged as a double-entry "once per matter element, not a physical $-2U$") giving $\lambda=+\tfrac14$; the interpolation $E_{\rm matter,cross}=-2fU$ giving $\lambda=\frac{2f-1}{4}$ and $\lambda\in[-\tfrac14,\tfrac14]$ for $0\le f\le1$; and Schwarzschild needing $f=-\tfrac32$ ($E_{\rm matter,cross}=+3U$, $E_{\rm field,cross}=-4U$, total still $-U$). It states plainly that "**the restriction $0\le f\le1$ must be recognized as part of the theorem's assumptions**" — the invariant budget fixes $-U$ but does not prove every decomposition lies in this interval — and that the bound "concerns the split, not energy conservation." What the paper does **not** claim: that Schwarzschild is physically excluded by energy — only that it falls outside the adopted convention.

---
**Path navigation:** ← [prev: ACC3](acc3-field-cross-term.md) · [next: ACC5](acc5-factor-of-four.md) →
**See also:** [ACC2](acc2-invariant-assembly-energy.md), [ACC6](acc6-energy-localization.md), [PPN5](../part6-ppn-observation/ppn5-perihelion-precession.md)
