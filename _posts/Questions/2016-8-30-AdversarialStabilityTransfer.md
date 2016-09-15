---
layout: post
title: How are adversarial training, stability and transfer lear
category: problem
published: false
rating: 1
---




***

In novelty detection (another project I’m working on) we want our classifier to draw a tight (decision) boundary around the data it has seen (but not so tight that it cant find patterns within our data). This tight boundary should help us classify/distinguish the novelties that lie outside our boundary (or off our manifold, if you prefer) and the data within/on it. The problem I have been facing is that my novelty detectors over generalise and classify novelties as being part of the original dataset. Our current solution to this problem is to use an adversarial generator that learns/is a model of novelties (an infinitely large class that we really have no idea about -- fundamentally, I don’t think this makes sense). We can then use this model to help shape/refine our boundaries/manifold (aka throw noise, crappy and eventually plausible, yet fake, images at your model and use them to help tighten the boundary). 

What I really want is a way to control how a network generalises (where it generalises and how well). So that I can tell my classifier to draw tight boundaries around my data without needing to train on noise, or more generally, without needing to have a model of novelties. I think this is related to adversarial examples, stability and transfer learning (which is the converse problem ??).

Related to;

* [Manifolds]()
* [Adversarial examples]() and [training]()
* [Transfer learning]()