---
title: Generalisation of the Menegozzi and Lamb maser algorithm to the transient superradiance regime
slug: menegozzi-lamb-superradiance
authors: C. M. Wyenberg, B. Lankhaar, F. Rajabi, M. A. Chamma, M. Houde
journal: Monthly Notices of the Royal Astronomical Society
year: 2021
date: 2021-08-01
volume: "507"
pages: "4464-4480"
doi: 10.1093/mnras/stab2222
arxiv: "2108.01164"
ads: https://ui.adsabs.harvard.edu/abs/2021MNRAS.507.4464W
summary: The gold-standard maser-modelling algorithm is rigorous, but assumes a quasi-steady state and is expensive to run. Here is the generalisation that extends it — with the same rigor, and a manageable cost — into the transient superradiance regime.
---

## In one sentence

We extend the venerable Menegozzi & Lamb algorithm — the most rigorous formulation of maser radiative transfer there is, though notoriously expensive to run — to the regime of *transient superradiance*, the bright, fast bursts of coherent emission that ordinary maser theory cannot describe.

## What's the question?

The most rigorous treatment of maser radiative transfer — Menegozzi & Lamb (1978) — solves the underlying Maxwell-Bloch equations in a quasi-steady-state limit. It is the gold standard against which simpler maser codes are usually checked. But the quasi-steady assumption fundamentally rules out *transient* phenomena: sudden flares, sub-second bursts, possibly even some fast radio bursts. In those events the maser switches on faster than the populations can equilibrate, entering R. H. Dicke's *superradiance* regime where the molecules emit cooperatively — and the standard formulation cannot describe that.

## What did we do?

We worked from the underlying Maxwell-Bloch equations and reordered the operations — performing the velocity-distribution integration *before* moving to the Fourier representation, rather than after. The result is an Integral-Fourier algorithm that converges in the transient superradiance regime at all field strengths, with computational cost scaling linearly in the number of velocity channels, and that reduces to the original Menegozzi & Lamb algorithm in the quasi-steady limit — a strict generalisation that keeps M&L's rigor without paying the runaway price of a naïve extension. We benchmarked the framework against simulations of transient superradiance.

## Why does it matter?

If transient superradiance is at play in observed maser flares, this is the framework needed to model them quantitatively. The same code can also be used to ask: which observed flares are genuinely superradiant, and which are simply rapid quasi-steady evolution?

## My role

Co-author. Contributed to the theoretical framework and to the development of the algorithm.
