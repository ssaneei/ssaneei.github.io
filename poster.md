---
layout: page
title: Posters
permalink: /poster/
---

<ul class="post-list">
  {% assign items = site.poster | sort: "date" | reverse %}
  {% for p in items %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
      {% if p.date %}<span class="post-meta"> — {{ p.date | date: site.date_format | default: "%b %-d, %Y" }}</span>{% endif %}
      {% if p.excerpt %}<p>{{ p.excerpt }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>


