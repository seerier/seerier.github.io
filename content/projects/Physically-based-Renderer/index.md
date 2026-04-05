---
title: Physically-based Renderer
summary: A multithreaded C++ Monte Carlo renderer implementing path tracing, BDPT, and photon mapping.
tags:
  - Computer Graphics
  - C++
  - Rendering
date: '2024-11-17'
external_link: ''

# Featured image
image:
  caption: 'Cornell Box'
  focal_point: Smart
  filename: featured.png

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Xeno
---

A physically-based Monte Carlo renderer written in C++, named after the Xenoblade game series. It solves the rendering equation via multiple light transport algorithms:

- **Path Tracing** with multiple importance sampling (MIS)
- **Bidirectional Path Tracing (BDPT)** for scenes with complex indirect lighting
- **Stochastic Progressive Photon Mapping (SPPM)** for specular-diffuse-specular light paths

The renderer features multithreaded execution and JSON-based scene configuration.