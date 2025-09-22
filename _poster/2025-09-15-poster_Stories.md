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
      
      <img src="/assets/photos/story_1.png" alt="Twilight festival by a fountain in a Mediterranean village with lanterns and art on the walls.">
    </figure>

    <div class="story-body">
      <div class="story-header">
        <span class="pill">Story 1 — Visual</span>
        <span class="meta">visual-modality: optics • color • form</span>
      </div>

      <div class="audio-group">
        <div class="audio-row">
          <span class="lang-badge"><span class="dot"></span> French audio</span>
          <audio controls preload="metadata" src="/assets/audios/story_1_6684_story_9.wav">
            Your browser does not support the audio element.
          </audio>
          <div class="mini-links">
            <a href="/assets/audio/day2/story1-fr.mp3" download>Download FR</a>
          </div>
        </div>
      </div>

      <details>
        <summary>Read story (FR)</summary>
        <p>Dans un petit <b>archipel</b> méditerranéen, Maya, une jeune <b>photographe</b> <b>sportive</b> , vivait dans un ancien <b>appartement <b>transformé en studio. Passionnée d'<b>astronomie</b> , elle passait ses <b>nuits</b> à capturer des <b>images</b> du <b>ciel</b> étoilé avec ses <b>lunettes</b> spécialisées, créant de magnifiques <b>photos</b> des <b>nuages</b> et constellations. Un matin, en explorant les <b>rues</b> du village, elle découvrit derrière un <b>massif</b> de pierres un vieux <b>portail</b> orné d'un <b>dessin</b> représentant une <b>baleine</b> entourée d'un <b>triangle</b> , d'un <b>cercle</b> et d'un <b>ovale</b> . Intriguée, elle décida de <b>lire</b> dans le <b>dictionnaire</b> local la signification de ces <b>symboles</b> , et apprit qu'ils indiquaient l'emplacement d'une ancienne <b>fontaine</b> aux pouvoirs artistiques légendaires. </p>

        <p>Guidée par sa <b>vision</b>  créative, Maya organisa avec la <b>religieuse</b>  du village un festival d'<b>illustration</b>  et de <b>photographie</b> . Elles transformèrent le <b>terrain</b>  autour de la <b>fontaine</b>  en galerie à ciel ouvert, décorant les <b>murs</b>  de <b>miroirs</b> , d'<b>enseignes</b> colorées et de <b>portraits</b> . Des <b>lampes</b>  et <b>lanternes</b>  <b>violettes</b>  illuminent les <b>statues</b>  disposées dans les <b>rues</b> , créant une <b>architecture</b>  <b>visuellement</b>  <b>attractive</b> . Les <b>passagers</b>  des bateaux de croisière venaient désormais admirer cette <b>île</b> devenue célèbre pour sa <b>transparence</b>  artistique, où <b>papillons</b>  et <b>abeilles</b>  voltigeaient entre les œuvres d'art. Le village prospéra grâce à ce projet <b>proprement</b>  magique, transformant un lieu oublié en destination <b>couleur</b>  de rêve pour tous les amateurs d'art et de <b>photographie</b>. </p>
      </details>

      <details>
        <summary>Read story (EN)</summary>
        <p>In a small Mediterranean <b>archipelago</b>, Maya, a young <b>photographer</b>, <b>sporty</b>, lived in an old <b>apartment</b> turned into a studio. Passionate about <b>astronomy</b>, she spent her <b>nights</b> capturing <b>images</b> of the starry <b>sky</b> with her specialized <b>lenses</b>, creating beautiful <b>photos</b> of the <b>clouds</b> and constellations. One morning, while exploring the village <b>streets</b>, she discovered behind a <b>massif</b> of stones an old <b>gate</b> decorated with a <b>drawing</b> of a <b>whale</b> surrounded by a <b>triangle</b>, a <b>circle</b>, and an <b>oval</b>. Intrigued, she decided to <b>read</b> in the local <b>dictionary</b> the meaning of these <b>symbols</b>, and learned that they indicated the location of an ancient <b>fountain</b> with legendary artistic powers.
        </p>
        <p>Guided by her creative <b>vision</b>, Maya organized with the village <b>nun</b> a festival of <b>illustration</b> and <b>photography</b>. They transformed the <b>terrain</b> around the <b>fountain</b> into an open-air gallery, decorating the <b>walls</b> with <b>mirrors</b>, colorful <b>signs</b>, and <b>portraits</b>. <b>Lamps</b> and <b>lanterns</b> <b>violet</b> illuminated the <b>statues</b> set along the <b>streets</b>, creating an <b>architecture</b> <b>visually</b> <b>attractive</b>. The <b>passengers</b> from cruise ships now came to admire this <b>island</b>, famous for its artistic <b>transparency</b>, where <b>butterflies</b> and <b>bees</b> fluttered among the artworks. The village prospered thanks to this <b>properly</b> magical project, turning a forgotten place into a <b>color</b> dream destination for all lovers of art and <b>photography</b>.
        
        </p>
      </details>
    </div>
  </article>

  <!-- ===== Story 2 ===== -->
  <article class="story-card">
    <figure class="story-media">
      <img src="/assets/photos/story_1.png" alt="Cozy brick workshop by the sea where a craftsman and a textile artist work with cotton and tools.">
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
          <audio controls preload="metadata" src="/assets/audios/story_2_6684_story_4.wav">
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
