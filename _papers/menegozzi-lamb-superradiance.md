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
summary: The most rigorous maser-modelling algorithm still misses the most extreme *transient superradiance* regime. Here is the generalisation that extends it — with the same rigor, and a manageable cost.
---

## In one sentence

We extend the venerable Menegozzi & Lamb algorithm — the most rigorous formulation of maser radiative transfer there is, though notoriously expensive to run — to the regime of *transient superradiance*, the bright, fast bursts of coherent emission that ordinary maser theory cannot describe.

## What's the question?

Most astrophysical maser modelling makes a *quasi-steady-state* approximation — assuming the maser populations and radiation field reach equilibrium fast compared to the timescales of interest. The Menegozzi & Lamb (1978) algorithm — originally developed for laser physics — is a notable exception: it solves the underlying Maxwell-Bloch equations rigorously, without that approximation, and is for that reason the gold standard against which simpler maser codes are usually checked. Even M&L, however, runs into a wall at the most extreme *transient* phenomena — sudden flares, sub-second bursts, possibly even some fast radio bursts — where the maser switches on faster than the populations can equilibrate and enters R. H. Dicke's *superradiance* regime, the cooperative emission of many molecules together.

## What did we do?

We worked from the underlying Maxwell-Bloch equations and reordered the operations — performing the velocity-distribution integration *before* moving to the Fourier representation, rather than after. The result is an Integral-Fourier algorithm that converges in the transient superradiance regime at all field strengths, with computational cost scaling linearly in the number of velocity channels, and that reduces to the original Menegozzi & Lamb algorithm outside the extreme-transient regime — a strict generalisation that keeps M&L's rigor while extending it into territory the original could not handle. We benchmarked the framework against simulations of transient superradiance.

## Why does it matter?

If transient superradiance is at play in observed maser flares, this is the framework needed to model them quantitatively. The same code can also be used to ask: which observed flares are genuinely superradiant, and which are simply rapid quasi-steady evolution?

## My role

Co-author. Contributed to the theoretical framework and to the development of the algorithm.
