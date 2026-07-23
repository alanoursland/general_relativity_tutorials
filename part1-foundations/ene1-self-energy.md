# Newtonian Gravitational Potential Energy & Self-Energy

> **Tutorial `ENE1`** · Part 1 · **Goal:** assembly work, the shell theorem, the two equivalent self-energy densities $-\frac{|\nabla\Phi|^2}{8\pi G}$ and $\frac12\rho\Phi$, and the localization ambiguity they expose — in miniature, before any GR. · **Prereqs:** [F6](./f6-newtonian-limit.md), [GAUSS1](./gauss1-flux-laplacian.md).

**Where this sits in the arc.** This tutorial is the dress rehearsal for the entire "does energy accounting select $\lambda$?" story of Part V ([`ACC1`](../part5-energy-accounting/acc1-circularity.md)–[`ACC6`](../part5-energy-accounting/acc6-energy-localization.md)). Its punchline — that gravitational self-energy has a well-defined *total* but no unique *local density* — is not a peculiarity of general relativity. It is already true in plain 19th-century Newtonian gravity, and seeing that clearly here is what makes the later relativistic version legible rather than mysterious.

## Assembly work: the two-body case

Define gravitational potential energy operationally: the work an external agent must do (or, equivalently, the negative of the work gravity itself does) to assemble a configuration by bringing its pieces together quasi-statically from infinite separation. For two point masses $m_1,m_2$ starting infinitely far apart and brought to separation $d$: gravity pulls them together with force $Gm_1m_2/r^2$, doing work

$$W_{\rm gravity} = \int_\infty^{d} \left(-\frac{Gm_1m_2}{r^2}\right)(-dr) = \int_d^\infty \frac{Gm_1m_2}{r^2}\,dr = \frac{Gm_1m_2}{d}$$

as they approach (a winch could extract exactly this much work and store it elsewhere, e.g. as [`ACC2`](../part5-energy-accounting/acc2-invariant-assembly-energy.md) will do explicitly with two mass shells). Since this energy *leaves* the gravitational configuration as it assembles, the configuration's own potential energy is the negative of what left it:

$$U_{\rm grav} = -\frac{Gm_1m_2}{d}.$$

This is the direct Newtonian ancestor of the two-shell winch calculation central to [`ACC2`](../part5-energy-accounting/acc2-invariant-assembly-energy.md): the *total* assembly energy of a system is an unambiguous, operationally defined quantity — you can, in principle, measure exactly how much work a winch extracts.

## The shell theorem

A uniform spherical shell of mass produces **zero** gravitational field everywhere in its interior, and behaves exactly like a point mass at its center for every point outside it. This follows directly from the flux-conservation reasoning of [`GAUSS1`](./gauss1-flux-laplacian.md): any sphere drawn strictly *inside* a mass shell encloses zero mass, so the flux through it — and hence, by spherical symmetry, the field strength everywhere on it — is exactly zero. This is not a separate postulate; it's the same $4\pi r^2 V'(r)=\text{const}$ bookkeeping applied to a region with no enclosed source. The shell theorem is the exact tool [`ACC3`](../part5-energy-accounting/acc3-field-cross-term.md) uses to localize where an interaction (cross) term can and cannot be nonzero.

## Self-energy of a continuous distribution: two equivalent formulas

For a continuous mass density $\rho(\mathbf{x})$ sourcing potential $\Phi(\mathbf{x})$ via Poisson's equation, $\nabla^2\Phi = 4\pi G\rho$ (the source-full generalization of the vacuum $\Delta V=0$ from [`GAUSS1`](./gauss1-flux-laplacian.md)), the total gravitational self-energy can be written two seemingly different ways:

$$E_{\rm self} = \frac12\int \rho(\mathbf{x})\,\Phi(\mathbf{x})\,d^3x \qquad \text{(matter-weighted form)}$$

$$E_{\rm self} = -\frac{1}{8\pi G}\int |\nabla\Phi|^2\, d^3x \qquad \text{(field-gradient form)}.$$

The first sums, over every point where matter actually sits, one-half the mass element times the potential *there* (the $\tfrac12$ avoids double-counting each pair of mass elements — every pair's mutual interaction energy $-Gm_im_j/r_{ij}$ would otherwise be counted twice, once from each element's perspective, since $\Phi(\mathbf{x})$ already sums the contribution of every other mass element). The second integrates a energy density built purely from the field's gradient, over **all of space** — including regions where $\rho=0$ entirely.

## Why they're identical: integration by parts plus the field equation

Start from the matter-weighted form and substitute $\rho = \nabla^2\Phi/(4\pi G)$ from Poisson's equation:

$$E_{\rm self} = \frac12\int \rho\,\Phi\,d^3x = \frac{1}{8\pi G}\int \Phi\,\nabla^2\Phi\;d^3x.$$

Integrate by parts (the divergence theorem, run in reverse): for any well-behaved $\Phi$,

$$\int \Phi\,\nabla^2\Phi\; d^3x = \oint_{\partial V} \Phi\,\nabla\Phi\cdot d\mathbf{A} \;-\; \int |\nabla\Phi|^2\, d^3x.$$

Take the boundary $\partial V$ to be a sphere at infinity. For an isolated source, $\Phi\sim -GM/r$ and $\nabla\Phi\sim GM/r^2$ at large $r$, so the boundary integrand scales as $\Phi\,\nabla\Phi\cdot(\text{area}) \sim \frac{1}{r}\cdot\frac{1}{r^2}\cdot r^2 = \frac1r \to 0$ — the boundary term vanishes. So:

