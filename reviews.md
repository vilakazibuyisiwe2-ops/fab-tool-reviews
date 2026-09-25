---
layout: page
title: Reviews
permalink: /reviews/
---

{% assign reviews = site.reviews | sort: "date" | reverse %}
{% if reviews.size > 0 %}
<ul class="post-list">
  {% for review in reviews %}
    <li>
      <h2><a href="{{ review.url | relative_url }}">{{ review.title | escape }}</a></h2>
      {% if review.date %}<p class="post-meta">{{ review.date | date: "%-d %B %Y" }}</p>{% endif %}
      {% if review.description %}
        <p>{{ review.description }}</p>
      {% else %}
        <p>{{ review.excerpt | strip_html | truncatewords: 35 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No reviews yet.</p>
{% endif %}
