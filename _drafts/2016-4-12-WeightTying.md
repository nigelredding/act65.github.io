---
layout: post
title: Weighting and invariance
---

What makes a good representation?? (invariant, specific, independent?, ) 

> What we really would like is for a particular feature set to be invariant to the irrelevant features and disentangle the relevant features. (Bengio 2014)

> The process of building invariant features can be seen as consisting of two steps. First, low-level features are recovered that account for the data. Second, subsets of these low level features are pooled together to form higher-level invariant features, exemplified by the pooling and subsampling layers of convolutional neural networks. (Bengio 2014)

General principle of learning. The less you have to learn the easier it is…

# Spatial transformer networks to optimise for minimal parameters

How does this related to spatial transformer networks?

```python
Init a wide deep net. 
Optimise the spatial transformer networks for the amount of weights they tie. 
Drop weights that are not used.
```

So now the net learns that ?. Too much invariance? The rotations of some things does matter. The position of others does matter. 

* Image we have learnt invariance to partial occlusion. Half a person is not the same as a whole person?


The dimensions we want to convolve clearly depends on the feature/context...

> In the context of digit recognition this might mean learning the concept of a ‘0’ with more rotation invariance than a ‘6’, which would incur loss if it had positive weights in the region of symmetry space where a ‘9’ would also fire. (Deep Symmetry Networks)


How can we know which variables our features should be invariant to?


> We conjecture that the main computational goal of the ventral stream of visual cortex is to provide a hierarchical representation of new objects/images which is invariant to transformations, stable, and selective for recognition—and show how this representation may be continuously learned in an unsupervised way during development and visual experience. (Anselmi, 2014)