---
{"dg-publish":true,"permalink":"/templates/test-456/","noteIcon":"default"}
---





<div class="flashcard-grid grid-4">
  <div class="flashcard">
    <a href="/BMS">
      <div class="flashcard-image">
        <img 
        src="/img/OfficeBollegraaf.png" 
        alt="BMS">
      </div>
      <div class="flashcard-content">
        <h3>BMS</h3>
        <p>"Office Bollegraaf" — BMS workflow overview</p>
      </div>
    </a>
  </div>
  <div class="flashcard">
    <a href="/PDF-to-Obsidian">
      <div class="flashcard-image">
        <img src="/img/BRS_Shield.png" alt="PDF to Obsidian">
      </div>
      <div class="flashcard-content">
        <h3>PDF to Obsidian</h3>
        <p>"Shield Structure" — How to import PDFs</p>
      </div>
    </a>
  </div>
  <div class="flashcard">
    <a href="/Your-Third-Link">
      <div class="flashcard-image">
        <img src="/img/Your-Third-Image.png" alt="Third Card">
      </div>
      <div class="flashcard-content">
        <h3>Third Card Title</h3>
        <p>"Third Card Description" — Additional information</p>
      </div>
    </a>
  </div>
  <div class="flashcard">
    <a href="/Your-Fourth-Link">
      <div class="flashcard-image">
        <img src="/img/Your-Fourth-Image.png" alt="Fourth Card">
      </div>
      <div class="flashcard-content">
        <h3>Fourth Card Title</h3>
        <p>"Fourth Card Description" — Additional information</p>
      </div>
    </a>
  </div>
</div>
<style>
  /* Container sizing */
  .flashcard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 1rem;
    margin: 1.5em auto;
    max-width: 1200px;
  }
  .grid-4 {
    grid-template-columns: repeat(4, 1fr);
  }
  /* Flashcard styling */
  .flashcard {
    position: relative;
    border-radius: 6px;
    box-shadow: 0 3px 8px rgba(0,0,0,0.3);
    transition: transform 0.3s ease;
    overflow: hidden;
    max-height: 240px; /* Control the maximum height */
  }
  .flashcard:hover {
    transform: translateY(-3px);
  }
  .flashcard a {
    color: inherit;
    text-decoration: none;
    display: block;
  }
  /* Image styling */
  .flashcard-image {
    position: relative;
    width: 100%;
    height: 130px; /* Fixed height for images */
    overflow: hidden;
  }
  .flashcard-image img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover; /* This ensures images cover the area without distortion */
    border-top-left-radius: 6px;
    border-top-right-radius: 6px;
  }
  /* Content styling */
  .flashcard-content {
    padding: 0.75em;
    background: rgba(18, 20, 42, 0.6); /* Cosmic Void @ 60% */
    color: #E0B2FF;                     /* Ethereal Glow */
  }
  .flashcard-content h3 {
    margin-top: 0;
    margin-bottom: 0.25em;
    font-size: 1rem;
  }
  .flashcard-content p {
    margin: 0;
    font-style: italic;
    font-size: 0.8rem;
    line-height: 1.2;
  }
  /* Responsive adjustments */
  @media (max-width: 1200px) {
    .grid-4 {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media (max-width: 768px) {
    .grid-4 {
      grid-template-columns: 1fr;
    }
  }
</style>