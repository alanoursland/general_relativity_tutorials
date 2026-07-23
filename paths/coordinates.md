# Path: Coordinates & horizons

*"The same spacetime wears many coordinates."* This path follows one thread —
how a single invariant geometry looks different depending on the chart you draw
it in, and how to tell a coordinate artifact from a real feature — from flat
space, through Schwarzschild's own coordinate pathology, through the family's
zeros, to the clearest possible definition of a horizon.

1. [`F4` — Flat space in curvilinear coordinates](../part1-foundations/f4-curvilinear-coordinates.md) — the baseline case where nothing is curved, so any weirdness you see is purely the coordinates: spherical coordinates, areal radius, $r^2d\Omega^2$.
2. [`SYM1` — Static, spherically symmetric metrics](../part1-foundations/sym1-static-spherical.md) — why symmetry forces the $-A\,c^2dt^2+B\,dr^2+r^2d\Omega^2$ form, and what "static" and "asymptotically flat" pin down precisely.
3. [`S4` — Coordinate vs. curvature singularities](../part2-schwarzschild/s4-singularities.md) — the paradigm case: $r=r_s$ is a coordinate artifact (finite curvature invariants) while $r=0$ is a real singularity, and the diagnostic that tells them apart.
4. [`ZERO1` — Finite-radius zeros and the sign of $\lambda$](../part4-family-structure/zero1-finite-radius-zeros.md) — the same $A(r)=0$ phenomenon reappears across the whole family, for every $\lambda<0$, at $r_0=-\lambda r_s$.
5. [`ZERO2` — When is a zero a horizon?](../part4-family-structure/zero2-when-is-a-zero-a-horizon.md) — applying `S4`'s diagnostic to the general family: a zero of $g_{tt}$ is necessary but never sufficient for a horizon.
6. [`PG1` — Painlevé–Gullstrand coordinates & the river model](../part7-michell-pg/pg1-painleve-gullstrand.md) — a different chart entirely: a time shift that makes the spatial slices flat, trading coordinate singularities for a mixed term.
7. [`PG2` — Where did the curvature go?](../part7-michell-pg/pg2-where-did-curvature-go.md) — the same invariant geometry, now with its curvature content carried by $2v\,dr\,dT$ instead of spatial curvature — coordinates reshuffling where the "difficulty" appears without changing what's real.
8. [`PG4` — Horizons as light-cone tipping](../part7-michell-pg/pg4-horizons-light-cones.md) — the payoff: in PG coordinates, extending smoothly through $A=0$, the horizon has a clean coordinate-independent meaning — outgoing light frozen at $v=c$ — settling what `S4` and `ZERO2` were building toward.

---
For the full derivation of the family whose zeros you met at stop 4, see the
[fast path](fast.md); for the historical payoff of the PG picture (Michell's
coincidence), continue to [`PG3`](../part7-michell-pg/pg3-newtonian-infall.md)
and the [history path](history.md).
