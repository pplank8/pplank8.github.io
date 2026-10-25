---
layout: default
permalink: /blog/
title: blog
nav: false
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 10
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 3
---

<div class="post blog-index">
  <header class="post-header">
    <h1 class="post-title">{{ site.blog_name }}</h1>
    {% if site.blog_description %}
      <p class="post-description">{{ site.blog_description }}</p>
    {% endif %}
  </header>

{% if page.pagination.enabled %}
{% assign postlist = paginator.posts %}
{% else %}
{% assign postlist = site.posts %}
{% endif %}

  <ul class="post-list">
    {% for post in postlist %}
      <li>
        <h2>
          {% if post.redirect == blank %}
            <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          {% else %}
            <a class="post-title" href="{{ post.redirect | relative_url }}">{{ post.title }}</a>
          {% endif %}
        </h2>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
        <p class="post-meta">{{ post.date | date: '%B %-d, %Y' }}</p>
      </li>
    {% else %}
      <li>No posts yet.</li>
    {% endfor %}
  </ul>

{% if page.pagination.enabled %}
{% include pagination.liquid %}
{% endif %}

</div>
