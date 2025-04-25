---
{"dg-publish":true,"permalink":"/test-123/","noteIcon":"default"}
---


<!-- COSMIC THEME FLASHCARDS (3 per row) -->
<div class="flashcards-cosmic cards-per-row-3">
  <!-- CARD 1 -->
  <div class="flashcard-cosmic">
    <a href="[[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]]" class="flashcard-cosmic-link">
      <div class="flashcard-cosmic-image">
        <img src="/IMG/OfficeBollegraaf.png" alt="Projects Dashboard">
      </div>
      <div class="flashcard-cosmic-content">
        <div class="flashcard-cosmic-title">Projects</div>
        <div class="flashcard-cosmic-glow"></div>
      </div>
    </a>
  </div>
  
  <!-- CARD 2 -->
  <div class="flashcard-cosmic">
    <a href="[[BMS\|BMS]]" class="flashcard-cosmic-link">
      <div class="flashcard-cosmic-image">
        <img src="/IMG/StructureBRS.png" alt="Health Dashboard">
      </div>
      <div class="flashcard-cosmic-content">
        <div class="flashcard-cosmic-title">Health</div>
        <div class="flashcard-cosmic-glow"></div>
      </div>
    </a>
  </div>
  
  <!-- CARD 3 -->
  <div class="flashcard-cosmic">
    <a href="[[PDF to Obsidian\|PDF to Obsidian]]" class="flashcard-cosmic-link">
      <div class="flashcard-cosmic-image">
        <img src="/IMG/VanDyk.png" alt="Learning Dashboard">
      </div>
      <div class="flashcard-cosmic-content">
        <div class="flashcard-cosmic-title">Learning</div>
        <div class="flashcard-cosmic-glow"></div>
      </div>
    </a>
  </div>
</div>

<!-- CSS STYLES (Add to your theme CSS or a snippet) -->
<style>
/* Shared Grid Styles */
.flashcards-glass,
.flashcards-cosmic,
.flashcards-minimal {
  display: grid;
  gap: 20px;
  margin: 30px 0;
  width: 100%;
}

/* Row configuration */
.cards-per-row-2 {
  grid-template-columns: repeat(2, 1fr);
}

.cards-per-row-3 {
  grid-template-columns: repeat(3, 1fr);
}

.cards-per-row-4 {
  grid-template-columns: repeat(4, 1fr);
}

/* ===== GLASS MORPHISM STYLE ===== */
.flashcard-glass {
  position: relative;
  height: 220px;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
}

.flashcard-glass:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
}

.flashcard-glass-link {
  display: block;
  height: 100%;
  width: 100%;
  text-decoration: none;
}

.flashcard-glass-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.flashcard-glass-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.flashcard-glass:hover .flashcard-glass-image img {
  transform: scale(1.1);
}

.flashcard-glass-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(18, 20, 42, 0.3);
  backdrop-filter: blur(4px);
  z-index: 2;
  transition: backdrop-filter 0.3s ease;
}

.flashcard-glass:hover .flashcard-glass-overlay {
  backdrop-filter: blur(0px);
  background: rgba(18, 20, 42, 0.1);
}

.flashcard-glass-title {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 16px;
  color: var(--text-primary, #E0B2FF);
  font-size: 1.3rem;
  font-weight: bold;
  text-align: center;
  background: rgba(30, 37, 78, 0.8);
  backdrop-filter: blur(10px);
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  z-index: 3;
  transform: translateY(0);
  transition: transform 0.3s ease;
}

.flashcard-glass:hover .flashcard-glass-title {
  transform: translateY(0);
  background: rgba(30, 37, 78, 0.95);
}

/* ===== COSMIC THEME STYLE ===== */
.flashcard-cosmic {
  position: relative;
  height: 260px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.3);
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  background: linear-gradient(135deg, rgba(96, 108, 136, 0.2), rgba(30, 37, 78, 0.6));
  border: 1px solid rgba(108, 120, 156, 0.3);
}

.flashcard-cosmic:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
  border-color: rgba(224, 178, 255, 0.3);
}

.flashcard-cosmic-link {
  display: block;
  height: 100%;
  width: 100%;
  text-decoration: none;
}

.flashcard-cosmic-image {
  height: 80%;
  width: 100%;
  overflow: hidden;
}

.flashcard-cosmic-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}

.flashcard-cosmic:hover .flashcard-cosmic-image img {
  transform: scale(1.1);
}

.flashcard-cosmic-content {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 20%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(18, 20, 42, 0.8);
  border-top: 1px solid rgba(255, 215, 122, 0.2);
}

.flashcard-cosmic-title {
  color: var(--text-accent, #FFD77A);
  font-size: 1.2rem;
  font-weight: 600;
  text-align: center;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
  z-index: 2;
}

.flashcard-cosmic-glow {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 80%;
  height: 3px;
  background: linear-gradient(90deg, 
    rgba(224, 178, 255, 0), 
    rgba(224, 178, 255, 1), 
    rgba(224, 178, 255, 0));
  filter: blur(1px);
  opacity: 0.6;
  transition: all 0.3s ease;
}

.flashcard-cosmic:hover .flashcard-cosmic-glow {
  width: 100%;
  opacity: 1;
  filter: blur(2px);
}

/* ===== MINIMALIST STYLE ===== */
.flashcard-minimal {
  height: 180px;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  transition: all 0.25s ease;
  background: var(--background-primary-alt, rgba(18, 20, 42, 0.85));
}

.flashcard-minimal:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.flashcard-minimal-link {
  display: block;
  height: 100%;
  width: 100%;
  text-decoration: none;
}

.flashcard-minimal-image {
  height: 75%;
  width: 100%;
  overflow: hidden;
}

.flashcard-minimal-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.flashcard-minimal:hover .flashcard-minimal-image img {
  transform: scale(1.05);
}

.flashcard-minimal-title {
  height: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-normal, #CFDACB);
  font-size: 1rem;
  font-weight: 500;
  background: var(--background-secondary, #1E254E);
  padding: 8px;
  text-align: center;
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
  
  .flashcard-glass,
  .flashcard-cosmic,
  .flashcard-minimal {
    height: 200px;
  }
}
</style>
