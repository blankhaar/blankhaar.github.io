---
title: Maser polarization through anisotropic pumping
slug: maser-anisotropic-pumping
authors: B. Lankhaar, G. Surcis, W. Vlemmings, V. Impellizzeri
journal: Astronomy & Astrophysics
year: 2024
date: 2024-03-01
volume: "683"
pages: A117
doi: 10.1051/0004-6361/202348420
arxiv: "2401.04185"
ads: https://ui.adsabs.harvard.edu/abs/2024A%26A...683A.117L
summary: Many of the most striking polarization signatures of cosmic masers are not magnetic at all — they come from the geometry of how the maser is pumped. Here is the first comprehensive code that handles both.
---

## In one sentence

A unified maser-polarization code that — for the first time — handles anisotropic pumping (which polarizes masers all by itself, no magnetic field required), magnetic-field effects, and full saturation behaviour in a single framework.

## What's the question?

Cosmic masers — natural radio amplifiers in molecules like CH₃OH, H₂O and SiO — are often strongly polarized. For decades, that polarization was usually interpreted as a magnetic-field signature via the Zeeman effect. But masers can also be *intrinsically* polarized by their pumping geometry alone: when the radiation that excites them comes from a preferred direction, the upper level of the maser transition is aligned, and the maser emission is polarized as a result. That non-Zeeman contribution had never been modelled comprehensively *alongside* the rest of the maser physics.

## What did we do?

I combined polarization-resolved excitation modelling with full polarized maser radiative transfer and wrote a single code that does both at once. I computed anisotropic-pumping parameters for class I CH₃OH, H₂O, and SiO masers, and showed that anisotropic pumping naturally explains why SiO masers are so strongly polarized while other species are more modest. The framework also predicts a previously unrecognised mechanism for non-Zeeman *circular* polarization, generated whenever the magnetic field rotates direction along the propagation through an anisotropically pumped maser.

## Why does it matter?

A meaningful fraction of the polarization that observers attribute to magnetic fields in masers is, on this analysis, set by pumping geometry — meaning some published field strengths inferred from masers need to be revisited. More positively, the same framework gives a quantitative way to *use* the pumping geometry as its own diagnostic.

## My role

First author. Devised the method, wrote the code, performed the simulations, and wrote the paper.
