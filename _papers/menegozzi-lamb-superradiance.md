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
summary: The standard maser-modelling algorithm breaks down for sudden, intense bursts of coherent emission — here is the generalisation that handles transient superradiance correctly.
---

## In one sentence

We extend the venerable Menegozzi & Lamb algorithm — the workhorse approach to maser modelling for half a century — to the regime of *transient superradiance*, the bright, fast bursts of coherent emission that ordinary maser theory cannot describe.

## What's the question?

Most astrophysical maser modelling assumes the maser sits in a quasi-steady state: pump, gain, propagate, repeat. The Menegozzi & Lamb (1978) algorithm encodes that assumption efficiently and is the de-facto standard tool. But some of the most interesting observed maser phenomena — sudden flares, sub-second bursts, possibly even some fast radio bursts — are *transient*: the maser switches on faster than the populations can equilibrate, entering R. H. Dicke's *superradiance* regime where the molecules emit cooperatively. The standard algorithm fundamentally cannot describe that.

## What did we do?

We worked from the underlying Maxwell-Bloch equations, performing the velocity-distribution integration *before* moving to the Fourier representation. The result is an Integral-Fourier algorithm that converges in the transient superradiance regime at all field strengths — a strict generalisation of Menegozzi & Lamb that reduces to it in the quasi-steady limit. We benchmarked the framework against simulations of transient superradiance.

## Why does it matter?

If transient superradiance is at play in observed maser flares, this is the framework needed to model them quantitatively. The same code can also be used to ask: which observed flares are genuinely superradiant, and which are simply rapid quasi-steady evolution?

## My role

Co-author. Contributed to the theoretical framework and to the development of the algorithm.
