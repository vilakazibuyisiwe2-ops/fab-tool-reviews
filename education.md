---
layout: page
title: Free Safety & Education
permalink: /education/
---

This section is dedicated to practical, free workshop education for welders, fabricators, and metalworkers. The goal is simple: help people work more safely, understand their tools better, and learn reliable workshop habits without a paywall.

These guides are written to be easy to read, useful on the job, and free to access.

{% assign educational_posts = site.posts | where_exp: "post", "post.categories contains 'Safety' or post.categories contains 'Education' or post.categories contains 'Educational Guides' or post.categories contains 'welding-safety' or post.categories contains 'safety' or post.categories contains 'education'" %}
{% if educational_posts.size > 0 %}
<ul class="post-list">
  {% for post in educational_posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
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
<p>No safety or education articles have been published yet.</p>
{% endif %}

## Popular topics

- Safe angle grinder use
- Welding PPE and eye protection
- Workshop housekeeping and fire prevention
- Correct use of cutting and grinding discs
- Fabrication drawing basics
- Safe handling of gas cylinders and equipment

This page is intended for free educational content, with no paywall. It is designed to support future AdSense eligibility by providing useful, original, evergreen content that serves readers before they buy tools or consume paid content elsewhere.
