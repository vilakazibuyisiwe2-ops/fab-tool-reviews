---
layout: home
title: Home
---

<style>
  .home-hero-bg {
    position: fixed;
    inset: 0;
    z-index: -1;
    background-image: linear-gradient(rgba(8, 12, 18, 0.52), rgba(8, 12, 18, 0.52)), url('{{ "/assets/images/etienne-girardet-sgYamIzhAhg-unsplash.jpg" | relative_url }}');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.9;
    pointer-events: none;
  }

  .home-content {
    position: relative;
    z-index: 1;
    color: #e0e0e0;
  }
</style>

<div class="home-hero-bg" aria-hidden="true"></div>
<div class="home-content">

## Built for people who work with metal

Straight-talking guidance on welding equipment, fabrication tools, safety gear, and engineering software — from a qualified boilermaker who cares about what works on the job.

<div class="home-links">
  <a class="btn" href="{{ '/posts/' | relative_url }}">Read the blog</a>
  <a class="btn btn-primary" href="{{ '/reviews/' | relative_url }}">Browse reviews</a>
  <a class="btn" href="{{ '/education/' | relative_url }}">Free safety guides</a>
</div>

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

### Workshop essentials

- **Welding equipment** — MIG, TIG, and plasma cutters
- **Fabrication tools** — measuring, cutting, and layout tools
- **Safety gear** — practical protection for real workshop conditions
- **CAD and design software** — budget-friendly options for small shops

Subscribe to the [RSS feed]({{ '/feed.xml' | relative_url }}) for new articles and reviews.

---

*This site contains affiliate links, including as an Amazon Associate. I earn from qualifying purchases at no extra cost to you.*

</div>
