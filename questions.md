---
layout: post
title: Questions
permalink: /questions/
---

<div class="posts">
  {% for post in site.posts %}
    {% if post.category contains "question" %}
      {% unless post.rating == 0 %}
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      {% endunless %}
      {% if post.rating == 0 %}
        <a1 href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a1>
      {% endif %}
    <br>
    {% endif %}
  {% endfor %}
</div>
