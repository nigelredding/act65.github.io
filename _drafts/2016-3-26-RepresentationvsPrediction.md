---
layout: post
title: Representation (and Prediction) learning
---

> I think real division in machine learning isn’t between supervised and unsupervised, but what I’ll term predictive learning and representation learning. [Roger Grosse - HIPS blog](https://hips.seas.harvard.edu/blog/)

# Representation learning


What is a good representation? (invariant, specific, independent?, ) 

> In representation learning, our goal isn’t to predict observables, but to learn something about the underlying structure. [HIPS blog](https://hips.seas.harvard.edu/blog/)

??


> So, why representation is important? The short answer is that “good” representation makes life so much easier, presumably, by reducing the computational burden of doing inference/classification/prediction. [HIPS blog](https://hips.seas.harvard.edu/blog/)

Instead of ?? (a simple example of how a different representation helps computation - roman numerals?)

> An algorithm is a systematic way of repeatedly applying mathematical operations to a representation in order to achieve some computational goal. Asking what algorithms a representation supports, therefore, is a matter of asking what mathematical operations can be meaningfully applied to it. [HIPS blog](https://hips.seas.harvard.edu/blog/)

Kinda like language? Depending on your representations (or words) you can combine representations in meaningful ways??


>  …, a more sensible approach would be to first transform (not necessarily bijectively) the data into a different space via an encoder map $\mathbf{f}:\mathbb{R}^D\rightarrow\mathbb{R}^K$, which we choose to “reshuffle” the information to accentuate interesting patterns in the inputs. [HIPS blog](https://hips.seas.harvard.edu/blog/)

# Predictive learning

I think the ?? is that predictive learning often uses representations to aid the prediction, but they are 

For example, we can learn to predict without using representations - by ??? without representations all we have is statistics?

* Predictive learning is when, given the past, you want to guess what the future will be like. (Extrapolations from known data)

*****

So, if predictive learning is commonly supervised (regression and classification) and representation learning is commonly unsupervised (clustering and data visualsations), what would _unsupervised predictive learning_ or _supervised representation learning_ look like?


### Supervised representation learning

Given that we want (Italy) + (Capital) = (Rome), or (royal) + (daughter) = (princess), ...

Word2vec already manages to capture some of these relations. But would a supervised model be better?

In my opinion, we do this a lot. The 'supervision' that these nets get is more at a meta level where the researchers designing the learner supervise the sorts of relation they think is important

##### Unsupervised predictive learning

This is really the ultimate goal. To have a system that we can just place in an environment, where it can gather data, and it eventually learns to predict its environment

*****

### Algebra with representations

I like the idea of having algorithms that can manipulate representations in meaningful ways. 


### CNNs

What if we consider a CNN as a supervised representation learner? Where the CNN is trying to learn good representations of features in the images, so that a softmax layer (maybe with a few fully connected layers) can use these representations to predict an images label.

Does this representation learning have to be supervised? (RBMs, pretraining? similar idea??)

So the goal of this representation learning is ??

What if the CNN was instead trying to minimise its number of parameters through making its features invariant to transformations (such as rotations, scale, …). 


