---
title: "Characterizing maser polarization: effects of saturation, anisotropic pumping and hyperfine structure"
slug: champ-maser-polarization
authors: B. Lankhaar, W. Vlemmings
journal: Astronomy & Astrophysics
year: 2019
date: 2019-08-01
volume: "628"
pages: A14
doi: 10.1051/0004-6361/201935064
arxiv: "1905.04868"
ads: https://ui.adsabs.harvard.edu/abs/2019A%26A...628A..14L
code: https://github.com/blankhaar/CHAMP
summary: A general code for the polarization of cosmic masers — the first to handle arbitrary saturation, hyperfine structure, and the non-Zeeman polarization signatures that confuse simpler models.
---

## In one sentence

I introduce **CHAMP**, the first code that solves polarized maser radiative transfer with arbitrary saturation, full hyperfine structure of the maser transition, and non-Zeeman polarization mechanisms — answering long-standing questions about how much of an observed maser polarization signal really comes from the magnetic field.

## What's the question?

Cosmic masers — natural radio amplifiers in molecules like SiO, H₂O, and methanol — are often strongly polarized. The polarization is nominally a probe of the magnetic field via the Zeeman effect, but the actual signal that reaches a telescope is shaped by an entanglement of effects: how saturated the maser is, the hyperfine structure of the transition, and various non-Zeeman polarization mechanisms (anisotropic pumping, polarized seed radiation). Earlier maser-polarization codes handled some of these but not all, and certainly not all together.

## What did we do?

I built CHAMP — *CHAracterizes Maser Polarization* — a 1-D radiative-transfer solver that handles all of the above in one self-consistent calculation. Applied to SiO and water masers, it reveals which features of an observed polarization spectrum are diagnostic of the magnetic field and which are diagnostic of pumping geometry, transition saturation, or hyperfine structure.

## Why does it matter?

CHAMP is the working tool with which my later maser papers actually do their physics, and it is open-source so that other groups can use it on their own data. It also clarifies, paper-by-paper, how cleanly a given maser observation can be turned into a magnetic-field measurement.

## My role

First author. Designed the algorithm, wrote the code, ran the simulations, and wrote the paper. CHAMP is open-source — see [Code]({{ '/code/' | relative_url }}).
