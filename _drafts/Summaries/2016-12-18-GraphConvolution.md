---
layout: post
title: Semi-supervised classification with graph convolutional networks
category: summary
---

_This post is based around [Thomas Kipf's paper/post](https://tkipf.github.io/graph-convolutional-networks/#fn2) and [Ferenc Huszár's post](http://www.inference.vc/how-powerful-are-graph-convolutions-review-of-kipf-welling-2016-2/)._

## Problem setting

> We consider the problem of classifying nodes (such as documents) in a graph (such as a citation network), where labels are only available for a small subset of nodes. This problem can be framed as graph-based semi-supervised learning, where label information is smoothed over the graph via some form of explicit graph-based regularization.

An example? What are we classifying? Labels of some sort: topic of documents. Reliability/truthiness. ???

Fundamentally it seems like there are a few parts to this problem;

* Extract structure from graphical representations
* Apply structure to the hidden representations of NNs (close to reasoning?? have vectors and want to know how to compose/relate them given info about their connections to others)

# How did they do it?

### Graph laplacian regularization

Let;

* $A_{ij}$ be an adjacency matrix,
* $X_k$ be a node feature vector,
* $f(X_k)$ be

<side> So this is just saying that we expect labels/information to diffuse across the graph as gaussians?</side>

$$L_{reg} = \sum_{i.j} A_{ij} \parallel f(X_i)−f(X_j)\parallel ^2 $$


### Spectral graph convolutions

$$x*g_{\theta}  = Ug_{\theta}U^Tx$$

> What is a Fourier transform at its core? An expansion of function in terms of eigenfunctions of the Laplacian. For a function on the real line, the Laplacian is simply the second derivative. The functions mapped to multiples of themselves by taking second derivatives are sines and cosines of various frequencies. A Fourier series is a change of basis, using as basis vectors those functions who behave the simplest under the second derivative.
The Fourier transform of a function on a graph is also a change of basis, expanding a discrete function in terms of eigenvalues of the Laplacian, in this case the graph Laplacian. ([John Cook](http://www.johndcook.com/blog/2016/02/09/fourier-transform-of-a-function-on-a-graph/))

### Semi-supervised node classification

$$ Z = f(X,A) = \sigma(\tilde A \rho (\tilde AXW_0)W_1) $$

# Thoughts

> The formulation of Eq. 1 relies on the assumption that connected nodes in the graph are likely to share the same label. This assumption, however, might restrict modeling capacity, as graph edges need not necessarily encode node similarity, but could contain additional information.

### Sparsity

I should look into how `tensorflow` manages sparsity.

The adjacency matrix representation must be extremely expensive in most cases?

How else can you represent a graph?

* A recursive/self-referencing language?
* ?

### Dimensionality reduction

Adjacency matrix at every layer?!? We are not really managing to compress this thing much... Only the dimensionality of the feature vectors. So if each node is a book, or video, or ... this is still pretty good. But, if ??? then = bad. Not scalable to large graphs.

### What problem does it solve?


### Why I think this paper is important



### Issues, criticisms and things to keep in mind


### Why is this problem hard/useful?


### Questions



# Conclusion
