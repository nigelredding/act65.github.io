---
layout: post
title: Learning to communicate
category: summary
---

_This post is based around two papers by Foerster, Assael, Freitas and Whiteson on learning to communicate for [solving riddles](https://arxiv.org/abs/1602.02672) and [reinforcement learning](https://arxiv.org/abs/1605.06676)._


# Problem setting

Fully cooperative, partially observable, sequential multi-agent decision making problems.

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



# How did they do it?

Definitions:

...


1. last-action inputs: supplying each agent with its previous action as input on the next time step so that agents can approximate their action-observation his- tories,
2. inter-agent weight sharing: a single network’s weights are used by all agents but that network conditions on the agent’s unique ID, to enable fast learning while also allowing for diverse behaviour,
3. and disabling experience replay, which is poorly suited to the non-stationarity arising from multiple agents learning simultaneously


### RIAL

> While RIAL is end-to-end trainable within an agent, it is not end-to-end trainable across agents, i.e., no gradients are passed between agents.

Hmm, want to fix that? Provide others with estimates of their utility? (what does across agents mean?)

### DIAL





# Thoughts


### What problem does it solve?

Centralised planning and decentralised execution is also a standard paradigm for multi-agent planning.

### Why I think this paper is important



### Issues, criticisms and things to keep in mind


> The second, inter-agent weight sharing, involves tying the weights of all agents networks. In effect, only one network is learned and used by all agents. However, the agents can still behave differently because they receive different ob- servations and thus evolve different hidden states.

Huh? What about just sharing low level feature extractors?
This seems to defeat the point of what they are doing? Have a diverse range of agents (they must have been unable to make it work?)

> when multiple agents learn independently the environment appears non- stationary to each agent, rendering its own experience obsolete and possibly misleading.

hmmm.

Not convinced by the riddle experiments. Kind of cool formulating each actor as an agent.

### Why is this problem hard/useful?


### Questions

* It would be nice if we could force them to speak the same language (?). How?

# Conclusion
