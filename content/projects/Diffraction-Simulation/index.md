---
title: Diffraction Simulation
summary: A wave optics simulation framework integrating Fraunhofer diffraction into Monte-Carlo ray tracing.
tags:
  - Computer Graphics
  - Optics
  - C++
date: '2024-07-21'

# Featured image
image:
  caption: 'Diffraction Pattern Simulation'
  focal_point: Smart
  filename: featured.png

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Diffraction-Simulation
---

A wave-optical rendering framework built on [PBRT-v3](https://github.com/mmp/pbrt-v3), implementing the [Free-Space Diffraction BSDF](https://dl.acm.org/doi/10.1145/3658166) from Steinberg et al. (SIGGRAPH 2024). It extends Monte Carlo path tracing with physically accurate diffraction effects that geometric optics cannot capture.

- Derived a closed-form edge-based Fraunhofer diffraction formulation, enabling free-space diffraction in path tracing without phase-carrying rays.
- Supports monochromatic, RGB tricolor (465/530/630 nm), and full continuous spectral rendering for comparing wavelength discretization effects on diffraction patterns.