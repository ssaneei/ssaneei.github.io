---
layout: archive-taxonomies
type: photography
title: Photography
permalink: /photography/
---

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Photography</title>

  <!-- Use your site CSS if you have one -->
  <link rel="stylesheet" href="style.css">

  <style>
    /* --- Gallery layout --- */
    .photo-page {
      max-width: 1100px;
      margin: 0 auto;
      padding: 2rem 1rem 4rem;
    }
    .photo-title {
      font-size: clamp(1.5rem, 2.5vw, 2rem);
      margin: 0 0 1rem;
      line-height: 1.25;
      letter-spacing: 0.2px;
    }
    .photo-sub {
      color: #666;
      margin-bottom: 1.5rem;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
      gap: 12px;
    }

    .gallery figure {
      position: relative;
      margin: 0;
      overflow: hidden;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,.06);
      background: #f6f6f6;
      transition: transform .2s ease;
    }
    .gallery figure:focus-within,
    .gallery figure:hover { transform: translateY(-2px); }

    .gallery img {
      width: 100%;
      height: 100%;
      display: block;
      object-fit: cover;
      aspect-ratio: 4 / 3; /* keeps rows tidy; remove if you want natural aspect */
    }

    /* Caption overlay (shows on hover desktop, always visible on touch) */
    .gallery figcaption {
      position: absolute;
      inset: auto 0 0 0;
      padding: .65rem .75rem;
      font-size: .95rem;
      color: white;
      background: linear-gradient(to top, rgba(0,0,0,.55), rgba(0,0,0,0));
      opacity: 0;
      transition: opacity .2s ease;
      text-shadow: 0 1px 2px rgba(0,0,0,.5);
    }
    .gallery figure:hover figcaption,
    .gallery figure:focus-within figcaption {
      opacity: 1;
    }
    /* On small screens, keep captions visible for accessibility */
    @media (max-width: 640px) {
      .gallery figcaption { opacity: 1; }
    }

    /* --- Lightbox --- */
    .lightbox {
      position: fixed; inset: 0;
      display: none;
      align-items: center; justify-content: center;
      background: rgba(0,0,0,.9);
      z-index: 9999;
    }
    .lightbox[aria-hidden="false"] { display: flex; }
    .lightbox-inner {
      max-width: min(92vw, 1400px);
      max-height: 88vh;
      display: grid;
      grid-template-rows: 1fr auto;
      gap: .5rem;
      width: 100%;
    }
    .lightbox-img-wrap {
      position: relative;
      overflow: hidden;
      border-radius: 14px;
      box-shadow: 0 10px 30px rgba(0,0,0,.35);
      background: #111;
    }
    .lightbox-img {
      display: block;
      max-width: 100%;
      max-height: 100%;
      margin: 0 auto;
    }
    .lightbox-caption {
      color: #ddd;
      font-size: 1rem;
      line-height: 1.4;
      text-align: center;
    }
    .lightbox-close,
    .lightbox-prev,
    .lightbox-next {
      position: absolute;
      top: 12px;
      padding: .55rem .7rem;
      border-radius: 10px;
      background: rgba(0,0,0,.5);
      backdrop-filter: blur(2px);
      color: #fff;
      border: 1px solid rgba(255,255,255,.2);
      cursor: pointer;
      user-select: none;
      line-height: 1;
    }
    .lightbox-close { right: 12px; }
    .lightbox-prev { left: 12px; top: 50%; transform: translateY(-50%); }
    .lightbox-next { right: 12px; top: 50%; transform: translateY(-50%); }
    .lightbox button:hover { background: rgba(255,255,255,.12); }

    /* Reduce motion */
    @media (prefers-reduced-motion: reduce) {
      .gallery figure { transition: none; }
    }
  </style>
