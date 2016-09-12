---
layout: post
title: Can a neural net learn to do a convolution?
category: problem
---

Instead of preprogramming structure into our neural networks, how can we design them with fewer prior assumptions? Is it possible to design a differentiable structure that is more felxible than our current architectures. One that can learn a [ResNet](https://arxiv.org/abs/1512.03385), a [Fractal Net](https://arxiv.org/abs/1605.07648), a [DenseNet](http://arxiv.org/abs/1608.06993), ... 

Alternatively, I am imagining a system that can do automatic weight tying. That, given a dataset of images, can learn that a convolution is the optimal operation to be doing.

Could this can be formulated as the problem of agents learning a communication protocol. How should information (usually represented in matrices) be stored and communicated?


### Related

* [Neural networks with differentiable structure](https://arxiv.org/abs/1606.06216)
* [Learning Multiagent Communication with Backpropagation](https://arxiv.org/abs/1605.07736)