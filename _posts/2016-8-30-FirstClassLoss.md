---
layout: post
title:  How can we use loss functions as first class functions?
category: problem
---

Is there some language that can take loss functions as [first class](https://en.wikipedia.org/wiki/First-class_function) objects which can be passed around, transformed, composed, … ? Thus allowing for [high order](https://en.wikipedia.org/wiki/Higher-order_function) loss functions. Much like functions can be in functional programming (interestingly, we could make a recursive loss functions).

Can we make this into a more general framework, where we can reason about how to compose and decompose loss functions? It would be nice to be able to say that the global loss function of a GAN is ???, or that some distributed system of agents is minimising ???, or … ???

### Related ideas and resources

* [Decoupled neural interfaces](http://arxiv.org/abs/1608.05343) decompose a global loss function into local loss functions (the functions learnt by the synthetic gradient predictors — the $M_i$s).
* Bootstrapping loss functions (term from [Integration of DL and NS](https://arxiv.org/abs/1606.03813)
* [Continuation optimisation](http://people.csail.mit.edu/hmobahi/pubs/aaai_2015.pdf)
* [Curriculum learning](http://ronan.collobert.com/pub/matos/2009_curriculum_icml.pdf)
* [Mollifying networks](http://arxiv.org/abs/1608.04980)