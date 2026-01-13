---
title: Monte-Carlo Rendering Engine
summary: A multithreaded C++ ray tracing engine for physically-based rendering
tags:
  - Computer Graphics
  - C++
  - Rendering
date: '2023-12-01'
external_link: ''

# Featured image
image:
  caption: 'Cornell Box'
  focal_point: Smart
  filename: featured.png  # 放在同目录下

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Xeno
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''
---

• Developed ahigh-performance simulation engine in C++ to solve high-dimensional light transport
equations via Monte-Carlo integration.
• Utilized variance reduction techniques including Importance Sampling and Multiple Importance
Sampling (MIS) to optimize convergence rates.
• ImplementedadvancedalgorithmsincludingPathTracing, BidirectionalPathTracing(BDPT),and
Stochastic Progressive Photon Mapping (SPPM) for complex global illumination.
• Optimized performance via multi-threaded ray tracing, BVH acceleration structures, and arena
based memory allocation for large-scale rendering.