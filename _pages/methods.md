---
permalink: /methods
layout: page
title: Methods
---

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


# Network based Iterative Dataset Generation
---

This setup, where we want to improve an existing method by replacing some parts with a neural network, allows some tricks.
Especially the objective function, which the optimizer tries to minimize, plays a central role, as it makes it possible to compare different suggestions for a given motion problem objectively.

This means that the dataset does not have to be static after its generated with the classical setup.
One can regularly check if the prediction of the network is better than the corresponding label. 
If the objective function of the prediction is lower, then this path is better and can replace the current label without adding any bias to the dataset.
Of course, for this to work, the dataset must have a certain quality, and the network must have already learned enough to make valuable predictions.
But we found that even in an early stage of training, the difference between network prediction and label is a good indicator of where to invest resources to improve the dataset.

One can continue this idea one step further and use the objective function to decide which samples have valuable information for the network and adjust the curriculum accordingly or produce new challenging samples.  
![flowchart](../assets/imgs/flowchart.png)

---
Those examples show the problem with inconsistent labels.
While more compuatational resources can solve those problems it is more efficient to use the help of the network as guidance.
Using the prediction of the network as indicator is also more general, then applying some custom heuristics to identify potential outliers.
![wrong labels](../assets/imgs/flow_wrong_labels.png)

---
* TODO add ablation study show necessity for each of those steps
