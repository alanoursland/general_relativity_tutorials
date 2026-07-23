# The PPN Formalism, Gently

> **Tutorial `PPN1`** · Part 6 · **Goal:** Learn the two-number language ($\gamma$, $\beta$) that lets solar-system data test which member of the $\lambda$-family, if any, is right · **Prereqs:** [F6](../part1-foundations/f6-newtonian-limit.md), [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md)

**Where this sits in the arc.** Part V asked whether *energy accounting* could pick out one member of the family and found only a convention-bound interval that excludes Schwarzschild. Part VI asks whether *observation* can do better. Before touching Mercury's orbit we need the vocabulary observers actually use to compare gravity theories against data: the Parametrized Post-Newtonian (PPN) formalism. This tutorial introduces its two relevant numbers, $\gamma$ and $\beta$, and nothing else — the identification of these numbers with $\lambda$ is the payoff of `PPN3`.

## Why you need a second expansion parameter at all

`F6` showed that the Newtonian limit fixes the *leading* term of $-g_{tt}$: $A \approx 1 + 2\Phi/c^2$. That single term already reproduces Newtonian gravity, including Mercury's ordinary orbital motion. But it says nothing about two further questions a real solar system can answer:

- Does space itself curve, and if so by how much per unit potential? (Newtonian space is flat by fiat — there is no term in Newtonian theory that curves it.)
- When the potential $\Phi$ gets self-referential — when the source of gravity is partly gravity's own energy — does the metric respond *linearly*, exactly as if two potentials had simply added, or is there an extra push or pull?

Both questions live one order higher than the Newtonian term, in the regime called *post-Newtonian*: corrections of relative size $U \equiv GM/(c^2\rho)$, the same small dimensionless number that measures $\Phi/c^2$ or $v^2/c^2$ for a bound orbit. ($\rho$ here is a radial coordinate to be pinned down precisely in `PPN2`; for now read it as "distance from the mass.") PPN is simply the bookkeeping scheme for these next-order terms, common to any metric theory of gravity, GR included.

## The isotropic PPN metric

For a single static, spherically symmetric mass, the PPN expansion of the metric — written in a coordinate system chosen so that the spatial part is a single scalar function times flat space (why *that* choice, rather than areal coordinates, is the subject of `PPN2`) — reads

$$ds^2 = -\left(1 - 2U + 2\beta U^2 + O(U^3)\right)c^2 dt^2 + \left(1+2\gamma U + O(U^2)\right)\left(d\rho^2+\rho^2 d\Omega^2\right),$$

with $U \equiv GM/(c^2\rho)$. Everything a static spherical source can contribute to the metric, to this order, is packaged into exactly two dimensionless numbers, $\gamma$ and $\beta$.

## Reading $\gamma$: space curvature per unit potential

The Newtonian limit fixes the $-2U$ term in $g_{tt}$ but is silent about $g_{ij}$; Newtonian space is flat, full stop. $\gamma$ is the coefficient that measures how much a *relativistic* theory curves space in response to the same potential $U$ that slows clocks. It is a pure statement about the spatial metric: $\gamma=0$ means flat space regardless of $U$ (a theory in which only clocks respond to mass); $\gamma=1$ means space curves exactly as strongly, term for term, as time does. General relativity predicts $\gamma=1$. This has direct observational teeth, because light responds to *both* the time part and the space part of the metric — so $\gamma$ controls light bending and radar (Shapiro) time delay, both of which vanish for a Newtonian-space theory ($\gamma=0$) and are largest, matching observation, at $\gamma=1$ (`PPN4`).

## Reading $\beta$: nonlinearity of the time–time term

