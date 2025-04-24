---
{"dg-publish":true,"permalink":"/test-file/","noteIcon":"default"}
---






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
      <a href="/PDF-to-Obsidian">
        <img
          src="/img/BRS_Shield.png"
          alt="PDF to Obsidian"
          class="art-slide"
        />
        <div class="overlay-caption">
          “Shield Structure” — How to import PDFs
        </div>
      </a>
    </div>
    <!-- Slide 2 -->
    <div class="swiper-slide">
      <a href="/BMS">
        <img
          src="/img/OfficeBollegraaf.png"
          alt="BMS"
          class="art-slide"
        />
        <div class="overlay-caption">
          “Office Bollegraaf” — BMS workflow overview
        </div>
      </a>
    </div>
    <!-- Add more slides here, following the same pattern -->
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

  /* Ensure slide wrapper is positioned for caption overlay */
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

  /* Overlay caption at bottom of image */
  .overlay-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 1em;
    background: rgba(18, 20, 42, 0.6); /* Cosmic Void @ 60% */
    color: #E0B2FF;                     /* Ethereal Glow */
    font-style: italic;
    font-size: 1rem;
    text-align: center;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
  }

  /* Back button styling */
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

  /* Swiper nav arrow colors */
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







[Open Excel Template](./Templates/YourTemplate.xlsx)



[Launch Excel Template](file:///C:\Users\k.mooibroek\OneDrive - Bollegraaf Recycling Solutions\Attachments)

[Launch Excel Template](file:///C:/Users/k.mooibroek/OneDrive%20-%20Bollegraaf%20Recycling%20Solutions/Attachments\book1.xlsx)


[Open Template](file:///../OneDrive%20-%20Bollegraaf%20Recycling%20Solutions/Attachments/book1.xlsx)


file:///%UserProfile%/OneDrive%20-%20Bollegraaf%20Recycling%20Solutions/Attachments/book1.xlsx
