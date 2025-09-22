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
  :root{
    --accent:#7c3aed;           /* violet */
    --accent-2:#a78bfa;         /* lighter violet */
    --ink:#111827;              /* text */
    --muted:#6b7280;            /* muted text */
    --card-bg:#ffffff;          /* cards */
    --card-bd:#e5e7eb;          /* card borders */
    --chip-bg:#f5f3ff;          /* chips */
    --chip-bd:#e9d5ff;
  }

  .pod-wrap{max-width:980px;margin:0 auto;padding:0 1rem 3rem}
  .hero{display:flex;flex-direction:column;gap:.5rem;margin:0 0 1.25rem}
  .hero img{width:100%;height:auto;border-radius:16px;border:1px solid var(--card-bd)}
  .credit{font-style:italic;color:var(--muted)}

  /* Cute modern cards */
  .story-card{
    background:var(--card-bg);
    border:1px solid var(--card-bd);
    border-radius:18px;
    overflow:hidden;
    box-shadow:0 8px 30px rgba(17,24,39,.06);
    margin:1.25rem 0;
  }
  .story-media img{
    width:100%;height:auto;display:block;object-fit:cover;
    aspect-ratio: 16/9;
  }
  .story-body{padding:1rem 1.1rem 1.3rem}
  .story-header{
    display:flex;align-items:center;gap:.6rem;margin-bottom:.6rem
  }
  .pill{
    font-size:.8rem;padding:.28rem .55rem;border-radius:999px;
    background:var(--chip-bg);border:1px solid var(--chip-bd);color:#4c1d95
  }
  .audio-group{
    display:grid;gap:.65rem;margin:.75rem 0 1rem
  }
  .audio-row{
    display:grid;gap:.45rem
  }
  .lang-badge{
    display:inline-flex;align-items:center;gap:.4rem;
    font-size:.86rem;font-weight:600;color:var(--ink)
  }
  .lang-badge .dot{
    width:.55rem;height:.55rem;border-radius:50%;
    background:var(--accent);
    box-shadow:0 0 0 4px rgba(124,58,237,.12)
  }
  audio{width:100%;height:40px;border-radius:10px}
  /* Small helper links under players */
  .mini-links{font-size:.85rem;color:var(--muted);display:flex;gap:.8rem}

  details{
    border:1px solid var(--card-bd);
    border-radius:14px;padding:.85rem 1rem;margin:.6rem 0;background:#fafafa
  }
  details>summary{cursor:pointer;font-weight:700;list-style:none}
  details>summary::-webkit-details-marker{display:none}
  .meta{color:var(--muted);font-size:.92rem}

  h2{margin:1.2rem 0 .4rem}
</style>

<div class="pod-wrap" markdown="0">

  {% if page.hero_image %}
  <header class="hero">
    <img src="{{ page.hero_image | relative_url }}" alt="{{ page.hero_alt | default: 'Episode cover image' }}">
    <p class="credit">Image credit: <i>illustrea</i></p>
  </header>
  {% endif %}

  <h2>Examples of Day 2 Stories</h2>
  <p class="meta">Each card shows the artwork, then the audio in <b>French</b> and <b>English</b>. Tap a summary to read the full text.</p>

  <!-- ===== Story 1 ===== -->
  <article class="story-card">
    <figure class="story-media">
      <!-- replace with your image path -->
      <img src="/assets/stories/story1.jpg" alt="Twilight festival by a fountain in a Mediterranean village with lanterns and art on the walls.">
    </figure>

    <div class="story-body">
      <div class="story-header">
        <span class="pill">Story 1 — Visual</span>
        <span class="meta">visual-modality: optics • color • form</span>
      </div>

      <div class="audio-group">
        <div class="audio-row">
          <span class="lang-badge"><span class="dot"></span> French audio</span>
          <!-- replace src with your FR file -->
          <audio controls preload="metadata" src="/assets/audio/day2/story1-fr.mp3">
            Your browser does not support the audio element.
          </audio>
          <div class="mini-links">
            <a href="/assets/audio/day2/story1-fr.mp3" download>Download FR</a>
          </div>
        </div>
      </div>

      <details>
        <summary>Read story (FR)</summary>
        <p>Dans un petit <b>archipel</b> méditerranéen, Maya, une jeune <b>photographe</b> <b>sportive</b>, vivait dans un ancien <b>appartement</b> transformé en studio. Passionnée d’<b>astronomie</b>, elle passait ses <b>nuits</b> à capturer des <b>images</b> du <b>ciel</b> étoilé avec ses <b>lunettes</b> spécialisées, créant de magnifiques <b>photos</b> des <b>nuages</b> et constellations…</p>
        <p>Guidée par sa <b>vision</b> créative, Maya organisa avec la <b>religieuse</b> du village un festival d’<b>illustration</b> et de <b>photographie</b>…</p>
      </details>

      <details>
        <summary>Read story (EN)</summary>
        <p>In a small Mediterranean <b>archipelago</b>, Maya, a young <b>photographer</b>, <b>sporty</b>, lived in an old <b>apartment</b> turned into a studio. Passionate about <b>astronomy</b>, she spent her <b>nights</b> capturing <b>images</b> of the starry <b>sky</b> with her specialized <b>lenses</b>, creating beautiful <b>photos</b> of the <b>clouds</b> and constellations…</p>
        <p>Guided by her creative <b>vision</b>, Maya organized with the village <b>nun</b> a festival of <b>illustration</b> and <b>photography</b>…</p>
      </details>
    </div>
  </article>

  <!-- ===== Story 2 ===== -->
  <article class="story-card">
    <figure class="story-media">
      <!-- replace with your image path -->
      <img src="/assets/stories/story2.jpg" alt="Cozy brick workshop by the sea where a craftsman and a textile artist work with cotton and tools.">
    </figure>

    <div class="story-body">
      <div class="story-header">
        <span class="pill">Story 2 — Haptic</span>
        <span class="meta">touch • texture • warmth</span>
      </div>

      <div class="audio-group">
        <div class="audio-row">
          <span class="lang-badge"><span class="dot"></span> French audio</span>
          <!-- replace src with your FR file -->
          <audio controls preload="metadata" src="/assets/audio/day2/story2-fr.mp3">
            Your browser does not support the audio element.
          </audio>
          <div class="mini-links">
            <a href="/assets/audio/day2/story2-fr.mp3" download>Download FR</a>
          </div>
        </div>
      </div>

      <details>
        <summary>Read story (FR)</summary>
        <p>Dans une petite maison en <b>brique</b> au bord de la mer, vivait un artisan aux <b>cheveux</b> gris nommé <b>Jean</b>… Ses <b>mains</b> expertes manient chaque <b>outil</b> avec précision…</p>
        <p>Un jour, alors qu’il testait un <b>levier</b> pour <b>ramassage</b> automatique, il fit la rencontre de Léa, une artiste <b>textile</b>…</p>
      </details>

      <details>
        <summary>Read story (EN)</summary>
        <p>In a small <b>brick</b> house by the sea lived a craftsman with gray <b>hair</b> named <b>Jean</b>… His skilled <b>hands</b> handled each <b>tool</b> with precision…</p>
        <p>One day, while testing a <b>lever</b> for automatic <b>pickup</b>, he met Léa, a <b>textile</b> artist…</p>
      </details>
    </div>
  </article>

</div>
