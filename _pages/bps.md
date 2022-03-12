---
permalink: /bps
layout: page
title: BPS
---

![BPS - Build](../assets/imgs/bps/bps_build.gif){:.this style="width: 400px"}

![BPS - Distances Lines](../assets/imgs/bps/bps_distances_lines.gif){:.this style="width: 400px"}

![BPS - Distances Circles](../assets/imgs/bps/bps_distances_circles.gif){:.this style="width: 400px"}


# World Encoding with Fixed Basis Set
---
[[Prokudin2019](https://arxiv.org/abs/1908.09186)] and applied it to robotic motion planning.
It is a memory and computation efficient representation of spatial information.
But because until now, its application mainly was to computer graphics with a focus on visual results, we looked at the maximal error this encoding can make when using it as the basis for collision avoidance.
We compared it to other common representations and found that it is well suited to represent the binary environment in which the robots should move. 

---
Occupancy Grid
![occupancy grid](../assets/imgs/worlds_occ.png)

---
Signed Distance Field
![signed distance field](../assets/imgs/worlds_sdf.png)

---
Basis Set and Comparision
![basis set](../assets/imgs/worlds_fb.png)

---