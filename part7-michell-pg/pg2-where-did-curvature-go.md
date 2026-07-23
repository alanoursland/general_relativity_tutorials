# PG2 — Where did the curvature go?

> **Tutorial `PG2`** · Part VII · **Goal:** Resolve the apparent paradox that Painlevé–Gullstrand slices are flat while the spacetime is curved — locate exactly where the gravity went. · **Prereqs:** [PG1](./pg1-painleve-gullstrand.md), [F7](../part1-foundations/f7-curvature.md), [CORE2](../part3-building-the-family/core2-log-variable-closure.md)

**Where this sits in the arc.** This is a short, pointed detour, and it matters precisely because it is the clearest possible instance of the book's recurring lesson: an invariant fact (here, curvature; earlier, the family member itself) can be relocated between different pieces of a chosen representation without becoming any more or less real. It is the geometric twin of [CORE2](../part3-building-the-family/core2-log-variable-closure.md)'s discovery that $\lambda$ is a property of a closure choice, not of the geometry.

## The apparent puzzle

[PG1](./pg1-painleve-gullstrand.md) derived, for any family member,
$$ds^2 = -c^2dT^2 + \big(dr+v(r)\,dT\big)^2 + r^2d\Omega^2,$$
and showed that the constant-$T$ slice, $d\ell^2=dr^2+r^2d\Omega^2$, is exactly flat Euclidean 3-space. If space, sliced this way, is flat — where is gravity? A mass $M\neq0$ certainly still gravitates in these coordinates: a dropped object accelerates, light bends, and so on. Flatness of a *slice* cannot mean the *spacetime* is flat, or gravity would have vanished by a change of clock — plainly false, since $A_\lambda(r)\not\equiv1$ whenever $M\neq0$, and a metric identically equal to flat Minkowski space is the *only* way for every curvature invariant to vanish everywhere. So the 4-dimensional spacetime is still curved; only a particular 3-dimensional slice through it is flat.

## Intrinsic vs. extrinsic: the resolution

The resolution is the same one that shows up whenever a curved higher-dimensional object contains a straight or flat lower-dimensional slice: a submanifold's own, *intrinsic* curvature (computable from measurements confined to the submanifold) is logically independent of how that submanifold is *bent* within the larger space that contains it (its *extrinsic* curvature). A straight line drawn on a sphere's surface is intrinsically straight, but it is still a curve bent within 3-space; a flat sheet of paper can be rolled into a curved cylinder while every intrinsic distance on the paper is unchanged. Here, the constant-$T$ slices are intrinsically flat — literally ordinary $\mathbb{R}^3$ in spherical coordinates — but the *family of slices*, stacked up as $T$ advances, is bent within the 4-dimensional spacetime, and that bending is exactly what the extra piece of the metric encodes.

Cast the PG metric in the standard "lapse and shift" form used to describe how one slice sits relative to the next:
$$ds^2 = -N^2c^2dT^2 + \gamma_{ij}\big(dx^i+N^idT\big)\big(dx^j+N^jdT\big),$$
where $\gamma_{ij}$ is the spatial metric on a slice, $N$ is the lapse (how much proper time elapses per unit $T$ for an observer sitting still in the spatial coordinates), and $N^i$ is the shift (how much the spatial coordinate origin itself is dragged as $T$ advances). Reading off PG1's result: $\gamma_{ij}dx^idx^j = dr^2+r^2d\Omega^2$ (flat, no $\lambda$-dependence at all), the lapse is the *constant* $N=1$ (the $-c^2dT^2$ coefficient carries no $r$-dependence once $v$ is moved into the shift), and the entire radial shift is $N^r=v(r)$. **All of the gravitational information — everything that distinguishes this spacetime from flat Minkowski space, and everything that distinguishes one family member from another — lives in the single function $v(r)$.** The spatial metric is trivial and the lapse is a bare constant; nothing is left for them to encode.

## Why this doesn't contradict curvature invariants

