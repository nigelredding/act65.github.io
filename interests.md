---
layout: page
title: Interests
permalink: /interests/
published: true
---

# Complex structures

How does structure effect function? Structure is function.(?)

### Languages

> Semantic and syntax. 

* Why is linear algebra such an effective language for thinking about and implementing structure in systems? What would a non-linear and differentiable language for structure look like? What language would allow me to differentiably learn, say, a convolution? What alternatives are there to representing information that rival linear algebra?
* What is the right language for describing systems of loss functions, optimisers and agents? How should they be composed and decomposed?
* [Tensorflow](https://www.tensorflow.org/), [Edward](http://edwardlib.org/), ... This is what AI will look like for the foreseeable future, better tools, manifesting as programs and programming languages. What makes these languages effective and useful?
* Graphical models (of computation) where gradients and/or uncertainty (and maybe even loss) can flow along edges and between nodes. Propagation (communication) of information through networks.
* (Programming) Languages. Lambda calculus, ...??? Functional programming ??? Compliers and ??? Declarative.
* What does the english language reflect about how we think, and how does the english language effect the way we think? Why is english such a successful language for communication, reason and ??? 
* Why should we build some languages based on set theory and others on type theory?
* What is optimal language syntax? Meta languages. CFG, or ...? H
* Recursion.

### Architectures

>  

* How does the architecture of a GPU reflect its function? Why is linear algebra so efficient on GPUs? Because fundamentally, a GPU is linear algebra.
* How can alternative computer architectures be used for different problems, what will they be good at? Von Neumann, neuromorphic, photonic, micro-fluid, biological, 
* How can quantum computers, (photonic?), biological computers and neuromorphic computers help us achieve ??? Does does their structure reflect ??
* Algorithmic architectures. Neural networks, ?? Why are Resnets, or Fractal nets, or … suited for their task?

### Physics

> Given that we live in a universe governed by physics, how does that determine the things that are possible, and what are the limits? How does (and should) this influence the way we design our tools?

* The math that describes physics has a nice habit of being incredibly useful elsewhere…
* Variational calculus and optimisation. 
* Connections to dynamical systems. Chaos? Emergence?
* Does $P = NP$? This is one of my favourite questions as it is really asking deep physical questions. What is possible given the physics of our universe?  Will our problems always be hard to solve/learn?
* Foundations and deeper truths. Godel's incompleteness, turing's halting, ???, EWA
* Learning and its connection to physics.
* Quantum computing.
* How fast is it possible to learn something? What are the limits to how much you can learn given that we live in a world governed by physics? Similarly, how fast can you optimise a function?
* If physics is fundamentally linear (like in quantum mechanics) then how should we be designing computers and algorithms to reflect/exploit this?

### Distributed systems

How can we coordinate multiple learners/agents? 
What happens if they process things at different speeds, how can we assign credit?Timing, ... causality.  
Economies

A distributed learning algorithm?!?
Learning to communicate?
How should information (gradients, uncertainty, …?) be propagated/communicated? Resets, densely connected nets, TD learning — all allow the interference for information from different …? How should this information interact?

Can we do as well or better than backprop through time (for training recurrent nets) with an efficient online algorithm (not requiring to store all our mental states for our lifetime and then play it backwards)?  Brains clearly achieve this feat but we have no clue how. TD learning? 

Group management?

Viewing the brain as a system of agents who compete for cognitive resources, barter for information (to remove uncertainty), ???

### Wetware and all that  

The most complex systems we know of, us. Genetics, epigenetics, synthetic biology, neuroscience.  How are we designed and managed? What biases and heuristics are pre-programmed within us? What is the minimal set of assumptions/heuristics/pre-programming that can lead to intelligence?

The brain. How does it work!?!?! [Surfing uncertainty -- Andy Clark](https://www.goodreads.com/book/show/25823558-surfing-uncertainty) Is consciousness just an illusion? The result of our brains trying to predict the world, and yet living within the world.



# Efficiency

> Intelligence is the ability to solve problems efficiently

### Compression and 
* Active learning. 
* Low-power learning and spiking, lazy evaluation, ‘just in time’ processing. Outsourcing memory to the environment, and predicting informations availability to save resources.
* Attention!! Anomaly, salience, novelty, residual errors from generative models, 
* Compression as intelligence and consciousness. AIT.  Efficiency.  Compressing memories. RNNs as program compressors? Following gradients of __?
* Intelligence as entropy maximising agents.[The last question]()


### Entropy

* Kolmogorov complexity.
* Learning is the opposite of (physical) entropy? Certainly structure is.

# Learning

> Generating structure from ???

> Learning is ... ??? finding structure ???

* The brain implements specialised optimisers [Integration of DL and neuro... -- Marblestone](https://arxiv.org/abs/1606.03813). How can we learn these specialised systems? How can you learn to learn? [Learning to learn -- Andrychowicz](https://arxiv.org/abs/1606.04474)
* How can we compose and manage neural networks? What if I want to make a net to make a net? Modular nets. A language .. .? How can neural nets learn to generate other networks? How about learning to manipulate function handles, where the handles are other neural nets?
* Replace everything with neural networks. Removing hand crafted features for more general ???. Gabor filters, ... . Adam, don’t need that, let a NN do it. Addition, boring, let a NN learn it.
* A way to understand the function of complex networks. To know how to networks are similar, what they share, how to morph one into the other, what structure one needs to do X function, ... To be able to decompose their structure into working parts.
* How can we learn good representations? How do we/nns understand things. Invariance and atomic, compositionality. How can we represent things in a way that allows us to do/understand (applied to people and computers). 
* Disentangled!! 
* Causal. Learning structural models.
* RL?!? Decision making? Gradient estimation. Goal invariance.
* Exploding/vanishing gradients, internal covariance shift, catastrophic interference and continuous learning, curse of dimensionality
* NNs, how do they work?!?!
* The big ones; credit assignment, catastrophic interference, invariant and disentangled representations, 
Creativity
Curiosity

### Memory and unsupervised learning

Memory. How do we decide what to remember? How can we store it efficiently, by picking out patterns, easy retrieval, ...

Unsupervised learning!
* Self-supervision and context.
* Generative models.

Prediction!

### Teaching

How can you augment an existing learning system to make is smarter? integrating with existing networks/systems. Transfer learning ... Continuous/on-line learning.

How to teach? Curriculum learning? Bootstrapping loss functions, … ???
Process learning

Model based learning. Teaching processes. Learning/testing/correcting a part. Causality??

Process learning.

Education.


# The scientific method 

Building the perfect scientist. Querying the world, falsifying hypotheses. Prediction and action.
Causality. Counterfactuals.
Specificity. Explanations, rationalism, 
The perfect scientist would ?. It’s a method
