---
layout: post
title: Recursive Optimisation
---

is recursive optimisation a thing? (i guess this is kinda related to adaptive optimisers?)

imagine we trained a network (#1) to do active learning/optimisation on another net (#2) that is being trained on some data, e.g. a CNN.
how do we learn the #1 optimiser network? (as the whole point is to avoid sgd...) can we use a previous version of itself, like in self-play in reinforcement learning. kind of like applying the optimiser net recursively to itself?