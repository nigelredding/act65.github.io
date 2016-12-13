---
layout: post
title: Answers
permalink: /answers/
---

I want to think about: What problem(s) do well known techniques/approaches help us solve? Or in other words, what problems can answers be applied to? In essence, why bother?

Maybe I can follow a process to try to explore this question. Explain the answer, link it to the question/problem and then find real world examples.

<div class="posts">
  {% for post in site.posts %}
    {% if post.category contains "answer" %}
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    {% endif %}
  {% endfor %}
</div>