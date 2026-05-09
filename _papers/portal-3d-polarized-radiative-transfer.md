---
title: "PORTAL: three-dimensional polarized (sub)millimeter line radiative transfer"
slug: portal-3d-polarized-radiative-transfer
authors: B. Lankhaar, W. H. T. Vlemmings
journal: Astronomy & Astrophysics
year: 2020
date: 2020-04-01
volume: "636"
pages: A14
doi: 10.1051/0004-6361/202037509
arxiv: "2003.04331"
ads: https://ui.adsabs.harvard.edu/abs/2020A%26A...636A..14L
code: https://github.com/blankhaar/PORTAL
summary: A 3-D code that turns a model cube and a magnetic-field configuration into the polarized molecular-line maps that ALMA actually observes.
---

## In one sentence

I introduce **PORTAL** — the first 3-D code for polarized molecular-line radiative transfer through arbitrary magnetic-field morphologies, designed to plug onto the back of any standard (unpolarized) astrophysical model and turn it into the Stokes Q, U, V maps an instrument like ALMA actually measures.

## What's the question?

Every astrophysically interesting region — protoplanetary disks, the envelopes of evolved stars, dense molecular clouds, the centres of galaxies — has a complex three-dimensional structure threaded by an equally complex magnetic field. To predict what a radio telescope sees, you need to follow polarized line emission as it propagates through that 3-D mess, accounting for radiative pumping, the local geometry of the field, and the way molecular alignment depends on the conditions along the ray. Until this paper, no public code did the full polarized 3-D problem.

## What did we do?

I built one. PORTAL works either standalone (in LTE) or — more usefully — as a polarization post-processor for any standard 3-D *unpolarized* radiative-transfer code: feed it a model cube of physical conditions and a magnetic-field map, and it returns synthetic polarized-line images. Two clean approximations (the strong-magnetic-field limit and the anisotropic-intensity limit) make the problem tractable while remaining valid in essentially all astrophysically relevant regimes.

## Why does it matter?

PORTAL is the bridge between theoretical models of magnetised astrophysical regions and what observers actually see at the eyepiece. It is now used to interpret line-polarization observations from ALMA and other facilities, and underpins much of my subsequent work on disk and circumstellar magnetism.

## My role

First author. Conceptualised the approximations that made the code feasible, wrote the code, and wrote the paper. PORTAL is open-source — see [Code]({{ '/code/' | relative_url }}).
