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



<!-- Flashcards CSS - Place this at the top of your note -->
<style>
  /* Common styles for all layouts */
  .flashcard-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin: 20px 0;
  }
  
  .flashcard {
    position: relative;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: all 0.3s ease;
    cursor: pointer;
    background-color: var(--background-secondary);
    height: 220px;
    display: flex;
    flex-direction: column;
  }
  
  .flashcard:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  }
  
  .flashcard-image {
    height: 160px;
    width: 100%;
    overflow: hidden;
    position: relative;
  }
  
  .flashcard-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }
  
  .flashcard:hover .flashcard-image img {
    transform: scale(1.05);
  }
  
  .flashcard-title {
    padding: 12px 15px;
    font-weight: 600;
    text-align: center;
    font-size: 1.1em;
    color: var(--text-normal);
    flex-grow: 1;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  /* Two cards per row */
  .flashcard-row-2 .flashcard {
    flex-basis: calc(50% - 10px);
    max-width: calc(50% - 10px);
  }
  
  /* Three cards per row */
  .flashcard-row-3 .flashcard {
    flex-basis: calc(33.333% - 14px);
    max-width: calc(33.333% - 14px);
  }
  
  /* Four cards per row */
  .flashcard-row-4 .flashcard {
    flex-basis: calc(25% - 15px);
    max-width: calc(25% - 15px);
  }
  
  /* Mobile responsiveness */
  @media (max-width: 768px) {
    .flashcard-row-3 .flashcard, 
    .flashcard-row-4 .flashcard {
      flex-basis: calc(50% - 10px);
      max-width: calc(50% - 10px);
    }
  }
  
  @media (max-width: 480px) {
    .flashcard-row-2 .flashcard,
    .flashcard-row-3 .flashcard,
    .flashcard-row-4 .flashcard {
      flex-basis: 100%;
      max-width: 100%;
    }
  }
</style>

<!-- Two Cards Per Row Example -->
<div class="flashcard-container flashcard-row-2">
  <!-- Card 1 -->
  <a href="obsidian://open?vault=DMS&file=BMS" class="flashcard">
    <div class="flashcard-image">
      <img src="img/BRS.png" alt="Card Title 1">
    </div>
    <div class="flashcard-title">Card Title 1</div>
  </a>
  
  <!-- Card 2 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FAnotherNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath2.jpg" alt="Card Title 2">
    </div>
    <div class="flashcard-title">Card Title 2</div>
  </a>
</div>

<!-- Three Cards Per Row Example -->
<div class="flashcard-container flashcard-row-3">
  <!-- Card 1 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FYourNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath1.jpg" alt="Card Title 1">
    </div>
    <div class="flashcard-title">Card Title 1</div>
  </a>
  
  <!-- Card 2 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FAnotherNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath2.jpg" alt="Card Title 2">
    </div>
    <div class="flashcard-title">Card Title 2</div>
  </a>
  
  <!-- Card 3 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FThirdNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath3.jpg" alt="Card Title 3">
    </div>
    <div class="flashcard-title">Card Title 3</div>
  </a>
</div>

<!-- Four Cards Per Row Example -->
<div class="flashcard-container flashcard-row-4">
  <!-- Card 1 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FYourNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath1.jpg" alt="Card Title 1">
    </div>
    <div class="flashcard-title">Card Title 1</div>
  </a>
  
  <!-- Card 2 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FAnotherNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath2.jpg" alt="Card Title 2">
    </div>
    <div class="flashcard-title">Card Title 2</div>
  </a>
  
  <!-- Card 3 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FThirdNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath3.jpg" alt="Card Title 3">
    </div>
    <div class="flashcard-title">Card Title 3</div>
  </a>
  
  <!-- Card 4 -->
  <a href="obsidian://open?vault=YourVaultName&file=Path%2FTo%2FFourthNote" class="flashcard">
    <div class="flashcard-image">
      <img src="YourImagePath4.jpg" alt="Card Title 4">
    </div>
    <div class="flashcard-title">Card Title 4</div>
  </a>
</div>