The genuinely coordinate-independent facts about curvature — the ones [F7](../part1-foundations/f7-curvature.md) establishes matter, like the Kretschmann scalar or tidal forces measured by nearby free-falling observers — are properties of the full 4-metric, not of any one 3-slice's intrinsic geometry. A slicing in which the intrinsic 3-curvature happens to vanish identically is not a slicing in which the 4-curvature vanishes; it is a slicing in which *all* of the curvature has been pushed into the extrinsic bending of the slices relative to each other, i.e., into how fast the shift $v(r)$ changes from one radius to the next. Concretely: $v(r)$ is nonconstant precisely because $A_\lambda(r)$ is nonconstant, and it is $v'(r)$ — the rate at which neighboring slices are dragged at different rates — that ultimately feeds the nonzero curvature invariants. The mixed term $2v\,dr\,dT$ is exactly what tilts the light cones (made precise in [PG4](./pg4-horizons-light-cones.md)); tilting light cones is a genuine, invariant, physical effect, and it is only visible once you look at more than one slice at a time.

**Beyond the paper:** the paper states the qualitative fact ("gravity encoded in mixed term $2v\,dr\,dT$... flat slices ≠ flat spacetime") without invoking lapse/shift language explicitly; the intrinsic/extrinsic framing above is a standard, correct way of making that statement precise, offered here as an aid to intuition rather than as an additional claim of the source.

## The echo of CORE2

[CORE2](../part3-building-the-family/core2-log-variable-closure.md) showed that $\lambda$ — which member of the family you have — is a fact about which potential variable was declared to satisfy the flux law; it is not written into the geometry in any unique way; you can only read it off once you've fixed a representation (the variable $s=\ln A$ and the closure $-F''/F'=\lambda$). Here, the same kind of move happens one level up: "where the curvature lives" — in the spatial metric's curvature (areal or isotropic coordinates) or in the mixed term (PG coordinates) — is likewise a fact about the representation, not the geometry. The invariant, representation-independent fact in both cases is unchanged (the actual value of $\lambda$; the actual tidal forces an observer feels); what moves is only which slot of a particular coordinate system you'd point to as "where it's stored."

## Simpler on-ramp

Imagine photographing a bent piece of wire from exactly the angle that makes its silhouette look like a straight line. The photograph (the "slice") is honestly straight — nothing about the picture is curved. But the wire itself, in three dimensions, is still bent; you've only found an angle from which one particular cross-section of it looks flat. Painlevé–Gullstrand coordinates do something analogous to spacetime: they choose a family of "instants" from which the spatial cross-section looks perfectly flat. That doesn't erase the bending of the whole four-dimensional object — it just means the bending shows up in how the "photographs" are angled relative to one another as you flip through them (the mixed term), not in any single photograph on its own.

## Check your understanding

- If a spatial slice through a spacetime is intrinsically flat, does that prove the full spacetime is flat?
- In the lapse/shift decomposition of the PG metric, which piece carries all the gravitational content, and which pieces are trivial?
- In what precise sense is this tutorial "a direct echo" of CORE2?
- Could a spacetime with $M\neq0$ ever have every curvature invariant vanish, in any coordinates?

**Answers**
- No. Intrinsic flatness of one submanifold says nothing about how that submanifold is bent within the larger space, or about the larger space's own curvature; PG slices are the standing counterexample.
- The shift, $N^r=v(r)$, carries everything; the lapse is the constant $N=1$ and the spatial metric $\gamma_{ij}$ is flat and $\lambda$-independent.
- Both show a genuine invariant (curvature; the parameter $\lambda$) being relocated between different components of a chosen representation without changing — the underlying fact never becomes more or less real depending on where you choose to display it.
- No — a spacetime with every curvature invariant vanishing everywhere is (locally) flat Minkowski space, which requires $A\equiv1$, i.e., $M=0$.

## What the paper claims here

Grounded in Sec. 6.1: "Constant-$T$ slice: $d\ell^2=dr^2+r^2d\Omega^2$ = FLAT Euclidean. Gravity encoded in mixed term $2v\,dr\,dT$ (tilts radial light cones)." The paper states this as a qualitative fact about the PG representation and does not develop an explicit intrinsic/extrinsic curvature or lapse-shift analysis — that framing above is offered as a standard, correct elaboration, flagged explicitly as going beyond the paper's own presentation. The paper does not compute curvature invariants for general $\lambda$ in this section; the claim used here (nonzero $M$ implies nonzero curvature somewhere) follows from the definition of flatness, not from a specific formula in the source.

---
**Path navigation:** ← [prev: PG1](./pg1-painleve-gullstrand.md) · [next: PG3](./pg3-newtonian-infall.md) →
**See also:** [CORE2](../part3-building-the-family/core2-log-variable-closure.md), [F7](../part1-foundations/f7-curvature.md), [EPI1](../part8-synthesis/epi1-representation-vs-fact.md)