The Newtonian potential adds linearly: two masses' potentials at a point are the simple sum $\Phi_1+\Phi_2$, with no cross-correction. GR's own field equations are nonlinear — gravity gravitates — so the next-order term in $g_{tt}$ need not be a bare continuation of $-2U$; it can carry an independent coefficient measuring how strongly the potential's *own* energy re-sources the metric. That coefficient is $\beta$: the number multiplying $U^2$ in $g_{tt}$. $\beta=1$ is a very specific, calculable prediction of full GR for the exterior of a static mass; other metric theories, or other closures of a flux law like the one built in Part III, can in principle produce any $\beta$. Because $\beta$ multiplies $U^2$ rather than $U$, it is invisible to any test that only probes the metric to first order in $U$ — you need genuinely nonlinear, second-order-in-potential data to see it. That is exactly what perihelion precession supplies (`PPN5`).

## Scope: only two parameters, here

The full PPN formalism (Will's ten-parameter version) also carries parameters for preferred-frame effects, violations of momentum conservation, and similar phenomena tied to motion, rotation, or multiple bodies. None of those appear for a single static, spherically symmetric source at rest: this problem has no preferred frame to violate and no momentum to fail to conserve. *Beyond the paper:* the restriction to $\gamma,\beta$ alone is a scope fact about the problem, not a claim that the other eight parameters are unmeasurable in general — they simply have nothing to say about a static point mass.

## Simpler on-ramp

Picture two independent knobs on any theory of gravity around a single still, round mass. The first knob, $\gamma$, controls how much the theory bends *space* — imagine a rubber sheet that dips near the mass; $\gamma$ tells you how deep the dip is, over and above what you'd guess from the clock-slowdown alone. Set $\gamma=0$ and the sheet stays perfectly flat no matter how strong gravity is; set $\gamma=1$ (GR's answer) and the sheet dips exactly as much as the clocks slow.

The second knob, $\beta$, is subtler: it asks whether gravity's *own energy* pulls a little extra, over and above simple addition. If you doubled the mass, would the field's contribution to itself double in the "obvious" linear way, or feed back on itself with some extra factor? $\beta=1$ is GR's specific answer to that feedback question for this problem. Both knobs are single real numbers because we have restricted attention to the simplest possible source: one mass, standing still, with no other structure to describe.

## Check your understanding

- Why does the Newtonian limit alone (from `F6`) fix nothing about $\gamma$?
- Why is $\beta$, but not $\gamma$, described as a *nonlinearity* parameter?
- Why doesn't rotation or motion of the source introduce new parameters here?
- If a theory predicted $\gamma=0$, what would that imply about light bending, intuitively?

**Answers**
- The Newtonian limit only constrains the leading term of $-g_{tt}$ ($\propto U^1$); it says nothing at all about $g_{ij}$, which is where $\gamma$ lives.
- $\gamma$ multiplies $U$, a term that would exist even if potentials added perfectly linearly (it just says "space curves too"). $\beta$ multiplies $U^2$, a term that only exists because the source of gravity is, in part, gravity's own energy — a genuinely nonlinear effect with no Newtonian analogue.
- The source here is a single static point mass at rest: there is no preferred frame to break and no momentum-carrying motion to fail to conserve, so the PPN parameters that measure those effects are simply not excited.
- With $\gamma=0$, space stays flat regardless of mass; since light bending needs *both* the time-dilation effect and the spatial-curvature effect to add up, $\gamma=0$ would cut the deflection roughly in half relative to GR (made precise in `HIST2`).

## What the paper claims here

Grounded in Sec. 5.1: the isotropic PPN metric $ds^2=-(1-2U+2\beta U^2+O(U^3))c^2dt^2+(1+2\gamma U+O(U^2))(d\rho^2+\rho^2d\Omega^2)$ with $U\equiv GM/(c^2\rho)$, and the statement that general relativity predicts $\gamma=\beta=1$. The paper does not derive the ten-parameter PPN formalism from scratch or justify why other parameters vanish for this source; it uses only the two-parameter static-spherical restriction, which is the scope adopted here as well.

---
**Path navigation:** ← [prev in default path](../part5-energy-accounting/grsol-are-these-gr-solutions.md) · [next](./ppn2-areal-isotropic.md) →
**See also:** [WEAK1](../part3-building-the-family/weak1-weak-field-degeneracy.md), [F6](../part1-foundations/f6-newtonian-limit.md), [PPN3](./ppn3-gamma-beta.md)
