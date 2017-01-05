---
layout: page
title: Interests
permalink: /interests/
---

# Languages

> Semantics and syntax. 

* [A functional language for neural networks, loss functions, optimisers, ...?](http://act65.github.io/FirstClassNets/)
* Why is [Linear algebra](http://act65.github.io/LinAlg/) so awesome?
* Is AI synonymous with better tools? What AI will look like for the foreseeable future, better tools, manifesting as programs and programming languages (for example [Tensorflow](https://www.tensorflow.org/), [Edward](http://edwardlib.org/)). What makes these languages effective and useful?
* Graphical languages ... (e.g. [PGMs](), [tensor networks](), category theory, geometry, ...) How can languages can help humans understand abstract and complex concepts?
* Why are graphical models (e.g. of computation) so powerful? How should information (gradients, uncertainty, …?) be propagated/communicated? How useful is it to be able to propagate gradients and/or uncertainty (and maybe even loss) along edges/between nodes. 
* What does the english language reflect about how we think, and how does the english language effect the way we think? Why is english such a successful language for communication and reason?
* Meta-structure in language. Parsers, contextfree grammars ...


# Architectures

> Structure and function.

* How does the architecture of a GPU reflect its function? Why is linear algebra so efficient on GPUs? Because fundamentally, a GPU is linear algebra.
* How can alternative computer architectures be used for different problems, what will they be good at? Von Neumann vs ?, neuromorphic, photonic, micro-fluid, biological, quantum, ...
* Algorithmic architectures. Why are Resnets, LSTMs, GANs, ... good at learning certain functions? How does their structure determine their function?
* How can we coordinate multiple learners/agents? What happens if they process things at different speeds, how can we assign credit or infer causality?

# Physics

> 

* Is there a link between variational calculus, lagrangian mechanices/the principle of least action and optimisation of neural networks?
* Given that we live in a universe governed by physics, how does that determine the things that are possible, and what are the limits? How does (and should) this influence the way we design our tools? ([Church-Turing-Deutsch principle](https://en.wikipedia.org/wiki/Church%E2%80%93Turing%E2%80%93Deutsch_principle))
* Does $P = NP$? This is one of my favourite questions as it is really asking deep physical questions. What is possible given the physics of our universe?  Will our problems always be hard to solve/learn?
* Quantum computing. At least one of the ridiculus statements is true. Quantum physics is wrong, quantum computers can be built, ??? (Scott Aaronson).
* What is feasibly learnable (or optimisable or solvable) given our physical world?
* If physics is fundamentally linear (like in quantum mechanics) then how should we be designing computers and algorithms to reflect/exploit this?
* How is the structure of physics refelcted in math? (e.g. Central limit theorem -> math as entropy -> physics)
* The unreasonable effectiveness of physical math in other areas. How do symmetries in physics...


# Cognitive science

* What biases and heuristics are pre-programmed within us? What is the minimal set of assumptions/heuristics/pre-programming that can lead to intelligence?
* The brain, how does it work?!? [Surfing uncertainty -- Andy Clark](https://www.goodreads.com/book/show/25823558-surfing-uncertainty) Is consciousness just an illusion? The result of our brains trying to predict the world, and yet living within the world.
* Can we find an effective distributed learning algorithm? Can we do as well or better than backprop through time (for training recurrent nets) with an efficient online algorithm (not requiring to store all our mental states for our lifetime and then play it backwards)?  Brains clearly achieve this feat but we have no clue how. TD learning? 
* Why are people biased? How are these biases a necessary result of efficient information processing?
* 

# Genetics

* The most complex systems we know of, us. Genetics, epigenetics, synthetic biology, ... How are we designed and managed?
* Protien networks. Epigenetic control/regulation of genes (gene networks).
* Natural selection. 

# Computation

* Computional complexity
* Information theory
* Church-turing thesis
* Type theory
* 


# Efficiency

> Intelligence is the ability to solve problems efficiently

* Active learning. How can we actively query the would to speed up learning?
* Low-power learning and spiking, lazy evaluation, ‘just in time’ processing. Outsourcing memory to the environment, and predicting informations availability to save resources.
* Attention!! Anomaly, salience, novelty, residual errors from generative models, 
* Compression as intelligence and consciousness. AIT.  Efficiency.  Compressing memories. RNNs as program compressors? Following gradients of compression.
* Kolmogorov complexity.
* Learning is the opposite of (physical) entropy? Well, certainly structure is.
* Compression and entropy

# Learning

* The brain implements specialised optimisers [Integration of DL and neuro... -- Marblestone](https://arxiv.org/abs/1606.03813). How can we learn these specialised systems? How can you learn to learn? [Learning to learn -- Andrychowicz](https://arxiv.org/abs/1606.04474)
* How can we compose and manage neural networks? How can neural nets learn to generate other networks? How about learning to manipulate function handles, where the handles are other neural nets?
* How much can we replace with neural networks, a kind of differntiable/learnable programming. Removing hand crafted features in general.
* A way to understand the function of networks. To know how to networks are similar, what they share, how to morph one into the other, what structure one needs to do X function, ... To be able to decompose their structure into working parts.
* How can we learn good representations? How do we/nns understand things. Invariance and compositionality. How can we represent things in a way that allows us to do/understand (applied to people and computers). 
* How does it make sense to learn causal connections from statistical information?
* Exploding/vanishing gradients, internal covariance shift, catastrophic interference and continuous learning, curse of dimensionality, credit assignment.
* How can we design learners to be creative and curious?
* How can you augment an existing learning system to make is smarter? integrating with existing networks/systems. Transfer learning ... Continuous/on-line learning.
* Curriculum learning and continuation optimisation.
* Model based learning. Teaching processes. Learning/testing/correcting a part.
* Memory. How do we decide what to remember? How can we store it efficiently, by picking out patterns, easy retrieval, ...
* How can we effectively use unlabelled data to help us learn? Self-supervision and context. Generative models?
* Which inductive bias is the right one? What are the inductive biases of neural networks and how does that help them learn?


# Math

* Optimisation
* Calculus, automatic gradients
* Linear algebra and tensors
* Symmetry, groups, ...
* A language for clear thought! If you understand a problem, then you can describe it using math. (kinda of?)


# Philosophy

* How can we build the perfect scientist? One that queries the world, makes specific predictions and falsifies hypotheses. 
* Scientific method
* Occam's razor.