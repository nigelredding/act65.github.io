---
layout: post
title: Prior Knowledge
---

> In machine learning, the typical approach is to hand design the structure of some 'learning' algorithm. Then to let a computer optimise its parameters. Given this approach, in what sense is the computer actually learning anything? (Talking Machines: Listener question: ???)


In my opinion this is **the** problem to solve in machine learning. The goal being to have general learning ability. As, if these algorithms could learn anything, then why would they need researchers?

So what is it the designer actually does? And how can we encode this process into a net?

### Designing a net

Hyper-parameters. Activation function, structure, ??
Hyper-Meta-learning, in the sense that the researchers, or entire fields, learn  ??? how to structure structure nets, … 

The typical process of designing a network is;

* Analyse data and figure out ???
* Test (and then repeat, but avoid the issue that you are using test data as validation data…)



### The lazy researcher

Cant be bothered designing it, let it design itself.
Ideally? Input from people: none, it would figure it out for itself.

But the search is too great.(?) No-free-lunch theorem. But then how can we explain our thought process? What limits are there, given the no-free-lunch theorem


Ihe need a way for networks to choose their own activation function, to design their own structure, to ...


Now, the problems.

* These dont have nice gradients that we can follow, so how do we find good solutions? Random search?
* Intractable search. 


Solutions?

* A universal network, or a network within a network. Where activation functions are made from networks. that is capable of 
* 

A simpler challenge/toy problem