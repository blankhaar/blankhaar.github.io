---
layout: page
title: Code & software
subtitle: Open-source codes for polarized line radiative transfer.
permalink: /code/
description: >-
  Open-source codes by Boy Lankhaar — PORTAL and CHAMP for polarized
  radiative transfer of atomic and molecular spectral lines.
---

A common thread in my work is that interpreting polarization observations needs careful theory and good numerics. Below are two open-source codes I have written to do exactly that.

## PORTAL

**POlarized Radiative Transfer Adapted to Lines** — a 3D code for simulating the emergence of polarization in molecular and atomic (sub)millimetre line emission through a magnetic field of arbitrary morphology.

PORTAL can be used standalone in LTE, or as a polarization post-processor for regular (unpolarized) 3D radiative-transfer codes: you give it a model cube and a magnetic field, and it returns the Stokes Q, U, and V maps. It is designed for the kinds of objects where polarization actually carries the magnetic-field information you want — protoplanetary disks, circumstellar envelopes around evolved stars, and dense molecular clouds.

- **Code:** [github.com/blankhaar/PORTAL](https://github.com/blankhaar/PORTAL)
- **Reference paper:** Lankhaar & Vlemmings, *A&A* 636, A14 (2020) — [DOI](https://doi.org/10.1051/0004-6361/202037509) · [arXiv:2003.04331](https://arxiv.org/abs/2003.04331)

## CHAMP

**CHAracterizing Maser Polarization** — a 1D radiative-transfer solver for the polarization of astrophysical masers.

CHAMP handles the regime that classical maser-polarization theory cannot: arbitrarily high saturation, high angular momentum, and the full hyperfine multiplicity of the maser transition. It also lets you turn on non-Zeeman polarizing mechanisms — anisotropic pumping, polarized seed radiation — so you can ask how much of an observed polarization signal is really tracing the magnetic field, and how much is something else.

- **Code:** [github.com/blankhaar/CHAMP](https://github.com/blankhaar/CHAMP)
- **Reference paper:** Lankhaar & Vlemmings, *A&A* 628, A14 (2019) — [DOI](https://doi.org/10.1051/0004-6361/201935064) · [arXiv:1905.04868](https://arxiv.org/abs/1905.04868)

## Other repositories

A few smaller projects live on my [GitHub profile](https://github.com/{{ site.author.github }}) — including [`zeeman_disk`](https://github.com/blankhaar/zeeman_disk), a Zeeman ray-tracer specialised to protoplanetary disks.
