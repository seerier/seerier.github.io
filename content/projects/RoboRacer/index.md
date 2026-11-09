---
title: RoboRacer Autonomous Racing (ESE 6150)
summary: 'Autonomous racing on a 1/10-scale car: pure pursuit for Race 1, a Frenet sampling planner with MPC around moving obstacles for Race 2, plus RRT* motion planning and MPC.'
tags:
  - Robotics
  - Autonomous Racing
date: '2026-11-04'
weight: 6
external_link: ''

# Featured image
image:
  caption: 'The car on the Race 1 track'
  focal_point: Smart
  filename: featured.jpg
  preview_only: true

url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''
---

Autonomous racing on a 1/10-scale car with a LiDAR and an onboard Jetson, in ROS 2, from a pure pursuit time trial to racing around moving obstacles.

## Race 2: racing around moving obstacles

{{< video src="race2.mp4" controls="yes" muted="yes" >}}

We raced a Frenet sampling planner with MPC tracking, localized by a particle filter, on a track where staff moved suitcases and boxes while the car was running. The car held steady 10.5 s laps through the obstacles for the full five-minute race.

- System identification from the race logs: about 0.25 s actuation delay, a 5-8 % odometry scale error and a 4.3 m/s² lateral grip limit.
- Traced the obstacle contacts in turns to a planner safety margin (7.5 cm) smaller than the car's real tracking error (about 0.2 m), and built a closed-loop simulation of the real planner node to test fixes.

## Race 1: pure pursuit

{{< video src="race1.mp4" controls="yes" muted="yes" >}}

Pure pursuit with a speed-dependent lookahead on a particle-filter pose. A minimum-curvature racing line cut the lap from about 10.2 s on the centerline to 9.4 s on the car. In the race we ran 8.55 s and 9.14 s laps, 4th of 14 teams by average.

## Motion planning with RRT*

{{< video src="rrtstar.mp4" controls="yes" >}}

An RRT* local planner that builds a clearance grid from every LiDAR scan, grows and rewires a tree toward the global path, and tracks the result. In simulation it clears the obstacle course on the Levine map in about 32 s at up to 3 m/s with no contact.

## Model predictive control

{{< video src="mpc.mp4" controls="yes" >}}

A linear MPC (CVXPY + OSQP) with a 0.8 s horizon on a kinematic bicycle model linearized about the path, following a minimum-curvature path from an offline QP that keeps 0.5 m from the walls. In simulation it laps Levine in 13.2-13.4 s with no wall contact, even with a noisy, delayed pose, and delay compensation cut the tracking error from 0.10 m to 0.01 m.
