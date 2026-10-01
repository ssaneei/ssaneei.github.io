---
title: "Project 2: Sensorimotor Language Encoding"
subtitle: "SNL poster 2026: more on the figures and stories."
#hero_image: /xx/xx/short_stories.jpeg
#hero_alt: "Stories_Example"
---
[Download Poster (PDF)]({{ '/assets/cv/SarahSaneei_SNL2026.pdf' | relative_url }}){: .btn .btn--primary}

**TL;DR** Using sEEG recorded while patients listen to naturalistic stories, we ask how
sensorimotor features of language (motor, oral, internal and auditory-visual) are encoded
in cortex. Stories were built and validated so that each one emphasises a single dimension,
and word-locked broadband high-frequency activity (BHA) is modelled with epoched ridge
regression on word- and sentence-level LSN composites.

[Overview](#overview) · [Stimuli design](#composition) · [Story design](#design) · [Validation](#validation) · [Planned analysis](#analysis)

## Overview {#overview}

**Poster, SNL 2026.** *Cortical Encoding of Sensorimotor Language Features During Naturalistic Story Listening*

sEEG encoding model · Sandbox · 3 patients · Word- and sentence-level LSN composites · Broadband high-frequency activity (BHA)

## Stimuli design {#composition}

Stories were selected from a larger corpus and assigned to one of four sensorimotor
categories based on LSN composite scores, plus a neutral baseline condition.

**Categories:** Motor · Oral · Internal · Auditory-Visual · Neutral

<!-- Add figures by uncommenting and pointing to your image files, e.g.:
![Story composition overview: distribution of stories across categories and patients](/assets/posters/snl/composition.png)
![LSN composite distributions per category, across all valid words](/assets/posters/snl/lsn-distributions.png)
-->

## Story design {#design}

Each sensorimotor category contains 4 matched stories, plus 4 neutral stories.
Below are example figures for each dimension and for the neutral baseline.

### Motor

<!-- ![Top motor stories](/assets/posters/snl/design-motor.png) -->

### Oral

<!-- ![Top oral stories](/assets/posters/snl/design-oral.png) -->

### Internal

<!-- ![Top internal stories](/assets/posters/snl/design-internal.png) -->

### Auditory-Visual

<!-- ![Top auditory-visual stories](/assets/posters/snl/design-audvis.png) -->

### Neutral

<!-- ![Neutral baseline stories](/assets/posters/snl/design-neutral.png) -->

## Validation {#validation}

Stories and sentences were rated by external participants on all four sensorimotor
dimensions, to check that the LSN-based category assignments match human perception.

<!-- One figure per dimension, e.g.:
![Validation: motor](/assets/posters/snl/validation-motor.png)
![Validation: oral](/assets/posters/snl/validation-oral.png)
![Validation: internal](/assets/posters/snl/validation-internal.png)
![Validation: auditory-visual](/assets/posters/snl/validation-audvis.png)
![Validation: neutral baseline](/assets/posters/snl/validation-neutral.png)
-->

## Planned analysis {#analysis}

1. **BHA epoch extraction.** Word-locked broadband high-gamma (70–150 Hz, z-scored) extracted from sEEG FIF files using `onset_fif` timestamps. Window: −200 ms to +1000 ms around each word onset.
2. **Feature matrix.** Per valid word (identical status, content word, LSN available): 4 LSN composites (motor, oral, internal, auditory-visual) plus control regressors (surprisal, semantic distance, concreteness, valence). About 355–500 valid words per patient.
3. **Epoched ridge regression.** Per electrode × timepoint: BHA ~ LSN composites, with cross-validated lambda selection (5-fold). Outputs: beta coefficients (n_electrodes × n_timepoints × 4) and cross-validated R².
4. **Statistical thresholding.** FDR correction (Benjamini-Hochberg, α = 0.05) across electrode × timepoint cells. Permutation-based p-values planned for publication.
5. **Visualization.** R² heatmap (electrodes × time), temporal beta profiles per dimension, and peak R² projected onto the MNI brain (native and MNI coordinates from BIDS `electrodes.tsv`).

### Features at each level

| Feature | Word-level | Sentence-level | Story-level |
|---|---|---|---|
| **LSN composites** | Motor / Oral / Internal / Audvis | Mean over content words | Mean over sentences |
| **Surprisal** | CamemBERT or trigram? | Mean or sentence LM prob? | — |
| **Semantic distance** | Cosine to context (FastText / CamemBERT, w = 1/3/5) | CamemBERT CLS cosine | Story embedding cosine |
| **Concreteness** | Brysbaert EN (~40k) / Bonin FR (~2k) | Mean over content words | Mean over sentences |
| **Valence** | FANCat FR (1033 words) | Mean or CamemBERT CLS? | Mean or story embedding? |