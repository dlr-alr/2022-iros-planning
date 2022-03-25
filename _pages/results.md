---
permalink: /results
layout: page
title: Results
---

---

![table for methods](../assets/imgs/results/table-methods.png){:.this 
style="width: 500px;
display: block;
margin-left: auto;
margin-right: auto"}
*Effect of the different methods for improving the dataset on the feasibility.*

---


![top: feasibility over iterations, bottom: feasibility distribution](../assets/imgs/results/results_iterations.png){:.this
style="width: 500px;
display: block;
margin-left: auto;
margin-right: auto"}
*Top: Average convergence to feasibility of OMP for different initial guesses. 
The prediction of the network outperforms the average and even the best out of 100 multi-starts significantly.
Bottom: Distribution of the average feasibility of the random multi-starts after 50 OMP iterations.*

---

**First experiments on the real robot**
<p align="center">
    <iframe width="730" height="400" 
        src="https://youtube.com/embed/zJdIBKAZaIU" 
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
    </iframe>
</p>
The network was only trained with the random astroid worlds, but was able to generalize to this unseen table scene.
The OMP was able to quickly converge to a feasible path for motion problems that required multi-starts otherwise.
The direct connection did not result in a feasible solution.*