---
layout: post
title: How can we be wrong faster and more often?
category: problem
rating: 1
---

Failure is the best/only way to learn (?). How can we fail more and faster? Failing more is the general idea behind TD learning (??!?). But how can we fail faster?

* In forward-mode TD learning you need to wait D (depth) time steps for the input to filter through the layers to the output, and then $[1,D]$ steps for the associated loss to filter backward through the layers.
* In generative/backward-mode TD learning you need to wait $[1,D]$ (depth) steps for the input/associated loss to filter through the layers to the output. This occurs because the top layer of the generative model predicts what is going to happen in D time steps.

<center><img src="{{ site.url }}/images/GenTD.png" alt="GenTD" align="middle" height="350" width="500"></center>


### Thoughts

* How can this be used in a reinforcement learning setting? Does this imply that we should be generating actions and their effects?
* This is super close to the architecture described in [Surfing Uncertainty](https://www.goodreads.com/book/show/25823558-surfing-uncertainty)