$$\int\Phi\nabla^2\Phi\,d^3x = -\int|\nabla\Phi|^2\,d^3x \quad\Longrightarrow\quad E_{\rm self} = \frac{1}{8\pi G}\Big(-\int|\nabla\Phi|^2\,d^3x\Big) = -\frac{1}{8\pi G}\int|\nabla\Phi|^2\,d^3x.$$

The two formulas give **exactly the same total**, for every configuration — but only after using the field equation ($\nabla^2\Phi=4\pi G\rho$) and discarding a boundary term. This "integration by parts plus the field equation" move is worth remembering by name; it is *exactly* the move [`ACC3`](../part5-energy-accounting/acc3-field-cross-term.md) performs in the relativistic setting to isolate the cross-term contribution to assembly energy.

## The localization ambiguity, in miniature

Here is the point this whole tutorial has been building to, and it needs no general relativity whatsoever to see: the two formulas agree on the **total**, but they disagree, pointwise, on **where** that energy "lives." The matter-weighted density $\tfrac12\rho\Phi$ is exactly zero everywhere outside the matter (since $\rho=0$ there) — all the energy, on this reading, sits *inside* the source. The field-gradient density $-|\nabla\Phi|^2/(8\pi G)$ is generically nonzero **everywhere the field extends**, including empty space arbitrarily far from any matter — on this reading, energy is spread throughout the surrounding vacuum.

Both are correct, self-consistent bookkeeping schemes; both integrate to the identical, physically meaningful total. But asking "how much gravitational potential energy is stored in this particular empty region of space, away from any matter?" has **no coordinate-free, convention-independent answer** — it depends entirely on which of the two (or which blend of the two) you choose to call "the" local energy density, a choice not fixed by any physical measurement, only by bookkeeping preference. This is the exact seed of two ideas developed at length once GR enters: the **self-consistency-lemma** worry that a density *defined* by reading a term off the field equation cannot be used to independently test or constrain that same equation ([`ACC1`](../part5-energy-accounting/acc1-circularity.md)), and the broader fact that **gravitational energy has no unique local address** ([`ACC6`](../part5-energy-accounting/acc6-energy-localization.md)) — true already here, in Newton, a century before general relativity made it famous.

## Simpler on-ramp

Imagine a company with a single, well-defined total annual profit — nobody disputes that number. Now ask: "how much of that profit did the marketing department generate, versus engineering?" Different, equally defensible accounting conventions will split the credit differently between departments — one convention might assign all the value to wherever the final sale happened, another might assign it proportionally to where costs were incurred — and both conventions can be made internally consistent and both will sum to the same total. But there may simply be no convention-independent fact of the matter about "how much profit lives in aisle 7." Gravitational self-energy is exactly like this: the total is real and measurable (via assembly work); its split into a spatial density is a bookkeeping choice, and two entirely reasonable choices ($\tfrac12\rho\Phi$ versus $-|\nabla\Phi|^2/8\pi G$) disagree about where the energy is while agreeing, necessarily, about how much there is.

## Check your understanding

1. Why does the matter-weighted formula for self-energy carry a factor of $\tfrac12$?
2. What two ingredients are needed to show $\tfrac12\int\rho\Phi\,d^3x$ equals $-\frac{1}{8\pi G}\int|\nabla\Phi|^2 d^3x$?
3. Where does the matter-weighted density say energy is stored, versus where the field-gradient density says it is stored? Can both be right?
4. Why is this ambiguity not a special pathology of general relativity?

<details>
<summary>Answers</summary>

- **1.** To avoid double-counting: summing $\rho(\mathbf{x})\Phi(\mathbf{x})$ over all $\mathbf{x}$ counts each pair of mass elements' mutual interaction energy twice (once from each element's contribution to the other's potential), so the sum must be halved to recover the actual total.
- **2.** Poisson's equation ($\nabla^2\Phi=4\pi G\rho$, to rewrite $\rho$ in terms of $\Phi$) and integration by parts (the divergence theorem, discarding a vanishing boundary term at infinity for an isolated source).
- **3.** The matter-weighted density says all the energy sits where matter actually is (zero elsewhere); the field-gradient density says energy is spread through all of space wherever the field is nonzero, including empty regions. Both are right about the *total*; neither is uniquely "more correct" about the *local* density — that split is a convention, not a physical fact.
- **4.** Because it appears already in ordinary Newtonian gravity, using nothing but Poisson's equation and elementary vector calculus — no curved spacetime, no pseudotensors, no relativity of any kind are needed to produce it. It is a generic feature of any field theory where "self-energy" can be written either as matter-weighted or field-gradient-weighted.

</details>

## What the paper claims here

This tutorial grounds the Newtonian prerequisite the paper invokes at the start of §4: "localization convention-dependent even in Newton: $-|\nabla\Phi|^2/(8\pi G)$ vs. $\frac12\rho\Phi$ (up to boundary terms + field eq)." The paper uses exactly this pre-GR fact to motivate why an analogous ambiguity — and an analogous circularity risk in trying to use it to fix a physical parameter — should be expected, not surprising, once the same two-density structure reappears for the relativistic $\lambda$-family in §4.1–4.3 ([`ACC1`](../part5-energy-accounting/acc1-circularity.md)–[`ACC3`](../part5-energy-accounting/acc3-field-cross-term.md)).

---
**Path navigation:** ← [prev in default path](./gauss1-flux-laplacian.md) · [next: S1 — The vacuum Einstein equations](../part2-schwarzschild/s1-vacuum-einstein.md) →
**See also:** [ACC1](../part5-energy-accounting/acc1-circularity.md), [ACC2](../part5-energy-accounting/acc2-invariant-assembly-energy.md)
