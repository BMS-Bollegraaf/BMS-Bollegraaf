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
      <a href="/">
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



<!-- FLASHCARDS CONTAINER -->
<div class="flashcards-container cards-per-row-2">
  <!-- CARD 1 -->
  <div class="flashcard">
    <a href="[[BMS\|BMS]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/img/BRS.png" alt="Dashboard 1">
        </div>
        <div class="flashcard-title">Dashboard 1</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 2 -->
  <div class="flashcard">
    <a href="[[Dashboard 2\|Dashboard 2]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/img/dashboard2-image.png" alt="Dashboard 2">
        </div>
        <div class="flashcard-title">Dashboard 2</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 3 -->
  <div class="flashcard">
    <a href="[[Dashboard 3\|Dashboard 3]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/img/dashboard3-image.png" alt="Dashboard 3">
        </div>
        <div class="flashcard-title">Dashboard 3</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 4 -->
  <div class="flashcard">
    <a href="[[Dashboard 4\|Dashboard 4]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/img/dashboard4-image.png" alt="Dashboard 4">
        </div>
        <div class="flashcard-title">Dashboard 4</div>
      </div>
    </a>
  </div>
</div>

<!-- CSS STYLES (Add to your theme CSS or a snippet) -->
<style>
/* Flashcards Container */
.flashcards-container {
  display: grid;
  gap: 20px;
  margin: 30px 0;
  width: 100%;
}

/* Responsive grid layouts */
.cards-per-row-2 {
  grid-template-columns: repeat(2, 1fr);
}

.cards-per-row-3 {
  grid-template-columns: repeat(3, 1fr);
}

.cards-per-row-4 {
  grid-template-columns: repeat(4, 1fr);
}

/* Individual flashcard styles */
.flashcard {
  position: relative;
  height: 240px;
  border-radius: var(--border-radius, 12px);
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
}

.flashcard::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, 
    rgba(255,215,122,0.05) 0%, 
    rgba(224,178,255,0.15) 100%);
  border-radius: inherit;
  z-index: 1;
}

.flashcard::after {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(30, 37, 78, 0.3);
  backdrop-filter: blur(8px);
  border-radius: inherit;
  z-index: 2;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.flashcard:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.3);
}

.flashcard:hover::after {
  opacity: 1;
}

/* Flashcard link (covers entire card) */
.flashcard-link {
  display: block;
  height: 100%;
  width: 100%;
  text-decoration: none;
  color: inherit;
  z-index: 3;
  position: relative;
}

/* Flashcard content container */
.flashcard-content {
  display: flex;
  flex-direction: column;
  height: 100%;
  padding: 0;
  position: relative;
  z-index: 3;
}

/* Image container */
.flashcard-image {
  flex: 1;
  overflow: hidden;
  position: relative;
}

/* Image styling */
.flashcard-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.flashcard:hover .flashcard-image img {
  transform: scale(1.05);
}

/* Title styling */
.flashcard-title {
  background: rgba(18, 20, 42, 0.85);
  color: var(--text-primary, #E0B2FF);
  padding: 12px 16px;
  font-size: 1.1rem;
  font-weight: 600;
  text-align: center;
  border-top: 1px solid rgba(255, 215, 122, 0.3);
  text-shadow: 0 1px 3px rgba(0,0,0,0.5);
}

/* Mobile responsiveness */
@media (max-width: 1024px) {
  .cards-per-row-3, .cards-per-row-4 {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .cards-per-row-2, .cards-per-row-3, .cards-per-row-4 {
    grid-template-columns: 1fr;
  }
  
  .flashcard {
    height: 200px;
  }
}
</style>
