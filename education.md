---
layout: page
title: Safety Guides & Education
permalink: /education/
---

## Free Safety Guides and Resources

Practical, hands-on guides for safe work in the workshop.

{% assign guides = site.educational | sort: "date" | reverse %}
{% if guides.size > 0 %}
<ul class="post-list">
  {% for guide in guides %}
    <li>
      <h3><a href="{{ guide.url | relative_url }}">{{ guide.title | escape }}</a></h3>
      {% if guide.date %}<p class="post-meta">{{ guide.date | date: "%-d %B %Y" }}</p>{% endif %}
      {% if guide.description %}<p>{{ guide.description }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>Safety guides coming soon. Check back soon for practical resources.</p>
{% endif %}
