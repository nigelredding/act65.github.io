---
layout: post
title: Learning to communicate
category: summary
---

<i>This post is based around two papers by Foerster, Assael, Freitas and Whiteson (on learning to communicate for [solving riddles](https://arxiv.org/abs/1602.02672) and [reinforcement learning](https://arxiv.org/abs/1605.06676)) and </i>


# Problem setting

The authors describe the setting as: <i>Fully cooperative, partially observable, sequential multi-agent decision making problems.</i>



Fundamentally it seems that we need to;

*

> In other words, we consider centralised learning of decentralised policies.

> Hence, this approach uses centralised learning but decentralised execution.


> How language and communication emerge among intelligent agents has long been a topic of intense debate.
Why does language use discrete structures? What role does the environment play? What is innate and what is learned? And so on. Some of the debates on these questions have been so fiery that in 1866 the French Academy of Sciences banned publications about the origin of human language.
The rapid progress in recent years of machine learning, and deep learning in particular, opens the door to a new perspective on this debate. How can agents use machine learning to automatically discover the communication protocols they need to coordinate their behaviour? What, if anything, can deep learning offer to such agents? What insights can we glean from the success or failure of agents that learn to communicate?


> All the agents share the goal of maximising the same discounted sum of rewards Rt.

So all agents see the reward. Similar to Kickback?

# Motivation

> We are interested in such settings because it is only when multiple agents and partial observability coexist that agents have the incentive to communicate.

Not actually true. Also when agents are distributed (which can be for a few reasons)

Communication is needed for any distributed setting. Problems can be distributed for a few main reasons;

* they are trying to solve a real world problem that is itself distributed in space or time. E.g. sensors over a city, or ...
* the scale (amount of memory/compute) required is large. Memory and computation take physical space, and when working at scale ...

(this motivates communication, but not necessarily having a diverse range of modules/agents)

# How did they do it?

Definitions:

...


1. last-action inputs: supplying each agent with its previous action as input on the next time step so that agents can approximate their action-observation his- tories,
2. inter-agent weight sharing: a single network’s weights are used by all agents but that network conditions on the agent’s unique ID, to enable fast learning while also allowing for diverse behaviour,
3. and disabling experience replay, which is poorly suited to the non-stationarity arising from multiple agents learning simultaneously


### RIAL

> While RIAL is end-to-end trainable within an agent, it is not end-to-end trainable across agents, i.e., no gradients are passed between agents.

Hmm, want to fix that? Provide others with estimates of their utility? (what does across agents mean?)

> split the network into $Q^a_u$ and $Q^a_m$, the $Q$-values
for the environment and communication actions

Chose action for environment and communication independently. Thus

> maximising over U and then over $M$, but not maximising over $U\times M$.

### DIAL

> While RIAL can share parameters among agents, it still does not take full advantage of centralised learning. In particular, the agents do not give each other feedback about their communication actions.

So this reminds me of massage passing? Each agent will give feedback to every other agent it listens to. But we can keep propagating the gradients recursively. How many times should we recurse? An exponential amount of messages, but can be combined at every step to keep them bounded?


> discretise/regularise unit (DRU(mat )). The DRU regularises it during centralised learning, DRU(mat ) = Logistic(N(mat ,σ)), and discretises it during decentralisedexecution, DRU(mat ) = I{ma t > 0}, where σ is the standard deviation of the noise added to the channel.

Can be directly replaced with the concrete distribution.



# Thoughts


### What problem does it solve?

> Centralised planning and decentralised execution is also a standard paradigm for multi-agent planning.

* Transfer learning and domain adaptation?
* Large scale!
  * Fundamental law of universe (it has a name...). Information processing density limit. Therefore we must distribute processing in space and time.
  * Edge/distributed processing means real time action/adaptation.
*

Learning at scale?!? E.g. Cars learning to navigate cities.
Each must learn something pretty similar, but how is it best to make this efficient? Centralise knowledge, or message passing/gossip/diffusion?
More efficient but less accurate(?)

###  (Learning to) Design communication protocols that are robust to noise.

This seems like a separate problem that could be studied in isolation? Given a task and, ?, ?, ?... what is the most efficient way to communicate relevant information?

* An auto encoder?!? But they are blurry...
* The GAN framework will not work as we need to communicate the whole image.
* Ultimate goal. Able to reconstruct from less information?
  * Not quite. Able to reconstruct relevant parts!
  * Depends on the task?

Given an `attender` and a `labeller`. How can these two communicate to classify MNIST?

* Simple solution. `attender` just classifies the digit and `labeller` is just a middle-man.
  * However, if the representation/computational/memorisational power of both agents is harnessed we can do better.


RNNs can be viewed as being distributed in time, therefore they pass messages between agents at every time step.

### Issues, criticisms and things to keep in mind


> The second, inter-agent weight sharing, involves tying the weights of all agents networks. In effect, only one network is learned and used by all agents. However, the agents can still behave differently because they receive different observations and thus evolve different hidden states.

Huh? What about just sharing low level feature extractors?
This seems to defeat the point of what they are doing? Have a diverse range of agents (they must have been unable to make it work?)

> when multiple agents learn independently the environment appears non-stationary to each agent, rendering its own experience obsolete and possibly misleading.

hmmm.


### Poor experiments

Why are the experiments poor? What experiments would have been better?

Colour-digit mnist. -> partial mnist.
What problems are fundamentally suited to being solve by a distributed set of actors?

* (transfer learning on atari games?)
*

Not convinced by the riddle experiments. Kind of cool formulating each actor as an agent.

> in the first step, both agents send a 1-bit message, in the second step they select a binary action u2a

Dont like that. Need to wait for the others reply until we make our action.

##### Distributed optimisation

Maybe it would be better to come at this problem from a different direction (e.g. distributed optimisation). This seems very unprincipled and hacky...


### Why is this problem hard/useful?


### Questions

* It would be nice if we could force them to speak the same language (?). How?
* What is a nice way to organise connectivity between agents. As a graph? By their spatial position/attention. Ideally they could learn how to interact with their environment so they could find the best agents to listen to.
* If we used sparse/spiking message passing (how?) we could regularise the amount of information communicated?!?
* not clear to me why we needed to be in the RL setting.
* Norm. R in graphs. The average reward for solving? So solving it must be binary? And achieving 90% means that we get it wrong 1 in every 10 times. Is this because of the added noise at test time or something else?
* What is the difference between a module and an agent? An agent has a loss function,
* we could use a GAN to regularise the difference between their learned/chosen language and english.
* setting. want the communication protocol/language to be domain agnostic? no probably not? but english...?

# Conclusion
