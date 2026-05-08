---
layout: page
title: On my mind
subtitle: Long-running research threads — questions and projects I keep returning to, even when they are not yet papers.
permalink: /on-my-mind/
---

Not everything I work on shows up in the publication list. Some questions are slow-burning, some are collaborative, some are still half-formed. This page is where I keep track of those threads.

## Fundamentals of radiative transfer

The canonical picture of spectral-line radiative transfer rests on the three processes introduced by Einstein: absorption, stimulated emission, and spontaneous emission. Together, these form the basis of the classical radiative transfer equation, which reduces to Beer's law in the limit of pure absorption and, with the inclusion of emissivity, becomes the standard equation used throughout astronomy.

In [Lankhaar 2025](https://arxiv.org/abs/2505.03888), I challenge a central assumption underlying this canonical formulation: that the interaction between radiation and matter can be represented as a simple sum of independent photon–molecule (or photon–atom) interactions — that the whole equals the sum of its parts. I argue instead that when the time between successive photon interactions with a molecular gas becomes shorter than the relevant molecular lifetimes, this approximation breaks down. In that regime, the radiative transfer problem becomes intrinsically *many-body* in nature, requiring a fundamentally different description: a [many-body radiative transfer equation](https://arxiv.org/abs/2505.03888) which I derive there.

In most astrophysical environments, molecular and atomic lifetimes are short compared to the time between photon interactions, and the classical radiative transfer equation remains an excellent approximation. However, for a number of key spectral lines in the interstellar medium, in stellar atmospheres, and in planetary atmospheres (including the Earth's), photons no longer interact with matter one molecule at a time. Instead, I maintain that they probe a collective, many-body medium — a regime where the classical equation begins to fail and must be replaced by a more complete description.

## Magnetic fields in star formation and protoplanetary disks

Stars form inside cold, magnetised clouds of gas, and the planets that follow form in the disks left over after the star itself has finished assembling. Magnetic fields thread this entire chain — clouds, collapsing cores, disks — and theory has long argued that they decide where gas can go, how fast it can fall in, and ultimately where matter accumulates into stars and planets. The question is not really *whether* magnetic fields matter; it is *how*, and *how much*, at each stage along the way.

The honest answer is that we still struggle to measure them. The fields are weak, the gas they thread is often faint, and most of our standard observational tools give us only indirect or statistical glimpses. What I am most interested in is using the **polarization of spectral lines** to do better. When light from atoms or molecules in a magnetised gas is observed carefully, its polarization carries quantitative information about both the *strength* and the *geometry* of the field — and unlike most other diagnostics, it does so for each line and each region of the source, exactly where the gas of interest sits.

Line polarization has historically been a niche tool, partly because the underlying physics is subtle and the signals are small. A lot of my work has gone into making it a reliable everyday diagnostic — see, for instance, the [TW Hya magnetic-field measurement]({{ '/papers/tw-hya-magnetic-field/' | relative_url }}) — and into applying it to the open questions of star and planet formation. I am convinced that this is the route by which we will eventually be able to *map*, rather than merely guess at, the magnetic fields that shape how stars and planets come into being.

## Nuclear dynamics of extreme galaxies

Cosmically speaking, we live in a rather boring epoch of the Universe's history. Had we been observing the sky some 10 billion years ago — during an era known as *Cosmic Noon* — we would have seen it glowing brightly, especially in the infrared, as colliding galaxies triggered prodigious episodes of star formation.

The best present-day analogues of these Cosmic Noon systems are the luminous and ultraluminous infrared galaxies (LIRGs and ULIRGs). These nearby — though still tens of megaparsecs away — and often interacting galaxy systems offer a unique laboratory to study, in remarkable detail, how galaxies evolve under extreme conditions, how gas is transported to their nuclei, and how violent interactions shape their future.

Since the advent of ALMA, we have been able to probe these galaxies with unprecedented spatial and spectral resolution. Almost all of them reveal intricate and sometimes spectacular gas flows into and out of their nuclear regions (check out [this one]({{ '/papers/zw049-oh-megamaser-fountain/' | relative_url }})). I am convinced that magnetic fields are deeply involved in shaping these flows, and I am building a research program to prove it.
