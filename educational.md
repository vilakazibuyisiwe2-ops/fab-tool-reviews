---
layout: page
title: Education
permalink: /education/
---

{% assign articles = site.educational | sort: "date" | reverse %}
{% if articles.size > 0 %}
  {% for article in articles %}
### [{{ article.title | escape }}]({{ article.url | relative_url }})
{% if article.date %}*{{ article.date | date: "%-d %B %Y" }}*{% endif %}

{% if article.description %}
{{ article.description }}
{% else %}
{{ article.excerpt | strip_html | truncatewords: 35 }}
{% endif %}

  {% endfor %}
{% else %}
No educational articles yet.
{% endif %}
