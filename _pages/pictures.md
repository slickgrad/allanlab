---
title: "Annamalai Lab - Gallery"
layout: piclay
excerpt: "Research Gallery"
permalink: /pictures/
---

<div class="container">
  <h1 class="mb-4">Lab Gallery</h1>
  
  <div class="alert alert-info">
    <i class="fas fa-info-circle"></i> Click any image to view full size
  </div>

  <div class="row">
    {% for pic in site.data.pictures_term %}
      <div class="col-sm-6 col-md-4 col-lg-3 mb-4">
        <a href="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}" 
           data-lightbox="gallery"
           data-title="{{ pic.caption }}">
          <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/{{ pic.image }}"
               class="img-fluid rounded shadow-sm"
               loading="lazy"
               width="800"
               height="600"
               style="object-fit: cover; height: 200px"
               alt="{{ pic.description }}">
        </a>
      </div>
      
      {% assign mod = forloop.index | modulo: 4 %}
      {% if mod == 0 and forloop.last == false %}
        </div><div class="row">
      {% endif %}
    {% endfor %}
  </div>
</div>

<!-- Add lightbox CSS/JS -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/js/lightbox.min.js"></script>

<style>
/* Custom gallery styling */
.img-fluid {
  transition: transform 0.3s ease;
  cursor: zoom-in;
}

.img-fluid:hover {
  transform: scale(1.03);
}

.lb-data .lb-caption {
  font-size: 1rem;
  line-height: 1.4;
}
</style>