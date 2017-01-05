---
layout: post
title: Optimisation
category: main
published: true
---

Optimisation is ... (a nice quote?)

<!-- Goals of this project.

* Learn optimisation
* Understand it in a unique way
* Find connections between disparate things and deeper problems
* ?

How?

* Read. (and keep notes, somewhere...)
* Derive. Proofs from first principles.
* Implement. Code it, test it, scale it. (find empirical validation of computational costs)
* Explain. Through metaphor, imagery, ?
* Compress! Summarise succinctly. Continually refine (code, proofs and explanations).

-->


## Online optimisation

Online optimisation is a new formulation of pattern detection and learning, as opposed to the commonly used statistical framework.

Goal: To get to SGD. The main algol used for NNs.

_Notes stolen from David Balduzzi's course on_ Prediction, learning and games. _Which were stolen from ...?_

### Prediction from expert advice

... ? [expert advice]({{ baseurl }}/Experts).

### Game theory

__TODO__
<!--
Minimax …
The cool things. A partial derivative in game theory.
-->

### Mirror descent

__TODO__

Would like to go into real detail here. A derivation. (possibly an alternate one?) And some implementations. (save distributed for another project?).
[Gradient descent]({{ baseurl }}/GradDescent).

## Search

A general look at [search]({{ baseurl }}/Search), its relation to [sampling]({{ baseurl }}/Sampling) and sorting.

[Sorting]({{ baseurl }}/Sorting) is especially interesting when you view it from the point of view ... (Hashing, ?, ... . Hierarchical. Chunking and ?)



## Dynamical systems

Optimisation can also be viewed as a [dynamical process]({{ baseurl }}/Dynamical).


## Distributed optimisation

What is it for? Why bother?

Collaboration
Parallelism
?

***

### Thoughts and notes on;

* convex optimisaiotn? and basics?
* bergman divergences
* frenchel duals
* bandit setting
* mechanism design
* Calculus of variations.
* recursive opt
* path sgd
* homotopy opt
* convex // non-convex optimisation?
* definition of rationality seems to be related to a) achieving goals b)
* RL? seems very close to core optimisation?
