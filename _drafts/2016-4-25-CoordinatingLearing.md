---
layout: post
title: Coordinating learning
---

Imagine we have a multi-modal network in an online reinforcement learning setting. The modes being fed into the network are; vision and audio. And it can effect its environment through some controls.

The vision network is a CNN that feeds into the multi-modal representation in a RNN (mmRNN). The audio network is a RNN that feeds into the mmRNN. The vision network runs at 10 frames per second, with a lag of 0.01s behind real time. The RNN runs at 20 samples per second, with a lag of 3s.

How can we correlate images and noises given that they cannot be ‘experienced’ together?

What if these ‘lags’ and frame rates change? (like how the speed of light/sound effect the correlation)

Now the problem of acting on the environment and trying to determine causal effects. 