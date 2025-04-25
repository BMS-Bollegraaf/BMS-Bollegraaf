---
{"dg-publish":true,"permalink":"/test-456/","noteIcon":"default"}
---

<div class="flashcard-grid grid-2">
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
</div>

<style>
  /* Container sizing */
  .flashcard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin: 2em auto;
    max-width: 1200px;
  }

  .grid-2 {
    grid-template-columns: repeat(2, 1fr);
  }

  /* Flashcard styling */
  .flashcard {
    position: relative;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    transition: transform 0.3s ease;
    overflow: hidden;
  }

  .flashcard:hover {
    transform: translateY(-5px);
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
    overflow: hidden;
  }

  .flashcard-image img {
    display: block;
    width: 100%;
    height: auto;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
  }

  /* Content styling */
  .flashcard-content {
    padding: 1em;
    background: rgba(18, 20, 42, 0.6); /* Cosmic Void @ 60% */
    color: #E0B2FF;                     /* Ethereal Glow */
  }

  .flashcard-content h3 {
    margin-top: 0;
    margin-bottom: 0.5em;
    font-size: 1.2rem;
  }

  .flashcard-content p {
    margin: 0;
    font-style: italic;
    font-size: 0.9rem;
  }

  /* Responsive adjustments */
  @media (max-width: 768px) {
    .grid-2 {
      grid-template-columns: 1fr;
    }
  }
</style>
