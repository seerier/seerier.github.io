---
title: Drone Racing with Deep Reinforcement Learning
summary: A PPO-based deep RL pipeline in Isaac Lab to train a Crazyflie quadrotor for autonomous multi-gate 3D drone racing.
tags:
  - Reinforcement Learning
  - Robotics
  - Python
date: '2026-04-01'
external_link: ''

# Featured image
image:
  caption: 'Drone Racing Simulation in Isaac Lab'
  focal_point: Smart
  filename: featured.png
  preview_only: true

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Drone-Racing
---

{{< video src="horizontal.mp4" controls="yes" >}}

Trained a quadrotor to autonomously race a multi-gate 3D track at high speed using PPO in NVIDIA Isaac Lab, with massively parallel simulation on a single GPU.

Key technical contributions:
- Asymmetric actor-critic architecture with multi-component reward shaping and curriculum learning for progressive skill acquisition from basic flight to aggressive racing.
- Domain randomization over physical dynamics parameters with independent curriculum scheduling to improve policy robustness, designed for future sim-to-real transfer.
