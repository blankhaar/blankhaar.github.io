---
layout: page
title: Research
subtitle: Cosmic magnetic fields, molecular spectroscopy, and the questions I keep coming back to.
permalink: /research/
---

## What I work on

My research is built around a simple idea: the detailed physics of molecules — how they rotate, vibrate, polarize, and emit light — can reveal how the largest structures in the Universe form and evolve. A molecule in a planet-forming disk, in the wind of an evolved star, as a very-small dust grain drifting through a diffuse cloud, even one close to the supermassive black hole of another galaxy, is a precision instrument. My work builds, calibrates, and uses those molecular instruments.

In practice that gets you a broader portfolio than it might sound. Much of my work circles cosmic magnetism — how magnetic fields organise the [formation of stars and planets]({{ '/papers/tw-hya-magnetic-field/' | relative_url }}), how they shape the [gas flows in and out of the most extreme galactic nuclei]({{ '/papers/zw049-oh-megamaser-fountain/' | relative_url }}), how they help launch and shape the [winds and outflows of evolved stars]({{ '/papers/agb-envelopes-line-polarization/' | relative_url }}), and how the very [smallest dust grains polarize the radiation they emit]({{ '/papers/dust-grain-quantum-alignment/' | relative_url }}). But I also venture into corners of physics and chemistry that look much further afield: the [fundamental quantum theory of how light propagates through a dense gas of molecules]({{ '/papers/many-body-radiative-transfer/' | relative_url }}), or the [origins and asymmetry of chiral organic molecules in interstellar space](https://doi.org/10.1051/0004-6361/202244295). Across these very different problems, the question I keep asking is the same: how precisely can one do the underlying molecular physics, and what does that precision buy us?

Over the course of these projects, I have developed two open-source codes — [PORTAL and CHAMP]({{ '/code/' | relative_url }}) — both for the polarized radiative transfer of molecular and atomic spectral lines, and both used in much of my own work.

What follows is a more personal map of the questions I keep returning to.

## Magnetic fields in star formation and protoplanetary disks

<figure class="paper-figure">
  <img src="{{ '/assets/img/papers/twhya-artwork.jpg' | relative_url }}" alt="Artist's impression of magnetic field lines threading the TW Hya protoplanetary disk">
  <figcaption>Artist's impression of the magnetic field threading TW Hya's planet-forming disk — its morphology changing as it crosses gaps and rings. Credit: NSF / AUI / NSF NRAO / M. Weiss, accompanying <a href="{{ '/papers/tw-hya-magnetic-field/' | relative_url }}">Teague, Lankhaar et al. (2025)</a>.</figcaption>
</figure>

Stars form inside cold, magnetised clouds of gas, and the planets that follow form in the disks left over after the star itself has finished assembling. Magnetic fields thread this entire chain — clouds, collapsing cores, disks — and theory has long argued that they decide where gas can go, how fast it can fall in, and ultimately where matter accumulates into stars and planets. The question is not really *whether* magnetic fields matter; it is *how*, and *how much*, at each stage along the way.

The honest answer is that we still struggle to measure them. The fields are weak, the gas they thread is often faint, and most of our standard observational tools give us only indirect or statistical glimpses. What I am most interested in is using the **polarization of spectral lines** to do better. When light from atoms or molecules in a magnetised gas is observed carefully, its polarization carries quantitative information about both the *strength* and the *geometry* of the field — and unlike most other diagnostics, it does so for each line and each region of the source, exactly where the gas of interest sits.

Line polarization has historically been a niche tool, partly because the underlying physics is subtle and the signals are small. A lot of my work has gone into making it a reliable everyday diagnostic. Methanol masers, for instance, light up brilliantly toward high-mass star-forming regions and had been used as magnetic-field tracers for over a decade — but only loosely, because the molecular quantum mechanics underpinning their polarization had never been pinned down. In a [*Nature Astronomy* paper](https://doi.org/10.1038/s41550-017-0341-8) ([press coverage](https://www.sciencedaily.com/releases/2018/01/180129110919.htm), [popular-science video](https://www.youtube.com/watch?v=2X2d5ZbTdIY)), I worked out methanol's Zeeman effect from first principles and turned a decade of circular-polarization observations into proper field measurements. More recently, the [TW Hya magnetic-field measurement]({{ '/papers/tw-hya-magnetic-field/' | relative_url }}) carries the same logic into the much fainter regime of a planet-forming disk — a different molecule (CN), a different physical effect (line broadening rather than circular polarization), but the same goal.

I am convinced that this is the route by which we will eventually be able to *map*, rather than merely guess at, the magnetic fields that shape how stars and planets come into being.

## Nuclear dynamics of extreme galaxies

<figure class="paper-figure">
  <img src="{{ '/assets/img/papers/zw049-fountain-cartoon.png' | relative_url }}" alt="Cartoon of the two-component nuclear outflow in Zw049.057">
  <figcaption>The nuclear region of Zw049.057: a fast collimated outflow (red/blue arrows) sheathed in a slower, wide-angle "fountain" (teal cones), traced by OH and formaldehyde megamasers and a large-scale radio jet. Figure from <a href="{{ '/papers/zw049-oh-megamaser-fountain/' | relative_url }}">Lankhaar et al. (2024)</a>.</figcaption>
</figure>

Cosmically speaking, we live in a rather boring epoch of the Universe's history. Had we been observing the sky some 10 billion years ago — during an era known as *Cosmic Noon* — we would have seen it glowing brightly, especially in the infrared, as colliding galaxies triggered prodigious episodes of star formation.

The best present-day analogues of these Cosmic Noon systems are the luminous and ultraluminous infrared galaxies (LIRGs and ULIRGs). These nearby — though still tens of megaparsecs away — and often interacting galaxy systems offer a unique laboratory to study, in remarkable detail, how galaxies evolve under extreme conditions, how gas is transported to their nuclei, and how violent interactions shape their future.

Since the advent of ALMA, we have been able to probe these galaxies with unprecedented spatial and spectral resolution. Almost all of them reveal intricate and sometimes spectacular gas flows into and out of their nuclear regions (check out [this one]({{ '/papers/zw049-oh-megamaser-fountain/' | relative_url }})). I am convinced that magnetic fields are deeply involved in shaping these flows, and I am investigating ways to prove it.

## Fundamentals of radiative transfer

<figure class="paper-figure">
  <img src="{{ '/assets/img/papers/manybody-schematic.png' | relative_url }}" alt="Schematic of many-body radiative transfer: photons interacting with a cloud of molecules over a coherence length">
  <figcaption>Photons traversing a molecular gas: when the time between successive photon interactions is shorter than a molecule's lifetime, the relevant unit is no longer a single molecule but a coherent volume of length ℓ<sub>coh</sub>. Figure from <a href="https://arxiv.org/abs/2505.03888">Lankhaar (2025)</a>.</figcaption>
</figure>

The canonical picture of spectral-line radiative transfer rests on the three processes introduced by Einstein: absorption, stimulated emission, and spontaneous emission. Together, these form the basis of the classical radiative transfer equation, which reduces to Beer's law in the limit of pure absorption and, with the inclusion of emissivity, becomes the standard equation used throughout astronomy.

In [Lankhaar 2025](https://arxiv.org/abs/2505.03888), I challenge a central assumption underlying this canonical formulation: that the interaction between radiation and matter can be represented as a simple sum of independent photon–molecule (or photon–atom) interactions — that the whole equals the sum of its parts. I argue instead that when the time between successive photon interactions with a molecular gas becomes shorter than the relevant molecular lifetimes, this approximation breaks down. In that regime, the radiative transfer problem becomes intrinsically *many-body* in nature, requiring a fundamentally different description: a [many-body radiative transfer equation](https://arxiv.org/abs/2505.03888) which I derive there.

In most astrophysical environments, molecular and atomic lifetimes are short compared to the time between photon interactions, and the classical radiative transfer equation remains an excellent approximation. However, for a number of key spectral lines in the interstellar medium, in stellar atmospheres, and in planetary atmospheres (including the Earth's), photons no longer interact with matter one molecule at a time. Instead, I maintain that they probe a collective, many-body medium — a regime where the classical equation begins to fail and must be replaced by a more complete description.
