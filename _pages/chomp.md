---
permalink: /chomp
layout: page
title: OMP
usemathjax: true
---

**Path**

$$
Q = [q_1, \dots, q_{\mathrm{t}}], \, q_t \in \mathbb{R}^{N_{\mathrm{q}}}
$$

**Objective Function**

$$
U(Q) = U_c(Q) + \alpha \, U_s(Q) + \beta \, U_l(Q)
$$

**Length Cost**

$$
U_l(Q) = \frac{N_{\mathrm{t}}-1}{|q_{N_{\mathrm{t}}}-q_1|^2} \sum_{t=1}^{N_{\mathrm{t}}-1} |q_{t+1} - q_{t}|^2
$$

**Collision Cost**

$$
U_c(Q) = \sum_{t, r}^{N_{\mathrm{t}}, N_{\mathrm{r}}} \sum_{i=1}^{N_{\mathrm{f}}} \sum_{k=1}^{N_{\mathrm{s}}} 
c \Big( 
    D \big( 
        F_i(q_{t, r}) \cdot{} x_{ik}
    \big) 
    - r_{ik}
\Big)
$$

**Smooth Clipping Function**

$$
\begin{aligned}
c(d) &= 
\left\{
\begin{array}{ll}
-d + \frac{\epsilon}{2}               & \text{, if }                d <    0 \\ 
\frac{1}{2 \epsilon} (d - \epsilon)^2 & \text{, if }  0        \leq d \leq \epsilon \\
0                                     & \text{, if }  \epsilon <    d
\end{array}
\right.
\end{aligned}
$$

**Self-collision Cost**

$$
U_s(Q) = \sum_{t, r}^{N_{\mathrm{t}}, N_{\mathrm{r}}} \, \sum_{j>i}^{N_{\mathrm{f}}, N_{\mathrm{f}}} \, \sum_{k, l}^{N_{\mathrm{s}i}, N_{\mathrm{s}j}} 
c \big( 
    \big| 
         F_{i}(q_{t, r}) \cdot x_{ik}  -  F_{j}(q_{t, r}) \cdot x_{jl} 
    \big|
    - r_{ik} - r_{jl} 
\big)
$$


![U](../assets/imgs/chomp/substepspheres.png)


<iframe width="660" height="335"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>