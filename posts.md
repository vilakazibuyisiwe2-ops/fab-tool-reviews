---
layout: home
title: Home
---

## Real reviews for people who actually work with metal

I test and research welding equipment, fabrication tools, and engineering software so you don't have to guess what's worth your money — just what works, what doesn't, and what's actually worth the price.

## Latest Posts

Fresh tips, safety advice, and fabrication guides from the workshop.

{% assign posts = site.posts | sort: "date" | reverse %}
<ul class="post-list">
  {% for post in posts limit: 4 %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%-d %B %Y" }}</p>
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>

[View all posts →]({{ "/posts/" | relative_url }})

## Latest Reviews

A quick look at the newest review-style breakdowns.

{% assign reviews = site.reviews | sort: "date" | reverse %}
<ul class="post-list">
  {% for review in reviews limit: 4 %}
    <li>
      <h3><a href="{{ review.url | relative_url }}">{{ review.title | escape }}</a></h3>
      {% if review.date %}
        <p class="post-meta">{{ review.date | date: "%-d %B %Y" }}</p>
      {% endif %}
      {% if review.description %}
        <p>{{ review.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>

[View all reviews →]({{ "/reviews/" | relative_url }})

### 🔧 Boilermaker Tools I Use in My Workshop

**1. 300mm Digital Caliper for precise measurements** The 150mm is too small for frustums. I use this 300mm Kynup — waterproof, holds the reading so I can type straight into my calculator.
👉 [Check Price on Amazon - Global Link](https://www.amazon.com/dp/B09KGHRKHY?tag=smartfabricat-20)

**2. N2 Engineering Drawing Book** For N2 students - First-angle vs Third-angle explained properly.
👉 [See Drawing Textbook on Amazon](https://www.amazon.com/s?k=engineering+drawing+textbook&tag=smartfabricat-20)

### Categories

- **Welding Equipment** — MIG, TIG, plasma cutters
- **Fabrication Tools** — measuring, cutting, layout tools
- **CAD & Design Software** — Budget friendly options for small shops

Explore the latest writing and research across the site — subscribe to the [RSS feed]({{ "/feed.xml" | relative_url }}).

---

*This site contains affiliate links, including as an Amazon Associate. I earn from qualifying purchases at no extra cost to you.*
