---
permalink: /dataset
layout: page
title: Dataset
---
[Click here](../dataset/measurements.csv.zip) to download the dataset.
____

The dataset contains $N=500$ measurements of the humanoid robot Agile Justin. Each data point consists of the commanded joint configuration $q$ and the corresponding positions of the left and the right end-effector $y$. 
The measurements were acquired using an external camera system from Vicon, consisting of six 16Mpx cameras mounted on the ceiling, which tracked the two retro-reflective markers on the robot’s hands. 

The sketch demonstrates the measurement setup and highlights some problems

![calibration sketch](../assets/imgs/calibration_sketch.png)

---

All positions are provided in the frame of the camera system.
Initial guesses for the base of the robot, seen from the camera system

```python
T_c_0 = [[ 0, -1,  0, -2.5], 
         [+1,  0,  0, +2.0],
         [ 0,  0, +1, +0.1],
         [ 0,  0,  0,    1]]
```

and the marker positions on the right and left arm

```python
p_r_m = [-0.1, -0.03, +0.1]
p_l_m = [-0.1, +0.03, +0.05]
```

All three frames need to be included to close the measurement loop and calibrate the forward kinematic with the provided data.

---

