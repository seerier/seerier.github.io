---
title: Humanoid Motion Tracking on the Unitree G1
summary: An end-to-end pipeline that turns human motion, from motion capture or a single video, into physically tracked motion on the Unitree G1 humanoid in simulation.
tags:
  - Reinforcement Learning
  - Robotics
  - Python
date: '2026-10-27'
weight: 2
external_link: ''

# Featured image
image:
  caption: 'Human motion capture and the G1 policy: a cartwheel and a back handspring'
  focal_point: Smart
  filename: featured.png
  preview_only: true

links:
  - icon: github
    icon_pack: fab
    name: Source Code
    url: https://github.com/seerier/Humanoid-Motion
---

{{< video src="acrobatics.mp4" controls="yes" >}}

{{< video src="teaser.mp4" controls="yes" >}}

{{< video src="video_dance.mp4" controls="yes" >}}

{{< video src="compare.mp4" controls="yes" >}}

Built an end-to-end pipeline that turns human motion, from motion capture or a single monocular video, into physically tracked motion on the Unitree G1 humanoid: retarget it to the robot with GMR, track it with one of two physics backends, then score both with one evaluation protocol.

Key technical contributions:
- Retargeting with GMR plus per-clip audits: 77 LAFAN1 recordings are cut into 2,594 six-second windows, and 2,153 pass checks for foot penetration, IK branch flips, joint speed and torso mismatch.
- Multi-motion PPO tracking policy in Isaac Lab (BeyondMimic environment) with failure-adaptive clip and phase sampling, trained with 4,096 parallel environments. It tracks 190 of 230 held-out test clips without a failure, from a single attempt per clip.
- A second backend reproducing SuperMimic, which trains the tracking policy through a learned differentiable world model instead of with PPO, in MuJoCo Warp. Trained on the same 1,062 clips, it completes 195 of 230 test clips.
- One offline scorer for both backends that reproduces the online Isaac evaluator exactly, plus the BeyondMimic policy running sim-to-sim in MuJoCo (190 of 230) for a same-engine comparison.
- A video front end (GVHMR, a ground fix from stationary-foot labels, then GMR) whose references both trackers follow zero-shot.
- Acrobatics: 13 segments from LAFAN1 and CMU motion capture (cartwheels, a kip-up, a backward roll, a side flip, backflips, a front handspring, breakdance flips), retargeted under a floor constraint on every collision geom of the robot and trained with the BeyondMimic backend. Four are tracked to the end: a cartwheel, a kip-up, a backward roll and a back handspring.
