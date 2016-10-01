---
layout: post
title: How informative are gradients?
category: problem
rating: 1
---

How much information does a gradient tell us?
If we have a complex hypothesis, aka one that is hard(er) to falsify, how does this effect the number of times we need to evaluate gradients and how much information each one gives us?

A simple hypothesis class, e.g. a convex bowl means we can evaluate few gradients to find our way to the global minima. But as the hypothesis class gets more complex, the amount of information each gradient gives us reduces. Can we bound the number of gradients required to find our way to the global minima?


Current practice tells us that second order is not necessary. Aka the computational trade off between calculating more datapoints and their gradients and calculating fewer datapoint, but their gradients and hessians,... Can we prove this? Why does it make sense to throw information away? Surely in small data applications we want all the information about the loss surface that we can get? 

What about third order and beyond?