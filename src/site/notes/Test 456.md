---
{"dg-publish":true,"permalink":"/test-456/","noteIcon":"default"}
---

<!-- 1) Swiper core CSS -->
<link
  rel="stylesheet"
  href="https://unpkg.com/swiper@11/swiper-bundle.min.css"
/>
<!-- 2) Swiper JS -->
<script src="https://unpkg.com/swiper@11/swiper-bundle.min.js"></script>

<div class="swiper myFlashcardSwiper">
  <div class="swiper-wrapper">
    <!-- Slide 1 -->
    <div class="swiper-slide">
      <a href="/BMS">
        <img
          src="/img/BRS.png"
          alt="Journal"
          class="flashcard-slide"
        />
        <div class="overlay-caption">
          <h3>Journal</h3>
          <p>Log your thoughts, reflections & insights.</p>
        </div>
      </a>
    </div>
    <!-- Slide 2 -->
    <div class="swiper-slide">
      <a href="/Projects">
        <img
          src="/img/projects.png"
          alt="Projects"
          class="flashcard-slide"
        />
        <div class="overlay-caption">
          <h3>Projects</h3>
          <p>Track and map out your ongoing quests.</p>
        </div>
      </a>
    </div>
  </div>

  <!-- Navigation buttons -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
</div>

<style>
  /* Container sizing */
  .myFlashcardSwiper {
    width: 100%;
    max-width: 800px;
    margin: 2em auto;
    position: relative;
  }

  /* Ensure slide wrapper is positioned for caption overlay */
  .swiper-slide {
    position: relative;
  }

  /* Images */
  .flashcard-slide {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
  }

  /* Overlay caption styling */
  .overlay-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 1em;
    background: rgba(18, 20, 42, 0.6); /* Cosmic Void @ 60% */
    color: #E0B2FF;                     /* Ethereal Glow */
    text-align: center;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
  }

  .overlay-caption h3 {
    margin: 0 0 0.3em 0;
    font-size: 1.2rem;
  }

  .overlay-caption p {
    margin: 0;
    font-size: 0.9rem;
    font-style: italic;
  }

  /* Swiper nav arrow colors */
  .swiper-button-prev,
  .swiper-button-next {
    color: #BFA6E0; /* Nebula Lavender */
  }
</style>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    new Swiper('.myFlashcardSwiper', {
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
