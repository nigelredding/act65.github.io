---
layout: post
title: Review of Building Machines That Learn and Think Like People 
---
by Brenden Lake, Tomer Ullman, Joshua Tenenbaum and Samuel Gershman.

Intelligent machines should;

* build models of their environments that seek to explain causes, not just predict features.
* ground learning based in a fundamental understanding of physics (e.g. existence, persistence, ?) and psychology (agency and goals).
* deconstruct their knowledge into smaller discrete representations that can be composed together.
* learn to learn.

# Models
##### Definition?

> We view learning as a form of model building, or explaining observed data through the construction of causal models of the world.

This is an interesting statement, as at first I am not sure I entirely agree with it. Obviously CNNs, RNNs and DQNs are capable of learning and yet they are model-free. But, you could also argue that these networks are model of the data. 

So I guess it comes down to our definition of model... what does it mean to model something?

Almost all state-of-the-art neural networks algorithms are model-free. (not so sure about this I should figure it out for myself)

For example, convolutional neural networks for image recognition such as ??, deep Q networks for games such as AlphaGO, 

##### Model building

> Connectionist learning algorithms have been shown to learn powerful models, yet their local and incremental nature seems at odds with important aspects of human learning. Many of the most impressive examples of human learning are better characterized as rapid model building than gradual improvements in pattern recognition.

They predict, and recognise patterns, they do not explain, ??. 

What is the best way to learn a model? To test and experiment? To try to reproduce? _What if you have a teacher, how does that help?_ 

So supervised model learning would be a good place for us to start?
How would this work, so we are telling the net that: these are the features you should have used to get to this result. (is that it??)


##### The combination of two styles of learning

> ... humans (may) combine model-based and model-free learning algorithms both competitively and cooperatively, and that these interactions are supervised by metacognitive processes.

The fast model-free system. Learns quick heuristics
The slower model-based system

How can model-free learning help teach a model-based system? And vice versa.

> People can perceive a novel scene or spoken utterance in a fraction of a second, in what is surely a mostly feedforward process.

I think this is the benefit of model-free, feed-forward networks. Like the CNNs and DQNs we see in many applications. They are efficient (kinda) and fast (at acting, not learning). So, we seem to have the ability to act fast and learn slow, but can we do it the other way around? Slow acting and fast learning? Or is that a false dichotomy?

I think the steps forward would be to get a fast learner working and then try to integrate the two types together. Maybe we can even use one to teach the other?



Pinker on learning words (a quote would be nice…)

After reading Steven Pinkers book - The stuff of thought- I have been carrying around his idea that there are two competing processes in the brain.

> words are either stored directly with their associated meanings, in a "mental dictionary", or constructed using morphological rules.

How would this work in a net? Irregular


Embeddings and ??


# Foundations

One of the biggest puzzles/problems with this line of thought is that we do not know how much humans are preprogrammed with through their genetics. This is important because we don't know how much children have to learn from their environment and how 

##### Physics

Are we sure we want to base thought in physics? Intuitively it makes sense, we live in the physical world, and everything we build is, in some sense, physical. But does this apply to machines living in the digital world? I think it requires more thought. 

I think that for the time being, it is a good goal, but maybe one we should reanalyse after its success.

This raises the idea that we could use a physical-net as a module that higher order NNs can be build ontop of.

##### Psychology

So an introductory problem of this would be to learn to predict the goals of different agents in an environment using model-free networks.

Where eventually we would want to learn to build nets that can learn models of the agents and their goals. (is this really necessary? how well can just the model free version do?) 

> A child watching someone play a new video game can infer that the avatar has agency and is trying to seek reward while avoiding punishment. This inference immediately constrains other inferences, allowing the child to infer what objects are good and what objects are bad.

How can a machine learn from another machine? I would love to explore this idea along transfer learning and ?? Also, it would be interesting to investigate how we can use model-based learners to teach model-free learners.

# Composition

> an infinite number of representations can be constructed from a finite set of primitives.

But how would this be done by a neural network?

This is about more than having primitive components, it is about having modular representations that can be composed together.

What are the best primitive components to use? Can this be formulated in information-theoretic terms? 

##### Learning to learn

> Since the parts and relations are themselves a product of previous learning, their facilitation of the construction of new models is also an example of learning-to-learn – another ingredient that is covered below. While compositionally and learning-to-learn fit naturally together

To be clear, they are really talking about helping learning go faster, not learning how to make learning faster.

Since we have already learnt the primitive components of our environment, we don’t need to relearn them every time we see something new. ...

# Challenges

* Learning (or making inferences) from small amounts of sparse data
* Learning goal invariance
* Building models


# Interesting points



> The ‘child as scientist’ proposal further views the process of learning itself as also scientist-like, with recent experiments showing that children seek out new data to distinguish between hypotheses, isolate variables, test causal hypotheses, make use of the data-generating process in drawing conclusions, and learn selectively from others.

I would love to explore this idea along with active learning and falsification.

I feel like this sort of reasoning could be paired with reinforcement learning optimsing for information gained and ...? See ... my pseudocode


Goal invariance. How the hell do you learn that? For example it makes no difference to us ...

## Final thoughts, questions and notes

> In their influential textbook, Russell and Norvig (2003) state that “The quest for ‘artificial flight’ succeeded when the Wright brothers and others stopped imitating birds and started using wind tunnels and learning about aerodynamics.”

So what could/would be the false idol that AI researches worship?

You can find the origional paper [here](https://arxiv.org/abs/1604.00289).
