# Properties of Schwarzschild

> **Tutorial `S3`** · Part 2 · **Goal:** Survey the physical content of the Schwarzschild metric — horizon, redshift, orbits, classical tests — as ordinary GR predicts them, before any of Part III's alternatives are on the table. · **Prereqs:** [S2](./s2-deriving-schwarzschild.md), [BIRK](./birkhoff.md)

**Where this sits in the arc.** Every one of these properties will recur later as a *discriminator*: which ones survive unchanged across the whole $\lambda$-family (blind tests), and which one — perihelion precession — breaks the degeneracy and selects Schwarzschild in `PPN5`. Read this tutorial as "what GR says the answer is," so that later tutorials can show you exactly how much of it the paper's weaker postulates actually reproduce.

## The metric, again

$$ds^2 = -\left(1-\frac{r_s}{r}\right)c^2dt^2 + \left(1-\frac{r_s}{r}\right)^{-1}dr^2 + r^2 d\Omega^2, \qquad r_s = \frac{2GM}{c^2}.$$

$r$ is the areal radius (`F4`): the sphere at coordinate value $r$ has surface area $4\pi r^2$, regardless of how curved the interior geometry is. Everything below is stated for $r>r_s$, outside the horizon.

## The horizon at $r_s$

At $r=r_s$, the metric coefficient $A=1-r_s/r$ vanishes and $B=1/A$ diverges — the coordinates used here break down. `S4` works out in detail why this is a coordinate artifact rather than a physical pathology (finite curvature invariants there) while $r=0$ is a genuine curvature singularity. For now, note the qualitative fact that matters for everything downstream: for $r<r_s$, $A<0$, so the roles of $t$ and $r$ as timelike/spacelike coordinates swap — $r$ becomes the timelike direction, decreasing $r$ becomes as unavoidable as the passage of time is outside. That is the operational meaning of "horizon": once inside, every future-directed path reaches $r=0$.

## Gravitational time dilation and redshift

A clock sitting at fixed $r$ (a "static observer") measures proper time $\tau$ related to coordinate time $t$ by

$$d\tau = \sqrt{A(r)}\,dt = \sqrt{1-\frac{r_s}{r}}\;dt.$$

Clocks deeper in the potential (`smaller $r$`) tick slower as seen by a distant observer. Light emitted at radius $r_{\rm e}$ with proper frequency $\nu_{\rm e}$ and received far away ($r\to\infty$) is redshifted according to

$$1+z = \frac{\nu_{\rm e}}{\nu_{\rm obs}} = \frac{1}{\sqrt{A(r_{\rm e})}} = \left(1-\frac{r_s}{r_{\rm e}}\right)^{-1/2}.$$

As $r_{\rm e}\to r_s$, $z\to\infty$: light from just outside the horizon is redshifted without bound — one more way of stating that the horizon is where a static observer would need to accelerate infinitely hard to hold position, and eventually cannot hold it at all.

## Orbits

Spherical symmetry and staticity supply two conserved quantities per geodesic (via the Killing vectors associated with time-translation and rotation, `F5`): a conserved energy-per-mass $E/c^2$ conjugate to $t$, and a conserved angular momentum-per-mass $L$ conjugate to $\phi$ (motion confined to a plane by symmetry, taken as $\theta=\pi/2$). Substituting into the geodesic equation for radial motion yields an effective-potential form,

$$\left(\frac{dr}{d\tau}\right)^2 = \frac{E^2}{c^2} - c^2\left(1-\frac{r_s}{r}\right)\left(1+\frac{L^2}{r^2c^2}\right),$$

structurally like a Newtonian energy equation $\dot r^2 = 2(\mathcal E - V_{\rm eff})$ with an effective potential

$$V_{\rm eff}(r) = c^2\left(1-\frac{r_s}{r}\right)\left(1+\frac{L^2}{r^2c^2}\right).$$

The Newtonian $-GM/r$ and centrifugal $L^2/r^2$ terms both appear, but GR adds a new term $\propto -GML^2/(r^3c^2)$ absent from Newtonian mechanics: an extra attractive term that grows faster than the centrifugal repulsion as $r$ shrinks. This is what makes the innermost stable circular orbit exist at $r_{\rm isco}=6GM/c^2 = 3r_s$ (below which no stable circular orbit exists at all, however large $L$ is made) and what produces the perihelion precession of eccentric orbits — the correction term makes orbits fail to close into simple ellipses, precessing forward each period.

