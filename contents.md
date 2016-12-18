---
layout: page
title: Contents
permalink: /contents/
---

Other than the main feed, there are a couple of different sections on this site. These are a eclectic collection of ideas and interests.

# Questions

Each weekend I am going to summarise a paper that interests me. They will probably be related to memory, learning and/or reasoning.

I want to write some summaries for a couple of reasons.

* Having a collection of papers I have read and analysed makes me feel good.
* These summarise act as a metric for progress and improvement.
* To hone the skill of reading a paper. (picking out the important details, and the ones they left out, …?)
* It helps me focus (which I struggle with).


### Process

* What is the problem setting?
* What problem did they solve?
* How did they do it?
* Why is it important?
* Where is it going? (how does it fit into future research directions?)
* What problems to they sweep under the rug?

<div class="posts">
  {% for post in site.posts %}
    {% if post.category contains "question" %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <br>
    {% endif %}
  {% endfor %}
</div>


# Answers

There are popular and successful answers (/approaches) that already exist. Why are they popular, what problems do they solve, why do we bother?

Ultimately, I would like to answer: what computational problem does ________ solve?

<div class="posts">
  {% for post in site.posts %}
    {% if post.category contains "answer" %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <br>
    {% endif %}
  {% endfor %}
</div>

# Summaries

Each weekend I am going to summarise a paper that interests me. They will probably be related to memory, learning and/or reasoning.

I want to write some summaries for a couple of reasons.

* Having a collection of papers I have read and analysed makes me feel good.
* These summarise act as a metric for progress and improvement.
* To hone the skill of reading a paper. (picking out the important details, and the ones they left out, …?)
* It helps me focus (which I struggle with).


### Process

* What is the problem setting?
* What problem did they solve?
* How did they do it?
* Why is it important?
* Where is it going? (how does it fit into future research directions?)
* What problems to they sweep under the rug?

<div class="posts">
  {% for post in site.posts %}
    {% if post.category contains "summary" %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <br>
    {% endif %}
  {% endfor %}
</div>
