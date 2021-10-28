---
layout: page
title: 
---

This site complements the paper [Massively Speeding Up Optimization-based Motion Planning through Deep Learning](https://arxiv.org).
Here we introduce the different robots we used for our work and talk about the details of the dataset generation.
Furthermore we describe the encoding of the world, the network architecture and the training process in more detail.

![Justin](/assets/imgs/Justin_in_Action.png)


# Abstract
---
Abstract—A robot needs a good motion planner to move efficiently in a complex and changing environment. 
One option to improve the planning is to encode the experience of successful motions in a neural network and use its prediction as an initial guess for an optimization-based planner. 
However, until now, this idea could not scale to complex robots in unseen 3D environments. We introduce the basis set representation as a modern method to process spatial data to motion planning to fill this gap. 
This new compact environment encoding from computer vision enables us to train motion planning networks efficiently that generalize well over challenging 3D worlds.
Furthermore, we show that datasets produced by classical methods are often ambiguous as the found solutions are not optimal, especially in hard scenarios. 
This inconsistency hinders the learning of a general mapping from motion task to trajectory. 
Using the network and the objective function as a metric, we can efficiently improve, extend and train on an initial dataset produced by a classical solver. 
Our network can predict an initial guess that quickly converges to a feasible solution, outperforming random multi-starts massively for all test cases, even in unseen environments. 
The quick inference time of the network plus the guarantees of a classical solver lead to a fast and safe way to generate optimal paths. 
Finally, our tests on the humanoid robot Agile Justin show the capabilities of this approach for the real world.
