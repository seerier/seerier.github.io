---
title: Sim2Real Drone Racing with Deep RL (ESE 6510)
summary: A PPO-based RL pipeline in Isaac Lab that trains a Crazyflie 2.1 to fly autonomous 3-lap, 7-gate races, with zero-shot sim-to-real transfer.
tags:
  - Reinforcement Learning
  - Robotics
  - Python
date: '2026-04-01'
external_link: ''

# Featured image
image:
  caption: 'Real-world power loop trajectory through a multi-gate track'
  focal_point: Smart
  filename: featured.png
  preview_only: true

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Drone-Racing
---

{{< video src="powerloop.mp4" controls="yes" >}}

{{< video src="circlereal.mp4" controls="yes" >}}

{{< video src="bestcircle.mp4" controls="yes" >}}

{{< video src="horizontal.mp4" controls="yes" >}}

Trained a Crazyflie 2.1 quadrotor to autonomously race a 7-gate 3D track at high speed using PPO in NVIDIA Isaac Lab, with 8,192 parallel environments on a single GPU.

Key technical contributions:
- PPO pipeline with a 36D body-frame observation (velocity, rotation matrix, gate corners) and a 10-term reward function shaping progress, attitude, and gate traversal.
- Zero-shot sim-to-real transfer via dynamics domain randomization (thrust-to-weight, drag, PID gains) and three iteration-conditioned curricula (approach distance, DR magnitude, speed reward weighting).
- Completed 3 laps in 20 s on a real Crazyflie 2.1, matching simulation behavior without on-hardware fine-tuning.
