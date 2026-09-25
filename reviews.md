---
layout: page
title: All Posts
permalink: /posts/
---

{% assign posts = site.posts | sort: "date" | reverse %}
{% if posts.size > 0 %}
<ul class="post-list">
  {% for post in posts %}
    <li>
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
      <p class="post-meta">{{ post.date | date: "%-d %B %Y" }}</p>
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% else %}
        <p>{{ post.excerpt | strip_html | truncatewords: 35 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No posts yet.</p>
{% endif %}
