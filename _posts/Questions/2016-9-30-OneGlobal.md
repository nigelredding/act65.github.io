---
layout: post
title: A single global minima or many?
category: question
---

In [Deep learning without poor local minima](https://arxiv.org/abs/1605.07110), Kenji proves that _Every local minimum is a global minimum_ (see Theorem 2.3 ii) for a linear feedforward neural network of the form;

$$\mathcal L = \sum_{t=0}^T \parallel y_t - W_1...W_i...W_nx_t\parallel_2^2$$

Does this mean that every local minimum is the same local minima (i.e. that they are connected) or that there are multiple distinct local minima that all happen to have the same loss. (I mean connected in the topological sense that we can follow some continuos transform of weights to get from one minima to another.)

If the local minima are connected, does this hint at an easier/alternative way to prove Kenji's result(s)? (We could show that every minima is the same minima, which implies they are all global) Alternatively, why are they not connected?