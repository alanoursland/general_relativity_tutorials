# Areal vs. Isotropic Coordinates

> **Tutorial `PPN2`** · Part 6 · **Goal:** Derive the coordinate transformation that turns the family's areal-coordinate metric into the isotropic form PPN is written in, through the order needed for $\gamma,\beta$ · **Prereqs:** [PPN1](./ppn1-ppn-formalism.md), [F4](../part1-foundations/f4-curvilinear-coordinates.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md)

**Where this sits in the arc.** `CORE4` built $A_\lambda(r)$ in *areal* coordinates ($r$ = the radius at which a sphere has area $4\pi r^2$) because that is the natural coordinate for the flux postulate (I2). PPN, by convention, is written in *isotropic* coordinates, where the spatial metric is a single scalar function times flat space. This tutorial does the purely coordinate-theoretic work of relating the two — a change of labels, not a change of physics — so that `PPN3` can read off $\gamma$ and $\beta$ directly.

## Why isotropic coordinates

In areal coordinates the family's metric is
$$ds^2 = -A(r)c^2dt^2 + B(r)dr^2 + r^2 d\Omega^2, \qquad B=A^{-1},$$
with $r$ picked out by a geometric property (sphere area) that has nothing to do with how "close" two nearby spheres are in radial distance. The PPN spatial metric, by contrast, is written as $(1+2\gamma U)\delta_{ij}$ times the flat-space line element $d\rho^2+\rho^2d\Omega^2$ — a single overall scale factor multiplying ordinary flat space, the same factor in every direction (that is what "isotropic" means here: locally, the metric looks like a rescaled Euclidean metric, not a stretched one). This is the natural gauge for comparing different metric theories weak-field term by weak-field term, because a bare scalar prefactor is the simplest possible way to package "how much bigger rulers are near the mass," with no leftover angular distortion to track. Areal $r$ does not have this property — its angular part is untouched ($r^2 d\Omega^2$, coefficient exactly 1) while its radial part carries a separate function $B(r)$. To compare with PPN we must find a new radial label $\rho$ under which *both* $d\rho^2$ and $\rho^2d\Omega^2$ pick up the *same* prefactor.

## Setting up the transformation

Seek $r$ as a function of a new coordinate $\rho$, order by order in the small parameter $w \equiv r_s/\rho$:
$$r = \rho\left(1+k_1 w + k_2 w^2 + O(w^3)\right).$$
Demanding the spatial part become isotropic, $B(r)\,dr^2 + r^2 d\Omega^2 = \Psi^2(\rho)\left(d\rho^2+\rho^2d\Omega^2\right)$, forces two conditions: the angular part fixes $\Psi^2 = r^2/\rho^2$, and the radial part then requires
$$B(r)\left(\frac{dr}{d\rho}\right)^2 = \frac{r^2}{\rho^2}.$$
This single equation, expanded order by order in $w$, determines $k_1$ and $k_2$.

## Expanding both sides

Recall from `WEAK1` (with $x=r_s/r$): $A(r) = 1 - x + a_2 x^2 + O(x^3)$, $a_2 = (1+\lambda)/2$. Since $B=1/A$,
$$B(r) = 1 + x + (1-a_2)x^2 + O(x^3).$$
(Check: $1/(1-x+a_2x^2) = 1+(x-a_2x^2)+x^2+O(x^3) = 1+x+(1-a_2)x^2+O(x^3)$.)

From $r=\rho(1+k_1w+k_2w^2)$ and $w=r_s/\rho$, write $r = \rho + k_1 r_s + k_2 r_s^2/\rho$. Since $r_s$ is a constant,
$$\frac{dr}{d\rho} = 1 - k_2\frac{r_s^2}{\rho^2} + O(w^3) = 1 - k_2 w^2 + O(w^3),$$
with **no** term linear in $w$ — the $k_1$ piece is a constant shift and drops out of the derivative. Squaring,
$$\left(\frac{dr}{d\rho}\right)^2 = 1 - 2k_2 w^2 + O(w^3).$$

Next we need $x=r_s/r$ re-expressed in $w$. Inverting $r=\rho(1+k_1w+k_2w^2)$ to first order in the bracket,
$$\frac{1}{r} = \frac{1}{\rho}\left(1 - k_1 w + O(w^2)\right) \implies x = \frac{r_s}{r} = w\left(1-k_1w+O(w^2)\right) = w - k_1 w^2 + O(w^3).$$

Substitute this into $B(r)$:
$$B(x(w)) = 1 + \left(w-k_1w^2\right) + (1-a_2)w^2 + O(w^3) = 1 + w + \left[(1-a_2)-k_1\right]w^2 + O(w^3).$$