## The classical tests, as GR predicts them

- **Gravitational redshift**: given above; leading order $z\approx r_s/(2r_{\rm e})$, i.e. $\Delta\nu/\nu \approx -GM/(rc^2)$ — a purely Newtonian-order effect.
- **Light bending**: a photon passing at impact parameter $b\gg r_s$ is deflected by angle $\delta\phi \approx 4GM/(c^2 b) = 2r_s/b$ — twice the naive Newtonian estimate, a famous factor traced in `HIST2`.
- **Shapiro (radar) delay**: a round-trip radar signal grazing the Sun is delayed relative to flat spacetime by an amount $\propto GM/c^3\ln(\cdots)$, logarithmically sensitive to how close the ray passes.
- **Perihelion precession**: an eccentric orbit of semi-major axis $a$ and eccentricity $e$ advances its perihelion each orbit by

$$\delta\phi_{\rm peri} = \frac{6\pi GM}{c^2 a(1-e^2)},$$

which for Mercury evaluates to about $43''$ of arc per century (after subtracting known Newtonian perturbations from other planets) — the classic confirmation of GR, and, as `PPN5` will show, the single test in this list sharp enough to separate Schwarzschild from every other member of the $\lambda$-family.

## Simpler on-ramp

Picture the Schwarzschild geometry as a funnel-shaped dip in an otherwise flat rubber sheet, deeper and steeper the closer you get to $r_s$. A ball rolling near the rim (large $r$) behaves almost exactly like it would under ordinary Newtonian gravity — ellipse-like orbits, mild light bending, small clock-rate differences. Closer to the rim of the funnel, the sheet curves away faster than Newton's $1/r^2$ law would predict, so orbits start to drift (precess) instead of closing, light bends more than a naive straight-line estimate would suggest, and clocks run detectably slower. At the funnel's throat, $r=r_s$, the slope becomes vertical in these coordinates — anything crossing it can only continue falling inward, never back out.

## Check your understanding

- Why does gravitational redshift diverge as $r_{\rm e}\to r_s$, and what does that divergence mean physically for a would-be static observer there?
- What extra term appears in the GR effective potential that has no Newtonian counterpart, and what does it do to orbits at small $r$?
- Why is perihelion precession, rather than redshift or light bending, singled out later as the test that discriminates between $\lambda$-family members?
- In what sense does light bending give "twice" the Newtonian estimate, and why is that worth remembering?

**Answers**
- $1+z=(1-r_s/r_{\rm e})^{-1/2}$ blows up as $A(r_{\rm e})\to0$; physically, a static observer that close to $r_s$ would need unbounded proper acceleration to resist falling in, so no static observer can actually sit there — the divergence is the metric's way of saying the horizon is not a place a static clock can occupy.
- A term $\propto -GML^2/(r^3c^2)$, absent in Newtonian mechanics, which grows faster than the centrifugal barrier as $r\to0$; it removes the innermost stable circular orbit below $r=6GM/c^2$ and drives eccentric orbits to precess rather than close.
- Because redshift and light bending/Shapiro delay depend only on the leading Newtonian term and on $\gamma$ respectively, both of which turn out identical across the whole family (`WEAK1`, `PPN4`); precession additionally depends on $\beta$, the one parameter that actually varies with $\lambda$.
- Because a naive Newtonian light-bending estimate (treating light as a slow test particle with speed $c$) predicts half of Einstein's full 1915 value; the missing half comes from spatial curvature, not from the time–time part of the metric alone — the point developed fully in `HIST2`.

## What the paper claims here

The paper does not re-derive these properties — they are standard textbook GR, assumed as background (§2.5 identifies Schwarzschild as the $\lambda=-1$ member; §5–6 quote redshift, light bending, Shapiro delay, and perihelion precession as *known* GR results to compare the family against). This tutorial supplies exactly that background so `WEAK1`, `PPN4`, and `PPN5` can meaningfully say which of these properties survive across the family unchanged and which one breaks the tie.

---
**Path navigation:** ← [prev in default path](./birkhoff.md) · [next](./s4-singularities.md) →
**See also:** [F5](../part1-foundations/f5-geodesics.md), [F4](../part1-foundations/f4-curvilinear-coordinates.md), [PPN4](../part6-ppn-observation/ppn4-classical-tests.md), [PG3](../part7-michell-pg/pg3-newtonian-infall.md)
