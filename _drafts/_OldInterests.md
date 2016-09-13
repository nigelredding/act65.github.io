# Languages

> Semantic and syntax. 

* Why is linear algebra such an effective language for thinking about and implementing structure in systems? What would a non-linear and differentiable language for structure look like? What language would allow me to differentiably learn, say, a convolution? What alternatives are there to representing information that rival linear algebra?
* What is the right language for describing systems of loss functions, optimisers and agents? How should they be composed and decomposed?
* [Tensorflow](https://www.tensorflow.org/), [Edward](http://edwardlib.org/), ... This is what AI will look like for the foreseeable future, better tools, manifesting as programs and programming languages. What makes these languages effective and useful?
* Graphical languages ... (e.g. PGMs, tensor networks, category theory, geometry, ... ???)What languages can help humans understand these problems better? 
    * Graphical models (of computation) where gradients and/or uncertainty (and maybe even loss) can flow along edges and between nodes. 
* What does the english language reflect about how we think, and how does the english language effect the way we think? Why is english such a successful language for communication and reason?
* How should information (gradients, uncertainty, …?) be propagated/communicated? Resets, densely connected nets, TD learning — all allow the interference for information from different …? How should this information interact?


# Architectures

* How does the architecture of a GPU reflect its function? Why is linear algebra so efficient on GPUs? Because fundamentally, a GPU is linear algebra.
* How can alternative computer architectures be used for different problems, what will they be good at? Von Neumann, neuromorphic, photonic, micro-fluid, biological, quantum, ...
* Algorithmic architectures. Why are Resnets, LSTMs, GANs, ... good at learning certain functions?
* How can we coordinate multiple learners/agents? What happens if they process things at different speeds, how can we assign credit or infer causality?

# Physics

> Given that we live in a universe governed by physics, how does that determine the things that are possible, and what are the limits? How does (and should) this influence the way we design our tools? ([Church-Turing-Deutsch principle](https://en.wikipedia.org/wiki/Church%E2%80%93Turing%E2%80%93Deutsch_principle))

* What is the a link between variational calculus, lagrangian mechanices/the principle of least action and optimisation. 
* Does $P = NP$? This is one of my favourite questions as it is really asking deep physical questions. What is possible given the physics of our universe?  Will our problems always be hard to solve/learn?
* Quantum computing.
* How fast is it possible to learn something? What are the limits to how much you can learn given that we live in a world governed by physics? Similarly, how fast can you optimise a function?
* If physics is fundamentally linear (like in quantum mechanics) then how should we be designing computers and algorithms to reflect/exploit this?
* How is the structure of physics refelcted in math? (e.g. Central limit theorem -> math as entropy -> physics)
* The unreasonable effectiveness of physical math in other areas.
* How do symmetries in physics

# Wetware

* The most complex systems we know of, us. Genetics, epigenetics, synthetic biology, neuroscience. How are we designed and managed? What biases and heuristics are pre-programmed within us? What is the minimal set of assumptions/heuristics/pre-programming that can lead to intelligence?
* The brain, how does it work? [Surfing uncertainty -- Andy Clark](https://www.goodreads.com/book/show/25823558-surfing-uncertainty) Is consciousness just an illusion? The result of our brains trying to predict the world, and yet living within the world.
* Can we find an effective distributed learning algorithm? Can we do as well or better than backprop through time (for training recurrent nets) with an efficient online algorithm (not requiring to store all our mental states for our lifetime and then play it backwards)?  Brains clearly achieve this feat but we have no clue how. TD learning? 


# Efficiency

> Intelligence is the ability to solve problems efficiently

### Compression

* Active learning. How can we actively query the would to speed up learning?
* Low-power learning and spiking, lazy evaluation, ‘just in time’ processing. Outsourcing memory to the environment, and predicting informations availability to save resources.
* Attention!! Anomaly, salience, novelty, residual errors from generative models, 
* Compression as intelligence and consciousness. AIT.  Efficiency.  Compressing memories. RNNs as program compressors? Following gradients of compression.

### Entropy

* Kolmogorov complexity.
* Learning is the opposite of (physical) entropy? Well, certainly structure is.
* The central limit theorem as the mathematical manifestiaiton of entropy.

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

### Memory and unsupervised learning

* Memory. How do we decide what to remember? How can we store it efficiently, by picking out patterns, easy retrieval, ...
* How can we effectively use unlabelled data to help us learn? Self-supervision and context. Generative models?


# Philosophy

* How can we build the perfect scientist? One that queries the world, makes specific predictions and falsifies hypotheses. 
* Scientific method
* 