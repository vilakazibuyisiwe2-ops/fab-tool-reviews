---
layout: home
title: Home
---

## Built for people who work with metal

Straight-talking guidance on welding equipment, fabrication tools, safety gear, and engineering software — from a qualified boilermaker who cares about what works on the job.

<div class="home-links">
  <a class="btn" href="{{ '/posts/' | relative_url }}">Read the blog</a>
  <a class="btn btn-primary" href="{{ '/reviews/' | relative_url }}">Browse reviews</a>
  <a class="btn" href="{{ '/education/' | relative_url }}">Free safety guides</a>
</div>

## Latest Blog Posts

{% assign posts = site.posts | sort: "date" | reverse %}
{% if posts.size > 0 %}
<ul class="post-list featured-list">
  {% for post in posts limit: 4 %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%-d %B %Y" }}</p>
      {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>
{% endif %}

<a class="btn" href="{{ '/posts/' | relative_url }}">View the blog →</a>

## Featured Reviews

{% assign reviews = site.reviews | sort: "date" | reverse %}
{% if reviews.size > 0 %}
<ul class="post-list featured-list reviews-list">
  {% for review in reviews limit: 4 %}
    <li>
      <h3><a href="{{ review.url | relative_url }}">{{ review.title | escape }}</a></h3>
      {% if review.date %}<p class="post-meta">{{ review.date | date: "%-d %B %Y" }}</p>{% endif %}
      {% if review.description %}<p>{{ review.description }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>
{% endif %}

<a class="btn btn-primary" href="{{ '/reviews/' | relative_url }}">See all reviews →</a>
