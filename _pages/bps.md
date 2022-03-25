---
permalink: /bps
layout: page
title: BPS
---

Here we discuss the basis point set [[Prokudin2019](https://arxiv.org/abs/1908.09186)] as an environment representation 
for motion planning.
It is a memory and computation efficient representation of spatial information.
But because until now, its application mainly was to computer graphics with a focus on visual results, we looked at the maximal error this encoding can make when using it as the basis for collision avoidance.
We compared it to other common representations and found that it is well suited to represent the binary environment in which the robots should move. 

---

The basis point set is strongly connected to a distance field. 
Each point in the set measures the distance to the closest obstacle in the environment. 
If the points lie on a regular grid this encoding is identical to a distance field.

|                                 Basis Points                                  |                                         Closest Obstacles                                         |                                          Conclusion to Area                                           |
|:-----------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------:|
| ![BPS - Build](../assets/imgs/bps/bps_build.gif){:.this style="width: 400px"} | ![BPS - Distances Lines](../assets/imgs/bps/bps_distances_lines.gif){:.this style="width: 400px"} | ![BPS - Distances Circles](../assets/imgs/bps/bps_distances_circles.gif){:.this style="width: 400px"} | 

*Here you can see the closest obstacle for all basis points and the conclusion on can draw from this for the free (blue) and occupied space (red).*

---

There are different options to choose the basis points. 
The random set worked best for [[Prokudin2019](https://arxiv.org/abs/1908.09186)] but for our use case we prefer a more conservative choice.
For a regular grid or a hexagonal closed pack (HCP) grid one can estimate the maximal error better.

|        |                                   Box                                    |                                    Sphere                                    |
|:------:|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
|  Grid  | ![](../assets/imgs/bps/bps_box-uniform.jpg){:.this style="width: 500px"} | ![](../assets/imgs/bps/bps_ellipse-uniform.jpg){:.this style="width: 500px"} | 
|  HCP   |   ![](../assets/imgs/bps/bps_box-hcp.jpg){:.this style="width: 500px"}   |   ![](../assets/imgs/bps/bps_ellipse-hcp.jpg){:.this style="width: 500px"}   |
| Random | ![](../assets/imgs/bps/bps_box-random.jpg){:.this style="width: 500px"}  | ![](../assets/imgs/bps/bps_ellipse-random.jpg){:.this style="width: 500px"}  | 


---

We use the basis point set to encode the environment and feed it to a neural network.
But, there are other choices.
The underlying ground truth from the data we generated is a 64x64 occupancy grid and the optimization-based motion planner uses the signed distance field to compute collision free paths.

**Occupancy Grid**
![occupancy grid](../assets/imgs/bps/bps_occ.png){:.this 
style="width: 750px; 
display: block;
margin-left: auto;
margin-right: auto"}

**Signed Distance Field**
![signed distance field](../assets/imgs/bps/bps_sdf.png){:.this 
style="width: 750px; 
display: block;
margin-left: auto;
margin-right: auto"}

**Accuracy of Basis Point Set compared to a down-sampled Occupancy Grid**
![basis set](../assets/imgs/bps/bps_vs_occ.jpg){:.this 
style="width: 750px; 
display: block;
margin-left: auto;
margin-right: auto"}

