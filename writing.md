---
layout: default
title: Writing
---

# Writing

## Personal reflections
{% for post in site.posts %}
{% if post.categories contains "reflections" %}
<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">{{ post.excerpt }}</div>
</div>
{% endif %}
{% endfor %}

## Other writing
{% for post in site.posts %}
{% if post.categories contains "writing" %}
<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">{{ post.excerpt }}</div>
</div>
{% endif %}
{% endfor %}
