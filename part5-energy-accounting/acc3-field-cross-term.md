# The gradient-local field cross term: doing the integral

> **Tutorial `ACC3`** · Part 5 · **Goal:** With the gradient-local field density $u_{\rm field}=\lambda\frac{c^4|\nabla s|^2}{8\pi G}$, use the shell theorem to localize the interaction to $r>b$ and integrate to get $E_{\rm field,cross}=4\lambda U$. · **Prereqs:** [ACC2](acc2-invariant-assembly-energy.md), [ACC1](acc1-circularity.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)

**Where this sits in the arc.** [ACC2](acc2-invariant-assembly-energy.md) fixed the invariant $E_{\rm matter,cross}+E_{\rm field,cross}=-U$. This tutorial computes the *field* half under one specific, natural localization convention — a density built from $|\nabla s|^2$, the same shape as the vacuum source $\lambda(s')^2$. The result $4\lambda U$ carries the parameter, so combining it with the invariant (next tutorial) turns bookkeeping into a bound on $\lambda$.

## The candidate density and superposition

Adopt the **gradient-local field energy density**
$$u_{\rm field} = \lambda\,\frac{c^4\,|\nabla s|^2}{8\pi G}.$$
This is the natural choice: it is $\lambda(s')^2$ (the vacuum source of $\Delta s$) rescaled by $c^4/8\pi G$ into an energy density, i.e. the density $u_\lambda$ of [ACC1](acc1-circularity.md) written with the full gradient. Remember the health warning from ACC1: *defining* this density does not by itself constrain $\lambda$. What breaks the circularity is comparing its integral to the independent invariant $-U$.

Work to leading (weak-field) order, where $s=2\Phi/c^2$ and potentials superpose. With two shells,
$$s = s_1 + s_2, \qquad \nabla s = \nabla s_1 + \nabla s_2,$$
so
$$|\nabla s|^2 = |\nabla s_1|^2 + |\nabla s_2|^2 + 2\,\nabla s_1\!\cdot\!\nabla s_2.$$
The first two terms are the shells' **self**-energies; they are unchanged when we move the shells and cancel in the assembly bookkeeping (exactly as in [ACC2](acc2-invariant-assembly-energy.md)). The **interaction** — the cross-term — lives entirely in
$$2\,\nabla s_1\!\cdot\!\nabla s_2.$$

## Localizing the cross term with the shell theorem

By the shell theorem, the field of a spherical shell **vanishes inside it** and equals a point-mass field **outside**. So $\nabla s_i \ne 0$ only outside shell $i$. Split space by radius (recall $a<b$):

- **$r<a$** (inside both shells): $\nabla s_1 = 0$ and $\nabla s_2 = 0$. Cross-term $=0$.
- **$a<r<b$** (outside shell 1, inside shell 2): $\nabla s_1\ne0$ but $\nabla s_2=0$. Cross-term $=0$.
- **$r>b$** (outside both shells): both gradients nonzero. Cross-term $\ne 0$.

Therefore **the cross term is supported only in $r>b$.** This is the geometric heart of the calculation: the interaction energy of the gradient-local density lives entirely in the region exterior to both shells, where their fields overlap.

## Evaluating the integrand for $r>b$

For $r>b$ each shell looks like a point mass at the origin, so
$$s_i(r) = \frac{2\Phi_i}{c^2} = \frac{2}{c^2}\left(-\frac{Gm_i}{r}\right) = -\frac{2Gm_i}{r\,c^2}.$$
The gradient is radial, $\nabla s_i = \dfrac{ds_i}{dr}\,\hat r$, and
$$\frac{ds_i}{dr} = -\frac{2Gm_i}{c^2}\frac{d}{dr}\!\left(\frac1r\right) = -\frac{2Gm_i}{c^2}\left(-\frac{1}{r^2}\right) = \frac{2Gm_i}{r^2 c^2},$$
so
$$\nabla s_i = \frac{2Gm_i}{r^2 c^2}\,\hat r.$$
Both gradients point *outward* along $\hat r$ (even though the potentials are negative, their gradients increase with $r$), so their dot product is positive:
$$\nabla s_1\!\cdot\!\nabla s_2 = \frac{2Gm_1}{r^2 c^2}\cdot\frac{2Gm_2}{r^2 c^2} = \frac{4G^2 m_1 m_2}{r^4 c^4}.$$

## The integral

Integrate the cross part of $u_{\rm field}$ over the support region $r>b$, using the flat volume element $dV=4\pi r^2\,dr$ (the proper-volume correction is $\sqrt{B}=1+O(G)$, higher order and negligible at this order):
$$
E_{\rm field,\,cross}
= \frac{\lambda c^4}{8\pi G}\int_{r>b} 2\,\nabla s_1\!\cdot\!\nabla s_2 \; dV
= \frac{\lambda c^4}{8\pi G}\int_b^\infty 2\cdot\frac{4G^2 m_1 m_2}{r^4 c^4}\cdot 4\pi r^2\,dr.
$$
Collect the constants outside the integral. The numerical factors are $2\cdot 4\cdot 4\pi = 32\pi$, and the dimensional factors are $\dfrac{\lambda c^4}{8\pi G}\cdot\dfrac{G^2 m_1 m_2}{c^4} = \dfrac{\lambda G m_1 m_2}{8\pi}$. Hence
$$
E_{\rm field,\,cross}
= \frac{\lambda G m_1 m_2}{8\pi}\cdot 32\pi \int_b^\infty \frac{r^2}{r^4}\,dr
= 4\lambda\,G m_1 m_2 \int_b^\infty \frac{dr}{r^2}.
$$
The remaining integral is elementary:
$$\int_b^\infty \frac{dr}{r^2} = \left[-\frac1r\right]_b^\infty = 0 - \left(-\frac1b\right) = \frac1b.$$
Therefore
$$
E_{\rm field,\,cross} = 4\lambda\,G m_1 m_2\cdot\frac1b = 4\lambda\,\frac{G m_1 m_2}{b},
$$
and with $U\equiv Gm_1m_2/b$,
$$\boxed{\,E_{\rm field,\,cross} = 4\lambda\,U\,}.$$

## Reading the result

Two features matter for what follows.

- **It carries $\lambda$ linearly.** The gradient-local convention assigns the field an interaction energy proportional to the very parameter we want to constrain. That is the hook: paired with the invariant $-U$, it will pin a relation between $\lambda$ and the matter convention ([ACC4](acc4-matter-conventions-bound.md)).
- **Its sign is the sign of $\lambda$.** Because the two outward gradients always align, $\nabla s_1\!\cdot\!\nabla s_2>0$, so the sign of $E_{\rm field,cross}$ is entirely the sign of $\lambda$. For Schwarzschild ($\lambda=-1$) the field cross energy is *negative* and large ($-4U$); for $\lambda=0$ it is zero (no field self-energy, consistent with [ACC1](acc1-circularity.md)); for $\lambda>0$ it is positive.

Notice already the tension the next tutorial resolves: the invariant says the *total* interaction is $-U$, but the gradient-local field alone would contribute $4\lambda U$. For Schwarzschild that is $-4U$, which *overshoots* $-U$ — so the matter piece would have to supply $+3U$. Whether that is allowed depends on what matter conventions we permit, and that is exactly the conditional bound.

## Simpler on-ramp

We already know (from [ACC2](acc2-invariant-assembly-energy.md)) the *total* togetherness energy of the two shells is $-U$. Now we ask a narrower question: if we insist the gravitational field carries an energy wherever its "strength squared" $|\nabla s|^2$ is nonzero, how much of the togetherness lands in the field?

The field-strength-squared of the two shells combined has three pieces: shell 1 alone, shell 2 alone, and a *cross* piece that exists only where *both* fields are present. By the shell theorem, a shell has no field inside it, so both fields are present only *outside the larger shell* — the region $r>b$. There, each shell looks like a point mass, its field falls off like $1/r^2$, and the cross piece like $1/r^4$. Add it up over that region (a quick $1/r^2$ integral) and you get $4\lambda U$: four times the total togetherness magnitude, scaled by $\lambda$. The factor 4 and the scaling by $\lambda$ are the whole story of the next two tutorials.

## Check your understanding

1. Why is the field cross-term supported only in $r>b$, and not in $a<r<b$?
2. The potentials are negative, yet $\nabla s_1\!\cdot\!\nabla s_2>0$. How do both hold at once?
3. Why is it legitimate to use $dV=4\pi r^2\,dr$ rather than the curved proper volume?
4. For Schwarzschild ($\lambda=-1$), what does $E_{\rm field,cross}=4\lambda U$ give, and why is that already interesting given the invariant $-U$?

<details>
<summary>Answers</summary>

- **1.** The cross-term needs *both* gradients nonzero. Inside shell 2 (which includes all of $a<r<b$) the shell theorem makes $\nabla s_2=0$, killing the product; only outside both shells ($r>b$) are both nonzero.
- **2.** The potential $s_i=-2Gm_i/(rc^2)$ is negative, but it *increases* toward zero as $r$ grows, so its gradient points outward ($+\hat r$). Both gradients point outward, so their dot product is positive.
- **3.** The correction to flat volume is $\sqrt{B}=1+O(G)$; since the integrand is already $O(G^2)$, that correction contributes at higher order in $G$ and is negligible at the order we work.
- **4.** It gives $E_{\rm field,cross}=-4U$. But the invariant total is $-U$, so the matter cross-term would have to be $+3U$ to make the books balance — a large positive matter contribution that only some conventions allow. That tension is what the bound in [ACC4](acc4-matter-conventions-bound.md) adjudicates.

</details>

## What the paper claims here

Grounds: **Sec. 4.3** ("Cross term of the gradient-local field density"). The paper takes $u_{\rm field}=\lambda\frac{c^4|\nabla s|^2}{8\pi G}$, writes $s=s_1+s_2$ so the cross term is $2\nabla s_1\cdot\nabla s_2$, uses the shell theorem to confine its support to $r>b$, evaluates $\nabla s_i=\frac{2Gm_i}{r^2c^2}\hat r$ and $\nabla s_1\cdot\nabla s_2=\frac{4G^2m_1m_2}{r^4c^4}$, and integrates with $dV=4\pi r^2 dr$ to obtain $E_{\rm field,cross}=4\lambda\frac{Gm_1m_2}{b}=4\lambda U$, noting the sign of the assigned field interaction energy equals the sign of $\lambda$. What the paper does **not** claim: that this density is *the* correct energy density — it is one convention, and the resulting bound is conditional on adopting it.

---
**Path navigation:** ← [prev: ACC2](acc2-invariant-assembly-energy.md) · [next: ACC4](acc4-matter-conventions-bound.md) →
**See also:** [ACC1](acc1-circularity.md), [ACC5](acc5-factor-of-four.md), [GAUSS1](../part1-foundations/gauss1-flux-laplacian.md)
