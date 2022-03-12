---
permalink: /worlds
layout: page
title: Worlds
---

# World Generation with Simplex Noise
---
We used [Simplex Noise](https://en.wikipedia.org/wiki/Simplex_noise) to generate a wide variety of challenging worlds for our robots.
Like its predecessor Perlin noise, Simplex noise is a gradient noise and used as a procedural texture to increase the realism in computer graphics.
It is, for example, used in computer games to produce always new worlds. 
One can overlay different noise scales to create variety on different resolution levels (elevation: continents/mountain range/hill).

In our case, we used a binary occupancy grid for the environments of our robots. 
To get from a continuous noise to a binary occupancy grid, we applied a threshold to decide which regions are not passable for the robot.

---
# Parameters of Simplex Noise

|                                           Noise                                            |                                         Occupancy Grid                                         |
|:------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------:|
| ![](../assets/imgs/worlds/worlds_simplex_noise.png){:.some-css-class style="width: 500px"} | ![](../assets/imgs/worlds/worlds_simplex_threshold.gif){:.some-css-class style="width: 490px"} |

This animation shows the influence of the threshold on the occupancy map, from a free plane to completely occupied.



![Worlds 2D Resolution](../assets/imgs/worlds/worlds_simplex_resolution.png)


---
# 2D Examples
![Worlds 2D Examples](../assets/imgs/worlds/worlds_examples_2d.png)
Here you can see different examples of 2D worlds all with the same noise level and threshold.

---
# 3D Examples
![Worlds 3D Examples](../assets/imgs/worlds/worlds_examples_3d.gif)
The same procedure can be applied in higher dimensions, and we use it to generate those asteroid field for our robots.


---