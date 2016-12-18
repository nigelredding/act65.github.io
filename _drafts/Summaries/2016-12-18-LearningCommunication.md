---
layout: post
title: Learning to communicate
category: summary
---

_This post is based around two papers by Foerster, Assael, Freitas and Whiteson on learning to communicate for solving riddles](https://arxiv.org/abs/1602.02672) and [reinforcement learning](https://arxiv.org/abs/1605.06676)_


# Problem setting


Fundamentally it seems that we need to;

*


# How did they do it?

Definitions:

...


1. last-action inputs: supplying each agent with its previous action as input on the next time step so that agents can approximate their action-observation his- tories,
2. inter-agent weight sharing: a single network’s weights are used by all agents but that network conditions on the agent’s unique ID, to enable fast learning while also allowing for diverse behaviour,
3. and disabling experience replay, which is poorly suited to the non-stationarity arising from multiple agents learning simultaneously

# Thoughts


### What problem does it solve?


### Why I think this paper is important



### Issues, criticisms and things to keep in mind


### Why is this problem hard/useful?


### Questions



# Conclusion
