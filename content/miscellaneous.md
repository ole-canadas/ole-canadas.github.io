---
title: "Miscellaneous"
date: 2025-10-20
---

Below is a map highlighting my education, talks, and collaborators’ locations. Click the fullscreen button to show the legend.


<a href="https://www.google.com/maps/d/u/2/edit?mid=12hMnghvbbjdai8y8NshPStW-QHhnP1c&usp=sharing" 
   target="_blank" 
   rel="noopener noreferrer"
   title="Open in Google Maps">
  <iframe
    src="https://www.google.com/maps/d/u/2/embed?mid=12hMnghvbbjdai8y8NshPStW-QHhnP1c&ehbc=2E312F"
    width="100%"
    height="450"
    style="border:0;"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>
</a>

<div style="height: 50px;"></div>

I love combining mathematical research with exploring places I probably wouldn’t have visited otherwise. Here are a few impressions from my travels.

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gallery with Lightbox</title>
<style>
/* Gallery grid */
.gallery-row {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-bottom: 20px;
}

.gallery-item {
  width: 40%;
  display: flex;
  flex-direction: column;
  text-align: center;
}

.gallery-item .image-wrapper {
  width: 100%;
  height: 200px;
  overflow: hidden;
  border-radius: 5px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}

.gallery-item .image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.gallery-item figcaption {
  margin-top: 8px;
  font-size: 0.95rem;
  line-height: 1.2rem;
  text-align: center;
}

/* Lightbox modal */
#lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

#lightbox img {
  max-width: 90%;
  max-height: 70%;
  border-radius: 5px;
}

#lightbox figcaption {
  margin-top: 10px;
  color: #fff;
  font-size: 1rem;
}

#lightbox .close {
  position: absolute;
  top: 20px;
  right: 30px;
  font-size: 2rem;
  color: #fff;
  cursor: pointer;
}

@media (max-width: 768px) {
  .gallery-item {
    width: 90%;
  }
  .gallery-item .image-wrapper {
    height: 180px;
  }
}
</style>
</head>
<body>

<!-- Gallery Rows -->
<div class="gallery-row">
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/limerick1.jpg" alt="A street in Limerick">
    </div>
    <figcaption>A street in Limerick, Ireland.</figcaption>
  </figure>
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/limerick3.jpg" alt="River Shannon">
    </div>
    <figcaption>The River Shannon runs right through the Limerick campus.</figcaption>
  </figure>
</div>

<div class="gallery-row">
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/tunisia2.jpg" alt="Mediterranean Sea in Hammamet">
    </div>
    <figcaption>A sunny view of the Mediterranean Sea in Hammamet, Tunisia.</figcaption>
  </figure>
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/tunisia.jpg" alt="El Jem amphitheater">
    </div>
    <figcaption>El Jem, Tunisia, is home to an impressive Roman amphitheater.</figcaption>
  </figure>
</div>

<div class="gallery-row">
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/vaxjo.jpg" alt="Morning in Växjö">
    </div>
    <figcaption>Morning atmosphere in Växjö, Sweden.</figcaption>
  </figure>
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/vienna.jpg" alt="Hundertwasser house">
    </div>
    <figcaption>Hundertwasser house in Vienna.</figcaption>
  </figure>
</div>

<div class="gallery-row">
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/heidelberg.jpg" alt="Heidelberg city">
    </div>
    <figcaption>The beautiful city of Heidelberg, Germany, is home to the oldest university in the country.</figcaption>
  </figure>
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/dresden.jpg" alt="Dresden city">
    </div>
    <figcaption>Dresden, Germany, also known as “Elbflorenz”, is renowned for its rich cultural heritage and stunning baroque architecture.</figcaption>
  </figure>
</div>

<div class="gallery-row">
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/trento1.jpg" alt="Hike in Trento">
    </div>
    <figcaption>Enjoying a hike after an intense week of research in Trento, Italy.</figcaption>
  </figure>
  <figure class="gallery-item">
    <div class="image-wrapper" onclick="openLightbox(this)">
      <img src="/images/trento2.jpg" alt="Christmas in Povo">
    </div>
    <figcaption>Christmas atmosphere in Povo, Trento, Italy.</figcaption>
  </figure>
</div>

<!-- Lightbox modal -->
<div id="lightbox" onclick="closeLightbox()">
  <span class="close">&times;</span>
  <img id="lightbox-img" src="" alt="">
  <figcaption id="lightbox-caption"></figcaption>
</div>

<script>
function openLightbox(elem) {
  const img = elem.querySelector('img');
  const caption = elem.nextElementSibling.textContent;
  document.getElementById('lightbox-img').src = img.src;
  document.getElementById('lightbox-caption').textContent = caption;
  document.getElementById('lightbox').style.display = 'flex';
}

function closeLightbox() {
  document.getElementById('lightbox').style.display = 'none';
}
</script>

</body>
</html>



