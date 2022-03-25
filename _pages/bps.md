---
permalink: /bps
layout: page
title: BPS
---

The basis point set [[Prokudin2019](https://arxiv.org/abs/1908.09186)] is strongly related to a distance field.
The only difference is, that it does not have to lay on a regular grid.
# TODO


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
![occupancy grid](../assets/imgs/bps/bps_occ.png)

---
Signed Distance Field
![signed distance field](../assets/imgs/bps/bps_sdf.png)

---
Basis Set and Comparision
![basis set](../assets/imgs/bps/bps_vs_occ.jpg)

---


---

|                                  Noise Field                                  |                                     Occupancy Grid                                     |
|:-----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
|        ![Noise](../assets/imgs/bps/bps_box-hcp.jpg){:.this style="width: 500px"}         | ![Occupancy Grid](../assets/imgs/bps/bps_box_uniform.jpg){:.this style="width: 500px"} |
 | ![Noise](../assets/imgs/bps/bps_box_uniform.jpg){:.this style="width: 500px"} |     ![Noise](../assets/imgs/bps/bps_box_uniform.jpg){:.this style="width: 500px"}      | 
