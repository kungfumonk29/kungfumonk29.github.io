---
layout: default
title: Writing
---

# Writing

<div class="subscribe-box">
  <h2>Subscribe</h2>
  <p>Get an email when new writing is published.</p>

  <form
    action="https://buttondown.com/api/emails/embed-subscribe/Aryaman29"
    method="post"
    class="embeddable-buttondown-form"
  >

    <input
      type="email"
      name="email"
      id="bd-email"
      placeholder="you@example.com"
      required
    >

    <button class="button" type="submit">
      Subscribe
    </button>

  </form>
</div>

---

## Personal reflections

{% for post in site.posts %}
{% if post.categories contains "reflections" %}

<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">
    {{ post.date | date: "%-d %b %Y" }} · {{ post.excerpt }}
  </div>
</div>

{% endif %}
{% endfor %}

---

## Other writing

{% for post in site.posts %}
{% if post.categories contains "writing" %}

<div class="list">
  <a class="item" href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <div class="meta">
    {{ post.date | date: "%-d %b %Y" }} · {{ post.excerpt }}
  </div>
</div>

{% endif %}
{% endfor %}