</head>
<body>
  <!-- If you have a site-wide navbar, add a link to this page there like:
       <li><a href="photography.html">Photography</a></li> -->

  <main class="photo-page">
    <h1 class="photo-title">Photography</h1>
    <p class="photo-sub">A selection of moments I’ve captured. Tap an image to view it larger.</p>

    <section class="gallery" id="gallery" aria-label="Photo gallery"></section>
  </main>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox" aria-hidden="true" role="dialog" aria-label="Image viewer">
    <div class="lightbox-inner">
      <div class="lightbox-img-wrap">
        <img id="lightbox-img" class="lightbox-img" alt="">
        <button class="lightbox-close" id="btnClose" aria-label="Close (Esc)">✕</button>
        <button class="lightbox-prev" id="btnPrev" aria-label="Previous (←)">←</button>
        <button class="lightbox-next" id="btnNext" aria-label="Next (→)">→</button>
      </div>
      <div class="lightbox-caption" id="lightbox-cap"></div>
    </div>
  </div>

  <script>

    const PHOTOS = [
      {
        id: "pic1",
        thumb: "{{ '/assets/photos/thumbs/pic1.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic1.jpeg' | relative_url }}",
        alt: "A sunny day in Geneva",
        caption: "A sunny day in Geneva",
        width: 1600, height: 1200
      },
      {
        id: "pic2",
        thumb: "{{ '/assets/photos/thumbs/pic2.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic2.jpeg' | relative_url }}",
        alt: "Sunset in Evian-les-Bains",
        caption: "Sunset in Evian-les-Bains",
        width: 1600, height: 1067
      },
            {
        id: "pic3",
        thumb: "{{ '/assets/photos/thumbs/pic3.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic3.jpeg' | relative_url }}",
        alt: "It's all about shadows.",
        caption: "It's all about shadows.",
        width: 1600, height: 1067
      },
            {
        id: "pic4",
        thumb: "{{ '/assets/photos/thumbs/pic4.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic4.jpeg' | relative_url }}",
        alt: "Bubbles and sunny Geneva facing Jet-d'eau.",
        caption: "Bubbly Jet d'eau in Geneva",
        width: 1600, height: 1067
      },
            {
        id: "pic5",
        thumb: "{{ '/assets/photos/thumbs/pic5.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic5.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic6",
        thumb: "{{ '/assets/photos/thumbs/pic6.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic6.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic7",
        thumb: "{{ '/assets/photos/thumbs/pic7.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic7.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic8",
        thumb: "{{ '/assets/photos/thumbs/pic8.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic8.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic9",
        thumb: "{{ '/assets/photos/thumbs/pic9.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic9.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic10",
        thumb: "{{ '/assets/photos/thumbs/pic10.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic10.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic11",
        thumb: "{{ '/assets/photos/thumbs/pic11.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic11.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic12",
        thumb: "{{ '/assets/photos/thumbs/pic12.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic12.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic13",
        thumb: "{{ '/assets/photos/thumbs/pic13.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic13.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic14",
        thumb: "{{ '/assets/photos/thumbs/pic14.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic14.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      },
            {
        id: "pic15",
        thumb: "{{ '/assets/photos/thumbs/pic15.jpg' | relative_url }}",
        full:  "{{ '/assets/photos/full/pic15.jpeg' | relative_url }}",
        alt: "Rainy city street with reflections and a lone cyclist crossing",
        caption: "Blue hour in the rain",
        width: 1600, height: 1067
      }
      // Add more here...
    ];

    /* ---------------------------------------------------
       2) Render the gallery
       --------------------------------------------------- */
    const galleryEl = document.getElementById('gallery');

    function makeFigure(photo, index) {
      const fig = document.createElement('figure');
      fig.tabIndex = 0;
      fig.dataset.index = index;

      const img = document.createElement('img');
      img.loading = 'lazy';
      img.alt = photo.alt || "";
      if (photo.width && photo.height) {
        img.width = photo.width;
        img.height = photo.height;
      }
      // Optional responsive srcset: add your own sizes if you export multiple thumbs
      // img.srcset = `${photo.thumb.replace('.jpeg','-800.jpeg')} 800w, ${photo.thumb} 1200w`;
      img.src = photo.thumb;

      const cap = document.createElement('figcaption');
      cap.textContent = photo.caption || "";

      fig.appendChild(img);
      fig.appendChild(cap);

      // Click / keyboard to open lightbox
      fig.addEventListener('click', () => openLightbox(index));
      fig.addEventListener('keypress', (e) => {
        if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); openLightbox(index); }
      });

      return fig;
    }

    function renderGallery() {
      const frag = document.createDocumentFragment();
      PHOTOS.forEach((p, i) => frag.appendChild(makeFigure(p, i)));
      galleryEl.appendChild(frag);
    }

    /* ---------------------------------------------------
       3) Lightbox logic (vanilla)
       --------------------------------------------------- */
    const lb = document.getElementById('lightbox');
    const lbImg = document.getElementById('lightbox-img');
    const lbCap = document.getElementById('lightbox-cap');
    const btnClose = document.getElementById('btnClose');
    const btnPrev = document.getElementById('btnPrev');
    const btnNext = document.getElementById('btnNext');

    let currentIndex = 0;

    function preloadAround(idx) {
      [idx-1, idx+1].forEach(i => {
        if (i >= 0 && i < PHOTOS.length) {
          const link = document.createElement('link');
          link.rel = 'preload';
          link.as = 'image';
          link.href = PHOTOS[i].full;
          document.head.appendChild(link);
        }
      });
    }

    function openLightbox(index) {
      currentIndex = index;
      const p = PHOTOS[index];
      lbImg.src = p.full;
      lbImg.alt = p.alt || "";
      lbCap.textContent = p.caption || "";
      lb.setAttribute('aria-hidden', 'false');
      document.body.style.overflow = 'hidden';
      preloadAround(index);
    }

    function closeLightbox() {
      lb.setAttribute('aria-hidden', 'true');
      document.body.style.overflow = '';
      // Optional: clear src to save memory on mobile
      // lbImg.removeAttribute('src');
    }

    function show(delta) {
      currentIndex = (currentIndex + delta + PHOTOS.length) % PHOTOS.length;
      const p = PHOTOS[currentIndex];
      lbImg.src = p.full;
      lbImg.alt = p.alt || "";
      lbCap.textContent = p.caption || "";
      preloadAround(currentIndex);
    }

    btnClose.addEventListener('click', closeLightbox);
    btnPrev.addEventListener('click', () => show(-1));
    btnNext.addEventListener('click', () => show(1));
    lb.addEventListener('click', (e) => {
      // Close if clicking outside the image
      if (e.target === lb) closeLightbox();
    });

    document.addEventListener('keydown', (e) => {
      if (lb.getAttribute('aria-hidden') === 'true') return;
      if (e.key === 'Escape') closeLightbox();
      if (e.key === 'ArrowRight') show(1);
      if (e.key === 'ArrowLeft') show(-1);
    });

    renderGallery();
  </script>
</body>
</html>
