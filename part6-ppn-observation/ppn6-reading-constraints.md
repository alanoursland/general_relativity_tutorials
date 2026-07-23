# From $\beta$ to $\lambda$: Reading Constraints Critically

> **Tutorial `PPN6`** · Part 6 · **Goal:** Read the real observational bounds on $\beta$ honestly — what they measure directly, what extra assumption they borrow, and what that licenses us to say about $\lambda$ · **Prereqs:** [PPN5](./ppn5-perihelion-precession.md)

**Where this sits in the arc.** `PPN3` gave the exact identity $\lambda=\beta-2$; `PPN5` showed that even a rough number for the observed precession is enough to rule out most of the family. This tutorial does the more careful thing: it looks at the actual quoted solar-system bounds on $\beta-1$, states exactly what assumption is needed to read them as bounds on $\beta$ *alone*, and draws only the conclusion those assumptions actually support. This is the book's recurring discipline — quote a bound with its scope, never past it.

## The number we actually want

Since $\lambda=\beta-2$, we have $\lambda+1=\beta-1$: constraining how far $\beta$ sits from GR's value of $1$ is *exactly* constraining how far $\lambda$ sits from Schwarzschild's value of $-1$. So the quantity to track is $\beta-1$ (equivalently $\lambda+1$), and the question is how tightly the solar system pins it down.

## The quoted bounds

Two independent analyses of solar-system data report:

- **Lunar Laser Ranging (LLR) + Cassini** (Williams, Turyshev, Boggs 2004): $\beta-1 = (1.2\pm1.1)\times10^{-4}$.
- **INPOP20a** (Fienga et al. 2022), a planetary ephemeris fit: $|\beta-1|\lesssim7.2\times10^{-5}$, described as a *conservative acceptance bound*.

