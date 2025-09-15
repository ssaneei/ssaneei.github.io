---
layout: page
title: "🎙️ Where Does Meaning Live? Four Theories, One Brain"
summary: >
  One of the most interesting challenges in neuroscience is where meaning locates in the brain. Here we share 4 different results based 4 lines of studies.
description: "Landing page for the poster QR — summary, audio, and credits."


hero_image: /assets/photos/meaning.png
hero_alt: "Four theories, one brain"
audio_src: /assets/audios/meaning-episode.mp4
audio_title: "Where Does Meaning Live? (Short Cut)"
notebooklm_url: https://notebooklm.google.com/notebook/f163972d-b36f-4fdf-af4e-f3416d89f409?artifactId=6ae5cf55-13e9-42af-9fab-9bc2afa8fbd6
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
  .audio-card audio{width:100%;margin-top:.25rem}
  a.button{display:inline-block;padding:.55rem .9rem;border:1px solid var(--card-bd,#e5e7eb);border-radius:.75rem;text-decoration:none}
</style>

<div class="pod-wrap">

  <!-- HERO IMAGE (replace path in front matter) -->
  {% if page.hero_image %}
  <header class="hero">
    <img src="{{ page.hero_image | relative_url }}" alt="{{ page.hero_alt | default: 'Episode cover image' }}">
    <p class="credit">Image: <i>brought to you by illustrae</i></p>
  </header>
  {% endif %}

  <!-- AUDIO PLAYER (use /assets/audio/... mp3 in front matter) -->
  <section class="card audio-card">
    <h2>▶️ Listen to the Episode</h2>
    {% if page.audio_src %}
      <p class="small">{{ page.audio_title | default: 'Episode audio' }}</p>
      <audio controls preload="metadata">
        <source src="{{ page.audio_src | relative_url }}" type="audio/mpeg">
        Your browser doesn’t support the audio element. You can <a href="{{ page.audio_src | relative_url }}">download the MP3</a>.
      </audio>
      {% if page.notebooklm_url %}
      <p class="small" style="margin-top:.5rem">
        Or listen externally on
        <a class="button" href="{{ page.notebooklm_url }}" target="_blank" rel="noopener">NotebookLM</a>
      </p>
      {% endif %}
    {% else %}
      <p class="small">The audio file is generated using Google NotebookLM.</p>
      {% if page.notebooklm_url %}
      <p><a class="button" href="{{ page.notebooklm_url }}" target="_blank" rel="noopener">Open in NotebookLM</a></p>
      {% else %}
      <p class="credit">Add an MP3 at <code>/assets/audio/...</code> and set <code>audio_src</code> in the front matter to show the player.</p>
      {% endif %}
    {% endif %}
  </section>

  <p class="credit">Text: <i>brought to you by ChatGPT [edited]</i></p>

  <section class="card callout">
    <strong>TL;DR</strong> Meaning isn’t in a single “spot.” Evidence points to a distributed network with influential hubs
    (notably <em>ATL</em>, <em>pMTG</em>, and <em>angular gyrus</em>) working together.
  </section>

  <nav class="toc" aria-label="Episode sections">
    <a class="pill" href="#intro">Intro</a>
    <a class="pill" href="#collins-2017">Collins et&nbsp;al. (2017)</a>
    <a class="pill" href="#matchin-2022">Matchin et&nbsp;al. (2022)</a>
    <a class="pill" href="#huth-2016">Huth et&nbsp;al. (2016)</a>
    <a class="pill" href="#caucheteux-2022">Caucheteux et&nbsp;al. (2022)</a>
    <a class="pill" href="#wrap-up">Wrap-Up</a>
  </nav>

  <section id="intro">
    <h2>🎙️ Episode Intro</h2>
    <p class="small"><em>[Intro Music Fades In]</em></p>
    <p><strong>Host:</strong> Welcome back to <em>Brains Explained</em>, the show where we dive into the latest neuroscience and cognitive science to figure out how our minds work.</p>
    <p>Today’s question: <strong>Where does meaning live in the brain?</strong> We’ll explore four landmark papers — each with a different take — and see how the field is moving from single hotspots to big networks.</p>
  </section>

  <section id="collins-2017">
    <h2>Segment 1 — Collins et&nbsp;al. (2017): The ATL Hub</h2>
    <details open>
      <summary>Key idea</summary>
      <p>Degeneration of the <strong>anterior temporal lobe (ATL)</strong> in semantic variant PPA leads to loss of word meaning.</p>
      <p>Conclusion: ATL works as a <em>semantic hub</em> integrating vision, hearing, and memory.</p>
    </details>
  </section>

  <section id="matchin-2022">
    <h2>Segment 2 — Matchin et&nbsp;al. (2022): The pMTG Solution</h2>
    <details>
      <summary>Key idea</summary>
      <p>Lesion–symptom mapping points to <strong>posterior middle temporal gyrus (pMTG)</strong> as key for comprehension, rather than classic Wernicke’s area.</p>
      <p>Conclusion: Meaning is more posterior; <strong>pMTG</strong> links word forms to concepts.</p>
    </details>
  </section>

  <section id="huth-2016">
    <h2>Segment 3 — Huth et&nbsp;al. (2016): Meaning Everywhere</h2>
    <details>
      <summary>Key idea</summary>
      <p>Natural-speech fMRI reveals widespread “<strong>semantic maps</strong>” across temporal, parietal, and frontal cortices for different categories.</p>
      <p>Conclusion: Meaning is <strong>distributed</strong> across cortex.</p>
    </details>
  </section>

  <section id="caucheteux-2022">
    <h2>Segment 4 — Caucheteux et&nbsp;al. (2022): Networks and Hubs</h2>
    <details>
      <summary>Key idea</summary>
      <p>Brain activity compared to deep language models shows both widespread activation and <strong>key hotspots</strong> (ATL, pMTG, angular gyrus) predictive of semantic content.</p>
      <p>Conclusion: It’s distributed <em>and</em> organized around crucial hubs.</p>
    </details>
  </section>

  <section id="wrap-up" class="card">
    <h2>Wrap-Up</h2>
    <p><strong>Collins:</strong> ATL is the hub. <strong>Matchin:</strong> pMTG is the hub. <strong>Huth:</strong> meaning is everywhere. <strong>Caucheteux:</strong> both are right — it’s distributed, with key nodes doing heavy lifting.</p>
    <p>The field converges on a <strong>network model</strong>: meaning emerges from patterns across the brain, with a few areas playing outsized roles.</p>
  </section>

  <footer>
    <p class="credit">Text: <i>brought to you by ChatGPT [edited]</i></p>
    <p class="small"><a href="{{ '/' | relative_url }}">← Back to home</a></p>
  </footer>

</div>