Multiply by $(dr/d\rho)^2$, keeping terms through $w^2$ (the cross term $w\cdot(-2k_2w^2)$ is $O(w^3)$ and drops):
$$B(r)\left(\frac{dr}{d\rho}\right)^2 = 1 + w + \left[(1-a_2)-k_1-2k_2\right]w^2 + O(w^3).$$

The right-hand side of the matching equation is
$$\frac{r^2}{\rho^2} = \left(1+k_1w+k_2w^2\right)^2 = 1 + 2k_1 w + \left(2k_2+k_1^2\right)w^2 + O(w^3).$$

## Matching order by order

**Order $w$:** $1 = 2k_1$, so
$$\boxed{k_1 = \tfrac12}.$$

**Order $w^2$:** substitute $k_1=1/2$ into both sides:
$$(1-a_2) - \tfrac12 - 2k_2 = 2k_2 + \tfrac14 \implies \tfrac14 - a_2 = 4k_2,$$
so
$$\boxed{k_2 = \frac{1-4a_2}{16}}.$$

Both results match the paper's Sec. 5.1.1 exactly, and follow from nothing but demanding the areal metric look isotropic through second order.

## What falls out immediately

With $k_1=1/2$ fixed, the conformal factor becomes
$$\frac{r^2}{\rho^2} = 1 + 2k_1 w + O(w^2) = 1 + w + O(w^2),$$
independent of $a_2$ — hence independent of $\lambda$. This single fact, carried into `PPN3`, is what forces $\gamma=1$ for *every* member of the family: the first-order isotropic spatial factor never had a chance to depend on the nonlinear coefficient, because $k_1$ was pinned down entirely by the *first-order* matching condition, before $a_2$ ever entered. Similarly, with $x=w-\tfrac12w^2+O(w^3)$ now fixed, `PPN3` substitutes this into $A(r)$ to extract $\beta$.

## Simpler on-ramp

Think of areal radius as "labeling spheres by their surface area" and isotropic radius as "labeling points by ordinary flat-space-like rulers, rescaled uniformly in every direction." These are two different rulers laid on the same curved space, and converting one to the other is bookkeeping, not physics — like converting Celsius to Fahrenheit doesn't change the temperature. The transformation $r=\rho(1+k_1w+k_2w^2+\dots)$ is just "how much do the two rulers disagree, order by order, as you get close to the mass." The disagreement at leading order ($k_1$) is fixed purely by matching areas to first order and turns out the same no matter which member of the family you're looking at; the disagreement at the next order ($k_2$) is where the family's members start to show through, because it has to compensate for whatever nonlinear term ($a_2$) that particular member's areal metric carries.

## Check your understanding

- Why does angular matching alone force $\Psi^2 = r^2/\rho^2$, with no separate freedom?
- Why does $k_1$ not depend on $a_2$ (i.e., not on $\lambda$)?
- What would go wrong with the whole comparison if we tried to read $\gamma,\beta$ directly off the areal-coordinate metric instead of transforming first?

**Answers**
- The angular part of both metrics is $(\text{radius})^2 d\Omega^2$ with no free coefficient of its own; matching it fixes the overall isotropic prefactor $\Psi^2$ to be exactly $r^2/\rho^2$, since that is the only way the angular pieces can agree.
- $k_1$ is determined purely by the *order-$w$* matching equation, and at that order neither side of the equation has yet involved $a_2$ (the nonlinear coefficient only enters at order $w^2$, through $B(r)$'s $x^2$ term). So $k_1$ is fixed before $\lambda$ has any chance to act.
- Areal $r$'s spatial metric coefficient of $d\Omega^2$ is exactly $r^2$ (coefficient 1, not $1+2\gamma U$-like); reading PPN parameters off it directly would misidentify the radial stretching $B(r)$ as if it were an isotropic curvature factor, since areal coordinates keep angular and radial distortion asymmetric by construction.

## What the paper claims here

Grounded in Sec. 5.1.1: the ansatz $r=\rho(1+k_1w+k_2w^2+O(w^3))$, $w=r_s/\rho$; the matching condition $B(r)(dr/d\rho)^2=r^2/\rho^2$; and the results $k_1=1/2$, $k_2=(1-4a_2)/16$. The paper treats this purely as coordinate algebra needed to compare with the PPN convention — it does not claim isotropic coordinates are more "physical" than areal ones, only more convenient for this comparison.

---
**Path navigation:** ← [prev in default path](./ppn1-ppn-formalism.md) · [next](./ppn3-gamma-beta.md) →
**See also:** [F4](../part1-foundations/f4-curvilinear-coordinates.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [CORE4](../part3-building-the-family/core4-classification-theorem.md)
