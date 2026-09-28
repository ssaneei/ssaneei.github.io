---
layout: page
title: Posters
permalink: /poster/
---

<div class="posters">
  {% assign items = site.poster | sort: "date" | reverse %}
  {% for p in items %}
    <article class="poster-card">
      <h2 class="poster-title">
        <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
      </h2>

      {% if p.summary %}
        <div class="poster-summary">
          {{ p.summary | markdownify }}
        </div>
      {% elsif p.excerpt %}
        <div class="poster-summary">
          {{ p.excerpt | strip_html | normalize_whitespace | truncate: 220 }}
        </div>
      {% endif %}
    </article>
  {% endfor %}
</div>

<style>
  .posters .poster-card { padding: 0 0 1.25rem; margin: 0 0 1.5rem; border-bottom: 1px solid rgba(255,255,255,.12); }
  .posters .poster-title { font-size: clamp(1.4rem, 2.4vw, 2rem); line-height: 1.2; margin: 0 0 .35rem; }
  .posters .poster-title a { text-decoration: none; }
  .posters .poster-title a:hover { text-decoration: underline; }
  .posters .poster-summary p { margin: 0; opacity: .9; }
</style>