Both are consistent with $\beta=1$ (Schwarzschild's value) to within their stated uncertainty, and both put $|\beta-1|$ at the level of $10^{-4}$ or smaller.

## What these bounds do and don't assume

It would be tempting to read $\beta-1=(1.2\pm1.1)\times10^{-4}$ as a direct, clean measurement of the single number $\beta$ in isolation. It is not, quite. Lunar laser ranging measures the *Nordtvedt effect* — whether the Earth and Moon, with different gravitational self-energy fractions, fall toward the Sun at slightly different rates — which is sensitive to a *combination* of PPN parameters, conventionally written
$$\eta_N = 4\beta - \gamma - 3.$$
Extracting a bound on $\beta$ alone from a measured $\eta_N$ requires either an independent measurement of $\gamma$ (available from light-bending/Shapiro-delay experiments, which as `PPN4` showed are excellent at pinning down $\gamma$ near $1$) or an assumption that other PPN parameters this relation implicitly sets to zero really are zero. That is a *restricted* PPN framework — one in which effects like preferred-frame violations are assumed absent — layered on top of the bare $\gamma,\beta$ language this book has developed for a single static spherical exterior.

This matters here specifically because the family constructed in Part III is a *one-body, static* construction: it has exactly two PPN-relevant numbers, $\gamma$ and $\beta$, and nothing to say about the multi-body, many-parameter PPN sector that $\eta_N=4\beta-\gamma-3$ belongs to. Borrowing the LLR+Cassini number to constrain *our* $\lambda$ means implicitly trusting that the wider PPN framework's restriction (other parameters vanish) holds — a piece of physics genuinely outside anything (I1)–(I4) established.

The INPOP20a number carries a related, but distinct, honesty flag: it is explicitly labeled a *conservative acceptance bound*, not a symmetric confidence interval from a single well-defined statistical model. An acceptance bound answers "how far from GR could $\beta$ be and still not conflict, at some agreed conservative standard, with the ephemeris fit" — a somewhat different statement than "here is our best-fit value and its 1-$\sigma$ uncertainty." Treating $7.2\times10^{-5}$ as if it carried the same statistical meaning as a Gaussian confidence interval would overstate what the number claims.

## Reading it at the honest level: order of magnitude

None of this means the bounds are useless — it means they should be used for what they reliably establish: an *order of magnitude*. Both independent analyses, despite resting on somewhat different assumptions and reporting somewhat different kinds of numbers, agree that
$$|\lambda+1| = |\beta-1| \lesssim 10^{-4}.$$
That is a real, solid conclusion, robust to the details above precisely because it only asks for the *scale* of the deviation, not its exact value or its precise statistical character. At this level of honesty:
$$\lambda \simeq -1,$$
Schwarzschild is selected to a precision no other selector in this book comes close to — Part V's accounting argument could only narrow $\lambda$ to a coarse interval that (per `PPN5`) turned out to be on the wrong side of the data entirely; PPN observation narrows it to four decimal places' worth of agreement with $-1$.

## Simpler on-ramp

Imagine two independent groups each report "the dial reads within $0.0001$ of zero," but one group's dial is calibrated using an assumption you haven't independently checked (here, that a certain combination of *other* unrelated dials all read exactly zero too), and the other group's number is phrased as "we're confident it's not further than this," rather than "here's our precise reading plus honest error bars." Both statements are still telling you something real and useful — the needle is very close to zero — but neither entitles you to claim you know the fifth decimal place, or that you've ruled out every alternative explanation with statistical rigor. The right thing to say, and the thing this tutorial insists on, is the modest one: the needle is close to zero, at the level of one part in ten thousand or so, and that's already enough to make $\lambda=-1$ overwhelmingly the best candidate — just don't claim more precision or more certainty than the assumptions underneath the number actually deliver.

## Check your understanding

- Why can't lunar laser ranging alone hand you $\beta$ without an extra assumption?
- What exactly is the difference between a "confidence interval" and a "conservative acceptance bound," and why does it matter here?
- Why does the paper insist on using these numbers only "for order of magnitude," rather than quoting them to full stated precision?
- Does this tutorial's conclusion ($\lambda\simeq-1$) depend on trusting the $\eta_N=4\beta-\gamma-3$ assumption? Why or why not?

**Answers**
- Because LLR directly measures the Nordtvedt effect, a combination $\eta_N=4\beta-\gamma-3$ of PPN parameters, not $\beta$ in isolation; isolating $\beta$ requires either an independent $\gamma$ measurement plus trust in that specific linear relation, or an assumption that other PPN parameters in the fuller multi-body framework vanish.
- A confidence interval reports a best-fit value with a probabilistic uncertainty from a specified statistical model; an acceptance bound reports a threshold beyond which the fit is judged unacceptable by some conservative standard, without necessarily being a symmetric probabilistic statement — treating the two interchangeably risks overstating the acceptance bound's precision.
- Because both quoted bounds carry assumptions (a restricted PPN relation for LLR; a "conservative" rather than fully probabilistic character for INPOP20a) that are reasonable but not established by the one-body static construction this book builds; only the *scale* of the numbers ($\sim10^{-4}$) is robust enough across both analyses to state with confidence.
- No — the order-of-magnitude conclusion $|\lambda+1|\lesssim10^{-4}$ is supported by *two* independent analyses with different assumptions, both landing at the same scale; even without fully trusting the $\eta_N$ relation, the qualitative conclusion "$\lambda$ is very close to $-1$, at roughly the one-part-in-ten-thousand level" is the robust content shared across both, which is exactly why the paper restricts itself to that level of claim.

## What the paper claims here

Grounded in Sec. 5.4: "$\lambda+1=\beta-1$. Solar-system: $\beta-1$ at $\sim10^{-4}$ or better. LLR+Cassini (Williams, Turyshev, Boggs 2004): $\beta-1=(1.2\pm1.1)\times10^{-4}$. INPOP20a (Fienga et al. 2022): $|\beta-1|\lesssim7.2\times10^{-5}$ (conservative acceptance bound). LLR value assumes restricted PPN relation $\eta_N=4\beta-\gamma-3$; one-body exterior here doesn't determine full many-body PPN sector. Use only for order of magnitude: $|\lambda+1|\lesssim10^{-4}$, so $\lambda\simeq-1$, Schwarzschild selected to high precision." This tutorial adds no numerical claim beyond what is quoted here, and preserves the paper's explicit caveat about the restricted-PPN assumption and the "order of magnitude only" instruction.

---
**Path navigation:** ← [prev in default path](./ppn5-perihelion-precession.md) · [next](./ppn7-beta-and-horizon.md) →
**See also:** [PPN3](./ppn3-gamma-beta.md), [ACC1](../part5-energy-accounting/acc1-circularity.md), [EPI2](../part8-synthesis/epi2-identities-not-measurements.md)
