---
layout: default
title: Writing
description: Personal reflections and selected writing across finance and strategy.
---

# Writing

## Personal reflections

{% for post in site.posts %}
  {% if post.category == "reflections" %}
  <div class="list">
    <a class="item" href="{{ post.url }}">{{ post.title }}</a>
    <div class="meta">{{ post.excerpt }}</div>
  </div>
  {% endif %}
{% endfor %}

## Other writing

{% for post in site.posts %}
  {% if post.category == "writing" %}
  <div class="list">
    <a class="item" href="{{ post.url }}">{{ post.title }}</a>
    <div class="meta">{{ post.excerpt }}</div>
  </div>
  {% endif %}
{% endfor %}
