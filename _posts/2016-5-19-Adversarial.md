
---
layout: post
title: A worthy adversary 
---


> In the proposed adversarial nets framework, the generative model is pitted against an adversary: a discriminative model that learns to determine whether a sample is from the model distribution or the data distribution. The generative model can be thought of as analogous to a team of counterfeiters, trying to produce fake currency and use it without detection, while the discriminative model is analogous to the police, trying to detect the counterfeit currency. Competition in this game drives both teams to improve their methods until the counterfeits are indistinguishable from the genuine articles. [Goodfellow et al. 2014](http://arxiv.org/abs/1406.2661)


### Dyamical systems?
Like a arms race. As one gets better, the other does as well, until ???. Is there a way to use tools from dynamical systems to analyse this? This just reminds me of the typical 2D population dynamics. 

$$
\begin{align}
\frac{dx}{dt} & = x(\alpha - \beta y) \\
\frac{dy}{dt} & = y(\delta x  - \gamma ) \\
\end{align}
$$
[Lotka-Voltera equations](https://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra_equations)
$$
\begin{align}
\frac{d \mathcal{L}_Recon}{d t} & = \alpha \mathcal{L}_Recon - \beta \mathcal{L}_Recon \mathcal{L}_Class \\
\frac{d \mathcal{L}_Class}{dt} & = \delta \mathcal{L}_Recon \mathcal{L}_Class  - \gamma \mathcal{L}_Class
\end{align}
$$

So if;

* the reconstruction cost is zero then the reconstion cost will be stable at zero.
* 



### Features

Two parts:

* Autoencoder to reconstruct its input.
* Classifier to predict category (true or false).

It seems to me that features useful for classification would also be useful for reconstruction? For example ...? And vice versa?

### Algorithmic game theory

* Is there a nash or correlated equilibrium that falls out of this?
* What happens if we make it a zero sum game?
* 