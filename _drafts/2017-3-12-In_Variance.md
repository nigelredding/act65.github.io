---
layout: post
title: Equivariance and invariance
category: notes
---

We want $f(\cdot)$ to be __equivariant__ to symmetries in $\mathcal G$.
Let $g$ be an action in $\mathcal G$.
Then $f(\cdot)$ is invariant to $\mathcal G$ if

<side> This is just commutativity? </side>

$$g(f(x)) = f(g(x))$$

For example. If we extract features from an image and then rotate those features it will be the same as rotating the image and then extracting the features.

***

We want $f(\cdot)$ to be __invariant__ to symmetries in $\mathcal G$.
Let $g$ be an action in $\mathcal G$.
Then $f(\cdot)$ is invariant to $\mathcal G$ if

$$f(x) = f(g(x))$$

For example. If we extract features from an image it will be the same as rotating the image and then extracting the features.

***

But which do we want for image processing, or audio processing?
