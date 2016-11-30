---
layout: post
title:  A functional language for neural networks, loss functions, optimisers, ...?
category: question
---

What is the right language for describing systems of loss functions, optimisers and agents? How should they be composed and decomposed? 

Is it possible to make an equivalent of a universal turing machine for neural networks. Where we have a networks that we can pass a description of another network and some inputs and it can 

Relatedly, is there some language that can take loss functions as [first class](https://en.wikipedia.org/wiki/First-class_function) objects which can be passed around, transformed, composed, … ? Thus allowing for [high order](https://en.wikipedia.org/wiki/Higher-order_function) loss functions. Much like functions can be in functional programming (interestingly, we could make a recursive loss functions).

Can we make this into a more general framework, where we can reason about how to compose and decompose parameterised (loss) functions?

<!-- We can do this with tf in some senses? Connecting nets together. We just dont have ideas about what the result will be-->

### Related ideas and resources

* How are the layers in a neural net related to the tapes in a turing machine?
* [Compsing neural networks for QAs](https://arxiv.org/abs/1601.01705), [Predicting parameters](https://arxiv.org/abs/1306.0543)
* [Decoupled neural interfaces](http://arxiv.org/abs/1608.05343) decompose a global loss function into local loss functions (the functions learnt by the synthetic gradient predictors — the $M_i$s).
* Bootstrapping loss functions (term from [Integration of DL and NS](https://arxiv.org/abs/1606.03813)
* [Continuation optimisation](http://people.csail.mit.edu/hmobahi/pubs/aaai_2015.pdf)
* [Curriculum learning](http://ronan.collobert.com/pub/matos/2009_curriculum_icml.pdf)
* [Mollifying networks](http://arxiv.org/abs/1608.04980)
* What about parameterised loss functions?