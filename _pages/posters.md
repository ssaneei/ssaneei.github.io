---
permalink: /poster/
title: "Posters"
layout: single
author_profile: true

# ── Choose what the Posters tab shows ─────────────────────────────
# One line per slot, in the order you want them on the page.
# Write the file name from _poster/ (with or without .md).
# Leave a slot as "" to keep it empty. Add or remove lines for more or fewer slots.
slots:
  - "2026-09-23-poster_SNL.md"
  - "2026-08-24-poster_inception_loop_results.md"
#   - "2025-09-15-poster_Stories.md"
#   - "2025-09-15-poster_BQ.md"
---
Posters and talks, with extra figures and material that did not fit on the printed version.

<div class="poster-list" markdown="0">
{% for slot in page.slots %}
  {% if slot and slot != "" %}
    {% assign name = slot | remove: ".md" %}
    {% assign file = "_poster/" | append: name | append: ".md" %}
    {% assign p = site.poster | where: "path", file | first %}
    {% if p %}
  <article class="poster-item">
    <h2 class="poster-item__title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h2>
    {% assign sub = p.subtitle | default: p.summary %}
    {% if sub %}<p class="poster-item__subtitle">{{ sub | strip_html }}</p>{% endif %}
  </article>
    {% else %}
  <p class="poster-item__missing">Slot: no file called <code>_poster/{{ name }}.md</code></p>
    {% endif %}
  {% endif %}
{% endfor %}
</div>