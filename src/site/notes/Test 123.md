---
{"dg-publish":true,"permalink":"/test-123/","noteIcon":"default"}
---

<div class="flashcard-grid grid-2">
  <div class="flashcard">
    <a href="BMS">
      <div class="flashcard-image">
        <img src="/IMG/BRS.png" alt="Journal">
      </div>
      <div class="flashcard-content">
        <h3>Journal</h3>
        <p>Log your thoughts, reflections & insights.</p>
      </div>
    </a>
  </div>

  <div class="flashcard">
    <a href="Projects">
      <div class="flashcard-image">
        <img src="/img/projects.png" alt="Projects">
      </div>
      <div class="flashcard-content">
        <h3>Projects</h3>
        <p>Track and map out your ongoing quests.</p>
      </div>
    </a>
  </div>
</div>



<!-- 1) Swiper core CSS -->
<link
  rel="stylesheet"
  href="https://unpkg.com/swiper@11/swiper-bundle.min.css"
/>
<!-- 2) Swiper JS -->
<script src="https://unpkg.com/swiper@11/swiper-bundle.min.js"></script>

<div class="swiper myArtSwiper">
  <div class="swiper-wrapper">
    <!-- Slide 1 -->
    <div class="swiper-slide">
      <img
        src="/img/StructureBRS.png"
        alt="StructureBRS"
        class="art-slide"
      />
      <div class="overlay-caption">
        “First piece” — My commentary here
      </div>
    </div>
    <!-- Slide 2 -->
    <div class="swiper-slide">
      <img
        src="/img/BRS.png"
        alt="BRS"
        class="art-slide"
      />
      <div class="overlay-caption">
        “Second piece” — More text
      </div>
    </div>
    <!-- Add more slides here -->
  </div>

  <!-- Navigation buttons -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>

  <!-- Back to Dashboard -->
  <div class="back-btn">
    <a href="/Leaf’s-Observatory">← Back to Observatory</a>
  </div>
</div>

<style>
  /* Container sizing */
  .myArtSwiper {
    width: 100%;
    max-width: 800px;
    margin: 2em auto;
    position: relative;
  }

  /* Each slide is positioned relative to contain overlay */
  .swiper-slide {
    position: relative;
  }

  /* Images */
  .art-slide {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
  }

  /* Overlay caption */
  .overlay-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 1em;
    background: rgba(18, 20, 42, 0.6); /* Cosmic Void at 60% opacity */
    color: #E0B2FF;                     /* Ethereal Glow */
    font-style: italic;
    font-size: 1rem;
    text-align: center;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
  }

  /* Back button */
  .back-btn {
    text-align: center;
    margin: 1.5em 0;
  }
  .back-btn a {
    color: #8AD6EE; /* Comet Trail */
    text-decoration: none;
    font-weight: bold;
  }
  .back-btn a:hover {
    text-decoration: underline;
  }

  /* Override Swiper navigation colors (optional) */
  .swiper-button-prev,
  .swiper-button-next {
    color: #BFA6E0; /* Nebula Lavender */
  }
</style>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    new Swiper('.myArtSwiper', {
      loop: true,
      speed: 600,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
      effect: 'fade',
      fadeEffect: { crossFade: true },
    });
  });
</script>
