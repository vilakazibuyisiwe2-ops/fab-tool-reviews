---
layout: home
title: "Fabrication & Tools Reviews: Tool and Gear Reviews for Artisans"
description: "Honest tool, safety gear, workshop reviews and safety precaution guides for artisans and tradesmen, from a qualified boilermaker."
---

## Tested by a boilermaker. Trusted on the shop floor

From the welder to the work boots, find out what's worth buying.
<div class="home-links">
  <a class="btn btn-primary" href="{{ '/reviews/' | relative_url }}">Browse reviews</a>
  <a class="btn" href="{{ '/education/' | relative_url }}">Free safety guides</a>
</div>

## Featured Reviews

{% assign reviews = site.reviews | sort: "date" | reverse %}
{% if reviews.size > 0 %}
<ul class="post-list featured-list reviews-list">
  {% for review in reviews limit: 2 %}
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

- **Artisan equipment** — MIG, TIG, and plasma cutters
- **Fabrication tools** — measuring, cutting, and layout tools
- **Safety gear** — practical protection for real workshop conditions
- **Workshop Essentials** — budget-friendly options for small shops too

Subscribe to the [RSS feed]({{ '/feed.xml' | relative_url }}) for new articles and reviews.

---

*This site contains affiliate links, including as an Amazon Associate. I earn from qualifying purchases at no extra cost to you.*
