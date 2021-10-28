---
permalink: /methods
layout: page
title: Methods
---



# World Encoding with Fixed Basis Set
---
We adopted the idea of a fixed basis set from computer vision [[Prokudin2019](https://arxiv.org/abs/1908.09186)] and applied it to robotic motion planning.

---
![occupancy grid](../assets/imgs/worlds_occ.png)

---
![signed distance field](../assets/imgs/worlds_sdf.png)

---
![basis set](../assets/imgs/worlds_fb.png)

---

# Network based Iterative Dataset Generation
---
![flowchart](../assets/imgs/flowchart.png)


---
![wrong labels](../assets/imgs/flow_wrong_labels.png)
Those examples show the problem with inconsistent labels.
While more compuatational resources can solve those problems it is more efficient to use the help of the network as guidance.
Using the prediction of the network as indicator is also more general, then applying some custom heuristics to identify potential outliers.

---
* TODO add ablation study show necessity for each of those steps
