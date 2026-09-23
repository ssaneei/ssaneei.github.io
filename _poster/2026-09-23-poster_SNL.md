---
layout: page
title: "Sensorimotor Language Encoding"
summary: >
  More on SNL poster 2026.
#hero_image: /assets/photos/short_stories.jpeg
#hero_alt: "Stories_Example"
---


<title>Sensorimotor Language Encoding</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,400;0,600;1,400&family=Roboto+Slab:wght@400;700&display=swap">

<style>
  :root {
    --bg: #fff;
    --surface: #f8f8f8;
    --border: #c8c8c8;
    --border-light: #e0e0e0;
    --text: #111;
    --text-muted: #666;
    --accent: #003be4;
    --accent-visited: #002aae;
    --label: #828282;
    --figure-bg: #f8f8f8;
    --figure-border: #c8c8c8;
    --table-zebra: #f0f0f0;
    --table-header-bg: #e8e8e8;
    color-scheme: light;
  }

  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --bg: #1a1a1a;
      --surface: #242424;
      --border: #444;
      --border-light: #333;
      --text: #e8e8e8;
      --text-muted: #aaa;
      --accent: #6b8fff;
      --accent-visited: #9ab0ff;
      --label: #888;
      --figure-bg: #242424;
      --figure-border: #444;
      --table-zebra: #2a2a2a;
      --table-header-bg: #333;
      color-scheme: dark;
    }
  }

  :root[data-theme="dark"] {
    --bg: #1a1a1a;
    --surface: #242424;
    --border: #444;
    --border-light: #333;
    --text: #e8e8e8;
    --text-muted: #aaa;
    --accent: #6b8fff;
    --accent-visited: #9ab0ff;
    --label: #888;
    --figure-bg: #242424;
    --figure-border: #444;
    --table-zebra: #2a2a2a;
    --table-header-bg: #333;
    color-scheme: dark;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    line-height: 1.5;
    color: var(--text);
    background: var(--bg);
    padding-inline: 16px;
    padding-block: 0;
  }

  a { color: var(--accent); }
  a:visited { color: var(--accent-visited); }

  code {
    font-family: Inconsolata, 'Courier New', monospace;
    font-size: 0.88em;
    background: var(--surface);
    padding: 0.1em 0.3em;
    border-radius: 3px;
    border: 1px solid var(--border-light);
  }

  /* Nav — Hamilton-style site header */
  nav {
    position: sticky;
    top: env(safe-area-inset-top, 0px);
    background: var(--bg);
    border-bottom: 1px solid var(--border);
    padding-block: 10px;
    display: flex;
    gap: 0;
    overflow-x: auto;
    scrollbar-width: none;
    z-index: 10;
  }
  nav::-webkit-scrollbar { display: none; }
  nav a {
    text-decoration: none;
    font-size: 14px;
    font-weight: 600;
    color: var(--text);
    white-space: nowrap;
    padding: 4px 14px;
    border-right: 1px solid var(--border-light);
    transition: color 0.15s;
  }
  nav a:first-child { padding-left: 0; }
  nav a:hover { color: var(--accent); }

  /* Layout */
  .page {
    max-width: 800px;
    margin-inline: auto;
    padding-block: 40px 80px;
    display: flex;
    flex-direction: column;
    gap: 56px;
  }

  /* Header */
  header { display: flex; flex-direction: column; gap: 10px; }
  .eyebrow {
    font-size: 14px;
    font-weight: 600;
    color: var(--text-muted);
  }
  header h1 {
    font-family: 'Roboto Slab', Georgia, serif;
    font-size: clamp(22px, 3.5vw, 34px);
    font-weight: 700;
    line-height: 1.2;
    color: var(--text);
    text-wrap: balance;
  }
  header p {
    color: var(--text-muted);
    font-size: 16px;
    border-top: 1px solid var(--border-light);
    padding-top: 10px;
    margin-top: 4px;
  }

  /* Section */
  section { display: flex; flex-direction: column; gap: 24px; }

  .section-header {
    border-bottom: 2px solid var(--border);
    padding-bottom: 8px;
    display: flex;
    align-items: baseline;
    gap: 12px;
  }
  .section-header h2 {
    font-family: 'Roboto Slab', Georgia, serif;
    font-size: clamp(18px, 2.5vw, 24px);
    font-weight: 700;
    color: var(--text);
  }
  .section-tag {
    font-size: 13px;
    color: var(--text-muted);
  }

  /* Figure placeholder */
  .figure-slot {
    background: var(--figure-bg);
    border: 2px dashed var(--figure-border);
    padding: 28px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 6px;
    min-height: 160px;
    text-align: center;
  }
  .figure-slot .fig-icon {
    width: 32px;
    height: 32px;
    opacity: 0.3;
  }
  .figure-slot .fig-label {
    font-size: 14px;
    font-weight: 600;
    color: var(--text-muted);
  }
  .figure-slot .fig-desc {
    font-size: 13px;
    color: var(--label);
  }

  /* Grid of figure slots */
  .fig-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
  }
  .fig-grid-2 {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 16px;
  }

  /* Category chips — Hamilton uses minimal styling */
  .dim-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 4px;
  }
  .dim-chip {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 3px 10px;
    font-size: 13px;
    font-weight: 600;
    border: 1px solid;
    border-radius: 2px;
  }
  .dim-chip.motor   { background: #fff5f3; border-color: #cc5540; color: #8b2a1a; }
  .dim-chip.oral    { background: #f0f5ff; border-color: #3060c0; color: #1a3a80; }
  .dim-chip.internal{ background: #f0f8f0; border-color: #3a8050; color: #1a5030; }
  .dim-chip.audvis  { background: #f5f0ff; border-color: #6040b0; color: #3a2070; }
  .dim-chip.neutral { background: var(--surface); border-color: var(--border); color: var(--text-muted); }

  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) .dim-chip.motor    { background: #2a1510; border-color: #cc5540; color: #f0a090; }
    :root:not([data-theme="light"]) .dim-chip.oral     { background: #0e1830; border-color: #3060c0; color: #80a8f0; }
    :root:not([data-theme="light"]) .dim-chip.internal { background: #0e2015; border-color: #3a8050; color: #80c898; }
    :root:not([data-theme="light"]) .dim-chip.audvis   { background: #1a1030; border-color: #6040b0; color: #b098e0; }
  }
  :root[data-theme="dark"] .dim-chip.motor    { background: #2a1510; border-color: #cc5540; color: #f0a090; }
  :root[data-theme="dark"] .dim-chip.oral     { background: #0e1830; border-color: #3060c0; color: #80a8f0; }
  :root[data-theme="dark"] .dim-chip.internal { background: #0e2015; border-color: #3a8050; color: #80c898; }
  :root[data-theme="dark"] .dim-chip.audvis   { background: #1a1030; border-color: #6040b0; color: #b098e0; }

  .dot { width: 7px; height: 7px; border-radius: 50%; background: currentColor; flex-shrink: 0; }

  /* Story group block */
  .story-group {
    border: 1px solid var(--border);
  }
  .story-group-header {
    padding: 10px 14px;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--surface);
  }
  .story-group-header h3 {
    font-size: 15px;
    font-weight: 600;
    color: var(--text);
  }
  .story-group-body { padding: 16px; display: flex; flex-direction: column; gap: 12px; }

  /* Analysis steps */
  .analysis-list { display: flex; flex-direction: column; gap: 16px; }
  .analysis-item { display: flex; gap: 14px; align-items: flex-start; }
  .analysis-num {
    flex-shrink: 0;
    width: 26px;
    height: 26px;
    background: var(--text);
    color: var(--bg);
    font-size: 12px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 2px;
    font-family: 'Roboto Slab', serif;
  }
  .analysis-item h4 {
    font-size: 15px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 3px;
  }
  .analysis-item p {
    font-size: 14px;
    color: var(--text-muted);
  }

  /* Feature table */
  .feature-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 14px;
  }
  .feature-table th {
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
    text-align: left;
    padding: 8px 12px;
    background: var(--table-header-bg);
    border: 1px solid var(--border);
  }
  .feature-table td {
    padding: 8px 12px;
    border: 1px solid var(--border);
    color: var(--text-muted);
    vertical-align: top;
  }
  .feature-table td:first-child {
    font-weight: 600;
    color: var(--text);
  }
  .feature-table tr:nth-child(even) td { background: var(--table-zebra); }
  .table-wrap { overflow-x: auto; }

  p { font-size: 16px; color: var(--text-muted); }

  @media (max-width: 600px) {
    body { font-size: 16px; }
    .dim-chip { font-size: 12px; }
  }
</style>

<nav>
  <a href="#overview">Overview</a>
  <a href="#composition">Composition</a>
  <a href="#design">Story Design</a>
  <a href="#validation">Validation</a>
  <a href="#analysis">Analysis</a>
</nav>

<div class="page">

  <header id="overview">
    <div class="eyebrow">Poster — SNL 6</div>
    <h1>Cortical Encoding of Sensorimotor Language Features During Naturalistic Story Listening</h1>
    <p>sEEG encoding model · Sandbox · 3 patients · Word- and sentence-level LSN composites · Broadband high-gamma activity</p>
  </header>

  <!-- STIMULI COMPOSITION -->
  <section id="composition">
    <div class="section-header">
      <h2>Stimuli Design</h2>
      <span class="section-tag">Final Composition</span>
    </div>

    <p style="color:var(--text-muted); font-size:14px;">
      Stories were selected from a larger corpus and assigned to one of four sensorimotor categories based on LSN composite scores, plus a neutral baseline condition.
    </p>

    <div class="dim-row">
      <span class="dim-chip motor"><span class="dot"></span>Motor</span>
      <span class="dim-chip oral"><span class="dot"></span>Oral</span>
      <span class="dim-chip internal"><span class="dot"></span>Internal</span>
      <span class="dim-chip audvis"><span class="dot"></span>Auditory-Visual</span>
      <span class="dim-chip neutral"><span class="dot"></span>Neutral</span>
    </div>

    <div class="fig-grid-2">
      <div class="figure-slot">
        <svg class="fig-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
          <rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18M9 21V9"/>
        </svg>
        <div class="fig-label">Story composition overview</div>
        <div class="fig-desc">Distribution of stories across categories and patients</div>
      </div>
      <div class="figure-slot">
        <svg class="fig-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
          <circle cx="12" cy="12" r="9"/><path d="M12 3v9l5 3"/>
        </svg>
        <div class="fig-label">LSN composite distributions</div>
        <div class="fig-desc">Per-category score distributions across all valid words</div>
      </div>
    </div>
  </section>

  <!-- STORY DESIGN -->
  <section id="design">
    <div class="section-header">
      <h2>Story Design</h2>
      <span class="section-tag">4 stories per category + 4 neutral</span>
    </div>

    <p style="color:var(--text-muted); font-size:14px;">
      Each sensorimotor category contains 4 matched stories. Below are example figures for each dimension and the neutral baseline.
    </p>

    <!-- Motor -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip motor" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Motor</span>
        <h3>Top motor stories</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Motor</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Motor</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Oral -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip oral" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Oral</span>
        <h3>Top oral stories</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Oral</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Oral</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Internal -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip internal" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Internal</span>
        <h3>Top internal stories</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Internal</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Internal</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Auditory-Visual -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip audvis" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Auditory-Visual</span>
        <h3>Top auditory-visual stories</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Auditory-Visual</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Auditory-Visual</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Neutral -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip neutral" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Neutral</span>
        <h3>Neutral baseline stories</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Neutral</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Neutral</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

  </section>

  <!-- VALIDATION -->
  <section id="validation">
    <div class="section-header">
      <h2>Stimuli Validation</h2>
      <span class="section-tag">Behavioral ratings</span>
    </div>

    <p style="color:var(--text-muted); font-size:14px;">
      Stories and sentences were rated by external participants on all four sensorimotor dimensions to validate that LSN-based category assignments matched human perception.
    </p>

    <!-- Motor -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip motor" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Motor</span>
        <h3>Validation — Motor</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Motor validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Motor validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Oral -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip oral" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Oral</span>
        <h3>Validation — Oral</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Oral validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Oral validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Internal -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip internal" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Internal</span>
        <h3>Validation — Internal</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Internal validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Internal validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Auditory-Visual -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip audvis" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Auditory-Visual</span>
        <h3>Validation — Auditory-Visual</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Audvis validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Audvis validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Neutral -->
    <div class="story-group">
      <div class="story-group-header">
        <span class="dim-chip neutral" style="font-size:12px;padding:4px 10px;"><span class="dot"></span>Neutral</span>
        <h3>Validation — Neutral baseline</h3>
      </div>
      <div class="story-group-body">
        <div class="fig-grid">
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Neutral validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
          <div class="figure-slot" style="min-height:140px">
            <div class="fig-label">Figure — Neutral validation</div>
            <div class="fig-desc">Add plot here</div>
          </div>
        </div>
      </div>
    </div>

  </section>

  <!-- PLANNED ANALYSIS -->
  <section id="analysis">
    <div class="section-header">
      <h2>Planned Analysis</h2>
      <span class="section-tag">Encoding model</span>
    </div>

    <div class="analysis-list">
      <div class="analysis-item">
        <div class="analysis-num">1</div>
        <div>
          <h4>BHA Epoch Extraction</h4>
          <p>Word-locked broadband high-gamma (70–150 Hz, z-scored) extracted from sEEG FIF files using <code>onset_fif</code> timestamps. Window: −200 ms to +1000 ms per word onset.</p>
        </div>
      </div>
      <div class="analysis-item">
        <div class="analysis-num">2</div>
        <div>
          <h4>Feature Matrix</h4>
          <p>Per valid word (identical status, content word, LSN available): 4 LSN composites (motor, oral, internal, auditory-visual) + control regressors (surprisal, semantic distance, concreteness, valence). Valid words: ~355–500 per patient.</p>
        </div>
      </div>
      <div class="analysis-item">
        <div class="analysis-num">3</div>
        <div>
          <h4>Epoched Ridge Regression</h4>
          <p>Per electrode × timepoint: BHA ~ LSN composites, cross-validated lambda selection (5-fold). Outputs: beta coefficients (n_electrodes × n_timepoints × 4) and cross-validated R².</p>
        </div>
      </div>
      <div class="analysis-item">
        <div class="analysis-num">4</div>
        <div>
          <h4>Statistical Thresholding</h4>
          <p>FDR correction (Benjamini-Hochberg, α = 0.05) across electrode × timepoint cells. Permutation-based p-values planned for publication.</p>
        </div>
      </div>
      <div class="analysis-item">
        <div class="analysis-num">5</div>
        <div>
          <h4>Visualization</h4>
          <p>R² heatmap (electrodes × time), temporal beta profiles per dimension, peak R² projected onto MNI brain (native + MNI coordinates from BIDS electrodes.tsv).</p>
        </div>
      </div>
    </div>

    <div class="table-wrap" style="margin-top:8px;">
      <table class="feature-table">
        <thead>
          <tr>
            <th>Feature</th>
            <th>Word-level</th>
            <th>Sentence-level</th>
            <th>Story-level</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>LSN composites</td>
            <td>Motor / Oral / Internal / Audvis</td>
            <td>Mean over content words</td>
            <td>Mean over sentences</td>
          </tr>
          <tr>
            <td>Surprisal</td>
            <td>CamemBERT or trigram?</td>
            <td>Mean or sentence LM prob?</td>
            <td>—</td>
          </tr>
          <tr>
            <td>Semantic distance</td>
            <td>Cosine to context (FastText / CamemBERT, w=1/3/5)</td>
            <td>CamemBERT CLS cosine</td>
            <td>Story embedding cosine</td>
          </tr>
          <tr>
            <td>Concreteness</td>
            <td>Brysbaert EN (~40k) / Bonin FR (~2k)</td>
            <td>Mean over content words</td>
            <td>Mean over sentences</td>
          </tr>
          <tr>
            <td>Valence</td>
            <td>FANCat FR (1033 words)</td>
            <td>Mean or CamemBERT CLS?</td>
            <td>Mean or story embedding?</td>
          </tr>
        </tbody>
      </table>
    </div>

  </section>

</div>