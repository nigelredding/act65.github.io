---
layout: post
title: First class loss functions
category: problem
---

Is there some formal system that can take loss functions as first class objects which can be passed around, transformed, composed, … ? much like functions can be in functional programming. Interestingly, this would allow for recursive loss functions.

I think [Decoupled neural interfaces](http://arxiv.org/abs/1608.05343) do something super interesting, they decompose a global loss function into local loss functions (the functions learnt by the synthetic gradient predictors — the $M_i$s).

Can we make this into a more general framework, where we can reason about how to compose and decompose loss functions? It would be nice to be able to say that the global loss function of a GAN is ???, or that some distributed system of agents is minimising ???, or … ???

Related to;

* Bootstrapping loss functions (term from [Integration of DL and NS](https://arxiv.org/abs/1606.03813)
* [Continuation optimisation](http://people.csail.mit.edu/hmobahi/pubs/aaai_2015.pdf)
* [Curriculum learning](http://ronan.collobert.com/pub/matos/2009_curriculum_icml.pdf)
* [Mollifying networks](http://arxiv.org/abs/1608.04980)