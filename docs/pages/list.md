---
layout: page
title: 紀錄
permalink: /list/
toc: false
---

本人超無聊紀錄

## 刮刮樂記錄

<div class="post-list">
  {% assign items = site.list
    | where: "category", "instant-list" %}

  {% for post in items %}
    <article class="post-item">
      <h3 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <!-- post.description -->
      {% if post.description %}
        <p class="post-excerpt">{{ post.description }}</p>
      {% else %}
        <p class="post-excerpt">{{ post.content | strip_html | truncate: 120 }}</p>
      {% endif %}
    </article>
  {% endfor %}
</div>
