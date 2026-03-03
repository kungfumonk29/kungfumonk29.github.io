---
layout: default
title: Writing
---

# Writing

Posts detected: {{ site.posts | size }}

## Personal reflections
{% for post in site.posts %}
{% if post.category == "reflections" %}
<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">{{ post.excerpt }}</div>
</div>
{% endif %}
{% endfor %}

## Other writing
{% for post in site.posts %}
{% if post.category == "writing" %}
<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">{{ post.excerpt }}</div>
</div>
{% endif %}
{% endfor %}
