---
title: Character-Animation-System
summary: A Character animation system integrated FK/IK solver.
tags:
  - Character Animation
  - Motion Capture
  - C++
date: '2025-11-11'
external_link: ''

# Featured image
image:
  caption: 'GUI of the FK/IK System'
  focal_point: Smart
  filename: featured.png

url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''
---

Below is the demonstration of the Forward Kinematics (FK) system using motion capture data:
![FK Dance](FK-Dance.png)

For the Inverse Kinematics (IK) part, I implemented a Jacobian-based solver to control the end-effector:
{{< figure src="IK.png" caption="Inverse Kinematics Demo" >}}