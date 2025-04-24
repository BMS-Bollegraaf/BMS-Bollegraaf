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
    <div class="swiper-slide">
      ![BRS.png](/img/user/IMG/BRS.png)
      <p class="caption">“First piece” — My commentary here</p>
    </div>
    <div class="swiper-slide">
      ![StructureBRS.png](/img/user/IMG/StructureBRS.png)
      <p class="caption">“Second piece” — More text</p>
    </div>
    <!-- repeat as needed -->
  </div>
  <!-- Navigation -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
  <!-- Back to dashboard -->
  <div class="back-btn">
    <a href="/Leaf’s-Observatory">← Back to Observatory</a>
  </div>
</div>
<style>
.myArtSwiper { width: 100%; max-width: 800px; margin: auto; }
.caption { text-align: center; margin-top: 0.5em; font-style: italic; }
.back-btn { text-align: center; margin: 1em 0; }
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
