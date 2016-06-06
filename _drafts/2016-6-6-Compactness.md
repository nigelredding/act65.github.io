---
layout: post
title: Compactness
subtitle: (in)finite?
rating: 3
author: Alex
---

What is compactness? What does it mean for a set to be compact in a space? How does this related to finite/infinite sets?

First lets start with the definitions. 

*****

Let $X$ be a set and $T_X$ be a topological space. Then a set U in X is called compact if: for all finite covers of U there is a finite sub cover of U. Where, a sub cover is a subset of C that still covers U. Or if you prefer, $\forall \mathcal{C} : U \subseteq \bigcup_i C_i $$ \exists \mathcal{S}: U \subseteq \bigcup_i S_i, \mathcal{S} \subseteq \mathcal{C}, \mid \mathcal{S} \mid < \infty$.

*****

What does we mean by a subset of C …? Does it mean that the we need each set in our sub cover ,$S_i$, to be a a subset of each set in our open cover, $C_i$? Or that our sub cover itself is a subset of the open cover?

One of my first thoughts was; doesn’t X just cover everything…? I.e. for any set I pick that is in $T_X$, X is a cover and X is also a sub cover, where $\mid \\{ X\\} \mid = 1$. So that’s it, compact. Nope. We need <underline>all</underline> covers to have finite sub covers.


Is a compact set necessarily finite? No. For example; take a collection of sets in $\mathbb{R}_{STD}$ that cover

Is a compact set necessarily infinite? No. For example

The point is that; a finite collection of infinite sets is compact. But an infinite collection of finite sets is not. (should check?) So compactness is a way to represent the ‘finiteness’ of the topology with respect to its open sets. 

How does this help?

So then how is compactness related to finite/infinite sets?

