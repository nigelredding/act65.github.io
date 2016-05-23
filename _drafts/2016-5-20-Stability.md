---
layout: post
title: Stability and uncertainty
---

Define stability.
* Stability is certainty, uncertainty is instability
[Off the convex path](http://www.offconvex.org/2016/03/14/stability/)
* How close you are to a decision boundary?
* …?

> An algorithm is stable, intuitively speaking, if its output doesn’t change much if we perturb the input sample in a single point. [Moritz Hardt](http://www.offconvex.org/2016/03/14/stability/)




### Dropout to approximate stability

The general idea is to perturb a system and see how it changes.

[](http://mlg.eng.cam.ac.uk/yarin/blog_3d801aa532c1ce.html)
[](http://arxiv.org/abs/1512.05287)

Why bother with numerical approximations, like using dropout, and instead use autograd? Is there some sort of other analysis we can do on the net (from controls??) to determine its stability?

### Active learning

> … we train a full Convolutional Neural Network (CNN) by selecting the training samples with a committee of partial CNNs based on batch-wise dropout on the current full CNN
[Query by dropout committee](https://arxiv.org/abs/1511.06412)

> Query by committee: a variety of models are trained on the current labeled data, and vote on the output for unlabelled data; label those points for which the "committee" disagrees the most [Wikipedia](https://en.wikipedia.org/wiki/Active_learning_(machine_learning))

[Committee of one](https://brage.bibsys.no/xmlui/bitstream/handle/11250/2352342/13954_FULLTEXT.pdf?sequence=1&isAllowed=y)

Two different scenarios;
* Cost for querying data
* Cost for labelling data



