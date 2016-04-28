---
layout: post
title: Prediction the value of a convolution
---

Following on from the posts exploring more dimensions to convolve in CNNs. I wonder if it is reasonable to use a net to learn to select which dimensions should be convolved.

To solve the problem that a N-D net would need more computations than the standard (2D conv) CNN, at least in forward propagation. I think a good solution would be to let the conv net learn which convolutions are important given the image and a kernel.

There is no point convolving over a feature that is already symmetric in a dimension. E.g. rotating a circle.

And there is no point convolving over a feature that never never varies in that dimension. E.g. a person is still a person regardless of orientation, position …

### Value estimation

I would want a network to learn to look at an input image, and the kernel to be convolved, and estimate the value of doing a convolution in certain dimensions. 

### Probable convolutions

We could also use statistics from which convolutions were performed for previous ‘similar’ images.

*****

So, we will choose which convolution to do depending on, each convolutions expected value (towards accuracy), how probable it is we should do this (stats on similar images) and some factor of training resources, time, space, error, data remaining, ...


### Questions, thoughts and notes

* Largely inspired by game playing tree search algorithms, like AlphaGO or Giraffe (just two papers I happen to have read).
* I think a great starting point would be trying to get a networks to learn to do a spatial convolution. However, I am unsure where to start.