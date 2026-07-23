# The factor of four: what Schwarzschild's field density does and doesn't mean

> **Tutorial `ACC5`** · Part 5 · **Goal:** Show that for Schwarzschild the gradient-local field density is *four times* the Newtonian one, $u_{-1}=4u_N$, and pin down exactly what that localization statement does and does not assert. · **Prereqs:** [ACC4](acc4-matter-conventions-bound.md), [ACC3](acc3-field-cross-term.md), [ENE1](../part1-foundations/ene1-self-energy.md)

**Where this sits in the arc.** A corollary of the accounting, and a trap for the unwary. Schwarzschild's gradient-local field energy density comes out four times the textbook Newtonian value — a striking number that is *purely a localization statement*. The invariant total is still $-U$. Getting this distinction right is the same discipline as crux 3: a convention-dependent density is not an observable.

## The computation

Take the gradient-local density from [ACC3](acc3-field-cross-term.md) at the Schwarzschild value $\lambda=-1$:
$$u_{-1} = \lambda\,\frac{c^4|\nabla s|^2}{8\pi G}\bigg|_{\lambda=-1} = -\frac{c^4|\nabla s|^2}{8\pi G}.$$
In the weak field $s=2\Phi/c^2$, so
$$\nabla s = \frac{2}{c^2}\nabla\Phi, \qquad |\nabla s|^2 = \frac{4}{c^4}\,|\nabla\Phi|^2.$$
Substitute:
$$u_{-1} = -\frac{c^4}{8\pi G}\cdot\frac{4|\nabla\Phi|^2}{c^4} = -\frac{4\,|\nabla\Phi|^2}{8\pi G}.$$
Compare the **Newtonian** gradient energy density (see [ENE1](../part1-foundations/ene1-self-energy.md)):
$$u_N = -\frac{|\nabla\Phi|^2}{8\pi G}.$$
Therefore
$$\boxed{\,u_{-1} = 4\,u_N\,}.$$
Schwarzschild's gradient-local field energy density is four times the standard Newtonian one, everywhere, in the weak field. This is the same factor 4 that produced $E_{\rm field,cross}=4\lambda U=-4U$ in [ACC3](acc3-field-cross-term.md): the Newtonian density integrates to $-U$ for the two-shell interaction, and quadrupling the density quadruples the integral to $-4U$.

## What it does mean

It is a **localization statement** about the $\lambda=-1$ member under the gradient-local convention. If you insist on assigning the gravitational field an energy density built from $|\nabla s|^2$, then Schwarzschild's nonlinearity forces that density to be four times the naive Newtonian $-|\nabla\Phi|^2/8\pi G$. Equivalently: the coefficient of the squared gradient, for Schwarzschild, differs from the textbook Newtonian one by a factor of 4 in magnitude. Schwarzschild's self-coupling is not "the standard Newtonian field density counted once."

Consistency check with the ledger of [ACC4](acc4-matter-conventions-bound.md): with the field carrying $E_{\rm field,cross}=-4U$, the invariant $-U$ requires the matter ledger to carry
$$E_{\rm matter,\,cross} = -U - (-4U) = +3U,$$
which is exactly the $f=-\tfrac32$ decomposition Schwarzschild needs. The factor of four and the "$+3U$ of matter" are the same fact seen from the two sides of the ledger.

## What it does not mean

It is tempting — and wrong — to read "$u_{-1}=4u_N$" as "Schwarzschild's binding energy is four times the Newtonian binding energy." It is not. The observable, convention-free quantity is the **total** interaction energy, and that is
$$E_{\rm int} = -U$$
in *every* member and *every* convention, Schwarzschild included. Nothing measurable is quadrupled. What is quadrupled is a piece of a *convention-dependent* split: the amount the gradient-local scheme chooses to store in the field. That extra $-3U$ in the field is precisely canceled by the $+3U$ the same scheme must then assign to matter. The books balance at $-U$; the factor of 4 lives entirely inside the bookkeeping.

So the factor of four is not a physical amplification. It is the numerical signature of the fact — established in [ACC4](acc4-matter-conventions-bound.md) — that Schwarzschild splits the (invariant, correct) total energy in a way that lies *outside* the "reasonable" matter conventions $0\le f\le1$. It sorts a large negative field contribution against a large positive matter contribution. That is a statement about localization, echoing crux 3: **energy has no unique address** ([ACC6](acc6-energy-localization.md)), and a density is not an observable.

## Simpler on-ramp

We found that if you assign the gravitational field an energy wherever its "strength squared" is nonzero, then Schwarzschild's field carries four times the energy the plain Newtonian rule would give.

Does that mean a Schwarzschild-bound system weighs four times less, or is four times harder to pull apart? No. The *actual* togetherness energy is $-U$ for everyone — that is the number you'd measure with a winch, and Schwarzschild is not special there. The "times four" is only about *where you filed* the energy. Schwarzschild files a big negative number under "field" ($-4U$) and a big positive number under "matter" ($+3U$); they add back to the same $-U$. Choosing to file more energy in one drawer and less in another never changes the total in the safe. The factor of four is a filing quirk of one particular filing system, not a fact about how strongly the system is bound.

## Check your understanding

1. Trace exactly where the factor of 4 comes from in $u_{-1}=4u_N$.
2. Why is it wrong to say "Schwarzschild's binding energy is $4\times$ Newtonian"?
3. How does $u_{-1}=4u_N$ connect to the $+3U$ that matter must carry?

<details>
<summary>Answers</summary>

- **1.** From $s=2\Phi/c^2$: the factor 2 in the relation becomes $2^2=4$ when squared in $|\nabla s|^2=4|\nabla\Phi|^2/c^4$. The $c^4$'s cancel against the $c^4$ in the density prefactor, leaving $u_{-1}=-4|\nabla\Phi|^2/8\pi G=4u_N$.
- **2.** Because binding energy is the *total* interaction $-U$, which is convention-independent and the same for all members. Only the field *share* under the gradient-local convention is quadrupled, and it is exactly canceled by the matter share.
- **3.** Field share $=4\lambda U=-4U$ for $\lambda=-1$; the invariant total $-U$ then forces matter share $=-U-(-4U)=+3U$. So $u_{-1}=4u_N$ (field $=-4U$) and "matter carries $+3U$" are two views of one ledger balancing at $-U$.

</details>

## What the paper claims here

Grounds: **Sec. 4.6** ("Localization corollary — factor of four"). The paper computes $u_{-1}=-\frac{c^4|\nabla s|^2}{8\pi G}$, uses $s=2\Phi/c^2$ so $|\nabla s|^2=4|\nabla\Phi|^2/c^4$, and gets $u_{-1}=-4\frac{|\nabla\Phi|^2}{8\pi G}=4u_N$, where $u_N=-\frac{|\nabla\Phi|^2}{8\pi G}$. It states explicitly this "does **not** mean observable binding energy is 4×; total stays $-U$," that the Schwarzschild source term assigns $-4U$ to the field cross energy so matter must contribute $+3U$, and that Schwarzschild's nonlinearity is not the standard Newtonian gradient density counted once — the coefficient differs by a factor 4 in magnitude. What the paper does **not** claim: any observable consequence of the factor 4; it is a property of the localization convention only.

---
**Path navigation:** ← [prev: ACC4](acc4-matter-conventions-bound.md) · [next: ACC6](acc6-energy-localization.md) →
**See also:** [ACC3](acc3-field-cross-term.md), [ENE1](../part1-foundations/ene1-self-energy.md), [ACC6](acc6-energy-localization.md)
