---
layout: post
title: Conserved complexity
---
Given a measure of complexity, $\mathcal C$, I want it to satisfy:

__Property 1__: the complexity all algorithms within the lower bound (according to C? -- this seems like a trivial definition?!) are equivalent.

Given a problem (such a 3-SAT), one can imagine many different algorithms that may give a solution. Some might be fast, some might be accurate, some might use a lot of memory...

![pic]({{site.baseurl}}\images/pareto.png)

Each of these algorithms must lie on or behind some lower-bound of complexity.

<!-- That is the lower bound on the complexity of a problem is a(n ordered) set of algorithms that ??? -->

Let $$S = \{s : \mathcal C(s) = \mathop{min}_S \mathcal C(s)\}$$

The main intuition behind this equivalence set is that you can trade memory for time, or parallelism for energy, or ... but underneath there is still the same fundamental problem you need to solve. That is what I want to capture.


* _Can this be generalised to approximate algorithms, trading data efficiency for accuracy?_
* _What is the fundamental unit of accounting? Energy?_

__Property 2__: The measure of complexity for a problem and its solution is the same (via some sort of duality?).

$s \in S, p \in P, \mathcal C(s) = \mathcal C(p)$.

The intuition is that the problem itself is where the complexity comes from, and is independent of the solution.

* _Is it possible to calculate C(p) without considering any solutions?_

<!--
* Need a complexity measure.
* Need to find set of algorithms in the lower bound $S_{LB}$
* Show that the complexity measure is invariant to transformations within $S_{LB}$
* Show that 'complexity' is conserved. -->

__Property 3__: This measure of complexity is proportional to the entropy produced by the implemented algorithm.

<side>Is that structure already captured by entropy?</side>
The intuition is that algorithms require energy to be run, and this costs us information. Some harder problems will require more information to be destroyed than others.

> Entropy is (/can be viewed as) a measure of the distribution of energy and that this measure of complexity would also capture the structure (symmetries, ???) within that energy.

* _Could this could give us a lower bound on the information that must be consumed to solve our problem?_
* ?
