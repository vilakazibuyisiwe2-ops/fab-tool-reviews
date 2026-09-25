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

<div class="affiliate-note">
  <strong>Quick note:</strong> Some links are affiliate links. If you buy through one, I may earn a commission at no extra cost to you. I only recommend products that fit the job.
</div>

## Latest Blog Posts

Practical tips, safety advice, and fabrication guides from the workshop.

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

Independent, practical breakdowns to help you choose gear that earns its place in the workshop.

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

### Workshop essentials

- **Welding equipment** — MIG, TIG, and plasma cutters
- **Fabrication tools** — measuring, cutting, and layout tools
- **Safety gear** — practical protection for real workshop conditions
- **CAD and design software** — budget-friendly options for small shops

Subscribe to the [RSS feed]({{ '/feed.xml' | relative_url }}) for new articles and reviews.

---

*This site contains affiliate links, including as an Amazon Associate. I earn from qualifying purchases at no extra cost to you.*
