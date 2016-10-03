---
layout: post
title: Is complexity conserved?
category: problem
rating: 1
---

Could the complexity of a problem/algorithm be a conserved quantity? (This is vaugley inspired by Scott Aaronson's [quip](http://www.scottaaronson.com/blog/?p=2212) about the latest claim that $P=NP$)

> All proposals along these lines simply _“smuggle the exponentiality”_ somewhere that isn’t being explicitly considered

I am imagining that increases in efficiency (that we see so regularly) are actually _smuggling_ the complexity somewhere else. For example;

* increases in 'efficiency' of matmuls are actually costing us elsewhere. Maybe we are having to do more irreversable computations (which we wouldn't notice atm (?)).
* or ??

If I wrote an equation that looked nice but didn't really say much it would be the one below.

$$
\begin{align*}
\mathcal{C}_{error} + \mathcal{C}_{robustness} = \mathcal{C}_{energy} + \mathcal{C}_{time} + \mathcal{C}_{memory} + \mathcal{C}_{data} = const.\\
\end{align*}
$$

### Thoughts

* What does this conservation of complexity imply about underlying structure and symmetries?
* What about the domain that an algorithm works over. What sort of complexity measure do we have there? Should there be one?
* How sure are we that each of these measures of complexity is the right metric?
* How can we represent problems/algorithms as structures?
    * What symmetries do these structures have? 
    * Do all NP-complete problems share the same symmetries?
* This seems like a fundamental property to the task that is trying to be achieved. And each potential algorithm ...? (struggling with the line between problem and solution)