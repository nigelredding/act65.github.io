---
layout: post
title: Is our current view of second order optimisation wrong?
category: problem
published: false
---

Current ??? says that second order is not necessary. Aka the computational trade off between calculating more datapoints and their gradients and calculating fewer datapoint, but their gradients and hessians,...

Can we prove this? Why does it make sense to throw information away? Surely in small data applications we want all the information about the loss surface that we can get? Second, third, ... ???

***
Can we approximate the hessians witha finite difference?
$$
\sum_{i=0}^t K_d^t (\frac{\partial \mathcal L}{\partial \theta^t} -\frac{\partial \mathcal L}{\partial \theta^{t-1}}) +
$$
