---
layout: page
title: "Examples of Day2 Stories"
summary: >
  Some examples of the stories played on Day2 of the experiment.
description: "Landing page for the poster QR about data collection — summary."

hero_image: /assets/photos/short_stories.jpeg
hero_alt: "Stories_Example"
---

<style>
  .pod-wrap{max-width:880px;margin:0 auto}
  .hero{display:flex;flex-direction:column;gap:.5rem;margin:0 0 1rem}
  .hero img{width:100%;height:auto;border-radius:14px;border:1px solid var(--card-bd,#e5e7eb)}
  .credit{font-style:italic;color:var(--text-muted,#6b7280)}
  .card{background:var(--card-bg,#fafafa);border:1px solid var(--card-bd,#e5e7eb);border-radius:14px;padding:1rem 1.2rem;margin:1rem 0}
  .callout{border-left:4px solid var(--accent,#6366f1);padding-left:1rem}
  .toc{display:flex;flex-wrap:wrap;gap:.5rem;margin:.5rem 0 1rem}
  .pill{font-size:.85rem;padding:.3rem .6rem;border-radius:999px;background:var(--chip-bg,#eef2ff);border:1px solid var(--chip-bd,#dbeafe)}
  details{border:1px solid var(--card-bd,#e5e7eb);border-radius:12px;padding:.8rem 1rem;margin:.6rem 0;background:var(--card-bg,#fafafa)}
  details > summary{cursor:pointer;font-weight:600;list-style:none}
  details > summary::-webkit-details-marker{display:none}
  h2{margin:1.2rem 0 .6rem}
  h3{margin:.8rem 0 .3rem}
  .small{font-size:.92rem}
  a.button{display:inline-block;padding:.55rem .9rem;border:1px solid var(--card-bd,#e5e7eb);border-radius:.75rem;text-decoration:none}
</style>

<div class="pod-wrap">

  <!-- HERO IMAGE (replace path in front matter) -->
  {% if page.hero_image %}
  <header class="hero">
    <img src="{{ page.hero_image | relative_url }}" alt="{{ page.hero_alt | default: 'Episode cover image' }}">
    <p class="credit">Image: <i>brought to you by illustrea</i></p>
  </header>
  {% endif %}

<div class="pod-wrap" markdown="1">

{% if page.hero_image %}
<header class="hero">
  <img src="{{ page.hero_image | relative_url }}" alt="{{ page.hero_alt | default: 'Episode cover image' }}">
  <p class="credit">Image: <i>brought to you by illustrea</i></p>
</header>
{% endif %}

> This is a Markdown callout rendered inside the box.

## Examples of Day 2 Stories
- Story A — one-line blurb
- Story B — one-line blurb

</div>