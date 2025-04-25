---
{"dg-publish":true,"permalink":"/test-123/","noteIcon":"default"}
---

<!-- APPROACH 1: DIRECT WIKI LINKS (Best for Obsidian) -->
<div class="flashcards-container cards-per-row-3">
  <!-- CARD 1 -->
  <div class="flashcard">
    <a href="[[IT/Applications/TOPDesk/TOPdesk\|TOPdesk]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/OfficeBollegraaf.png" alt="TOPdesk System">
        </div>
        <div class="flashcard-title">TOPdesk</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 2 -->
  <div class="flashcard">
    <a href="[[BMS\|BMS]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/StructureBRS.png" alt="BMS System">
        </div>
        <div class="flashcard-title">BMS</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 3 -->
  <div class="flashcard">
    <a href="[[PDF to Obsidian\|PDF to Obsidian]]" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/VanDyk.png" alt="PDF Converter">
        </div>
        <div class="flashcard-title">PDF to Obsidian</div>
      </div>
    </a>
  </div>
</div>

<!-- APPROACH 2: EXPLICIT PATH LINKS (Alternative for Digital Garden) -->
<div class="flashcards-container cards-per-row-2">
  <!-- CARD 1 -->
  <div class="flashcard glass">
    <a href="/topdesk" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/OfficeBollegraaf.png" alt="TOPdesk System">
        </div>
        <div class="flashcard-title">TOPdesk</div>
      </div>
    </a>
  </div>
  
  <!-- CARD 2 -->
  <div class="flashcard glass">
    <a href="/bms" class="flashcard-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/StructureBRS.png" alt="BMS System">
        </div>
        <div class="flashcard-title">BMS</div>
      </div>
    </a>
  </div>
</div>

<!-- APPROACH 3: HYBRID LINKS (Will work in both) -->
<div class="flashcards-container cards-per-row-4">
  <!-- Use data-href for Obsidian and href for web compatibility -->
  <div class="flashcard minimal">
    <a href="/pdf-to-obsidian" data-href="[[PDF to Obsidian\|PDF to Obsidian]]" class="flashcard-link hybrid-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/VanDyk.png" alt="PDF Converter">
        </div>
        <div class="flashcard-title">PDF to Obsidian</div>
      </div>
    </a>
  </div>
  
  <div class="flashcard minimal">
    <a href="/companies/van-dyk-recycling-solutions" data-href="[[Companies/VAN DYK Recycling Solutions\|Companies/VAN DYK Recycling Solutions]]" class="flashcard-link hybrid-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/VanDyk.png" alt="VAN DYK">
        </div>
        <div class="flashcard-title">VAN DYK</div>
      </div>
    </a>
  </div>
  
  <div class="flashcard minimal">
    <a href="/it/po-policies/isms-po-it-010-remote-access-policy" data-href="[[IT/PO (Policies)/ISMS-PO-IT-010 Remote Access Policy\|IT/PO (Policies)/ISMS-PO-IT-010 Remote Access Policy]]" class="flashcard-link hybrid-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/OfficeBollegraaf.png" alt="Remote Access Policy">
        </div>
        <div class="flashcard-title">Remote Access</div>
      </div>
    </a>
  </div>
  
  <div class="flashcard minimal">
    <a href="/it/po-policies/isms-po-it-007-cloud-security-policy" data-href="[[IT/PO (Policies)/ISMS-PO-IT-007 Cloud Security Policy\|IT/PO (Policies)/ISMS-PO-IT-007 Cloud Security Policy]]" class="flashcard-link hybrid-link">
      <div class="flashcard-content">
        <div class="flashcard-image">
          <img src="/IMG/StructureBRS.png" alt="Cloud Security Policy">
        </div>
        <div class="flashcard-title">Cloud Security</div>
      </div>
    </a>
  </div>
</div>

<!-- CSS STYLES -->
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

/* Base flashcard styles */
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

/* Glass variation */
.flashcard.glass {
  background: rgba(30, 37, 78, 0.4);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

/* Minimal variation */
.flashcard.minimal {
  height: 180px;
  background: var(--background-primary-alt, rgba(18, 20, 42, 0.85));
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
}

.flashcard.minimal .flashcard-image {
  height: 75%;
}

.flashcard.minimal .flashcard-title {
  height: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--background-secondary, #1E254E);
  padding: 8px;
  font-size: 0.95rem;
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

/* Javascript for hybrid links (add to a script file or inline) */
document.addEventListener('DOMContentLoaded', function() {
  // Check if we're in Obsidian
  const isObsidian = document.body.classList.contains('obsidian') || 
                     document.body.classList.contains('theme-dark') || 
                     document.body.classList.contains('theme-light');
  
  // Process hybrid links
  document.querySelectorAll('.hybrid-link').forEach(link => {
    if (isObsidian && link.dataset.href) {
      // We're in Obsidian, use wiki links
      link.href = link.dataset.href;
    }
    // In web environment, keep the existing href
  });
});

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
  
  .flashcard.minimal {
    height: 180px;
  }
}
</style>
