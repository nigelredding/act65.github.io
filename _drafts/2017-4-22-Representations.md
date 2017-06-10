---
layout: post
title: Representation learning
category: notes
---

<!-- this isnt good style? should let people formulate the questions themselves.
i should be aiming to set up the info in a way to encourages (these) questions -->

* What are the differences between learned representations?
* What makes a good representation (e.g. for classification with softmax and crossentropy)?
* What do we want from our representations?
* What is the connection between how a representation is used and the representation itself?
* What about other types of representation. What are the pros/cons?

<!-- Want.
- Test accuracy on unsupervised pretraining. (does it work as advertised?)
  - for classification, and segmentation and ??.
- Tensorflow embedding visualsisations of each. (what are the observable differences/patterns)
- 2d vector fields of input and output relations?
- Math showing the differences
 -->

## Autoencoders (AEs)

Learn principle components/eigenvectors of the covariance matrix of x, y. \Sigma_{xy} [baldi](https://arxiv.org/abs/1108.4135)
But nonlinear aes ?!?!
[vae](https://arxiv.org/abs/1312.6114)

## Generative adversarial networks (GANs)
[gan](https://arxiv.org/abs/1406.2661)

All that talk about learning moments??
The discriminator will learn things about the boundaries of P(x), but not necessarily about relationships between x_is. What is it we actually want?!? And for what uses?

What can we use p(x) for? does this in any way allow us to randomly sample the subspace of p(x) to do a sort of random SVD?
$$
\mathcal L
$$


## Noise as targets (NAT)

[nat](https://arxiv.org/abs/1704.05310)

http://www.inference.vc/unsupervised-learning-by-predicting-noise-an-information-maximization-view-2/
https://papers.nips.cc/paper/2410-information-maximization-in-noisy-channels-a-variational-approach.pdf

$$
\mathcal L = argmin_{\theta} argmin_{P} \parallel PCf_{\theta}(x)\parallel
$$

so optimising this is the same as optimising for maximum mutual information.
thus we have a measure of the difference between a uniform distribution and the
distribution of zs.
but f is a deterministic mapping. so this is really just saying that we want
uniform spacing? this makes more sense to interpret as a hash.
mapping each x to a unique z such that the zs are evenly spaced and preseve the locality of xs.

a locality sensitity represnetation should need a fully connected layer to make predictions.
we should be able to classify based upon clusters?


## Siamese networks

What about
$$
\mathcal L = argmin_{\theta} (1-\parallel f(x_1)-f(x_2)\parallel_2)^2 \
$$

Want all x_is to be evenly spaced (thus they will be easily separable?!?).
Will incur a higher loss for tightly packed (aka hard to separate) sets of x.

## Clustering

?!? Nearest neightbors? k-means?


##

***

Optimising for ???
* reconstruction
* mutual information
* ?

If the data is the same, and the optimiser is the same, and the network architecture is the same, then all that is left is their loss functions and metrics. So these must determine the different types of representation, and ...?
