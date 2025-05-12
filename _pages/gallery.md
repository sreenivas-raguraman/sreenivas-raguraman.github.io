---
layout: page
title: gallery
permalink: /gallery/
images:
  lightbox2: true
---
<!-- Gallery Carousel with Thumbnails and Responsive Styling -->
<div id="researchGallery" class="carousel slide carousel-fade" data-ride="carousel" data-interval="3000" data-pause="hover">
  <div class="carousel-inner rounded shadow">
    {% assign images = "Biometal_Beril_Poster.jpeg,Biometal_Sreeni_Poster.jpeg,Biometal_Talk.jpeg,DOM_2022.jpeg,GRS-GRC2023.jpeg,MACH.jpeg,MGS_Talk.jpeg,MS_Graduation_Cohort.jpeg,MS_Graduation.jpeg,PNWAVS.jpeg,TMS_2022_Weihs_Group.jpeg,TMS_2023_BG.jpeg,TMS_2024_Advanced.jpeg,TMS_2024_Mg_Tech.jpeg,TMS_2024_Weihsgroup.jpeg,TMS2022_Talk.jpeg,TMS2022_Background.jpeg" | split: "," %}
    {% for image in images %}
      <div class="carousel-item {% if forloop.first %}active{% endif %}">
        <a href="/assets/img/{{ image | strip }}" data-lightbox="gallery" data-title="{{ image }}">
          <img src="/assets/img/{{ image | strip }}" class="d-block w-100 img-fluid" alt="{{ image }}">
        </a>
        <!-- <div class="carousel-caption d-none d-md-block">
          <p>Caption for {{ image }}</p>
        </div> -->
      </div>
    {% endfor %}
  </div>

  <!-- Navigation Controls -->
  <a class="carousel-control-prev" href="#researchGallery" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#researchGallery" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>

  <!-- Thumbnail Preview Navigation -->
  <ol class="carousel-indicators mt-3">
    {% for image in images %}
      <li data-target="#researchGallery" data-slide-to="{{ forloop.index0 }}" class="{% if forloop.first %}active{% endif %}">
        <img src="/assets/img/{{ image | strip }}" class="img-thumbnail" style="height: 60px; object-fit: cover;">
      </li>
    {% endfor %}
  </ol>
</div>

<style>
  #researchGallery {
    max-width: 1000px;
    margin: 40px auto;
  }

  .carousel-item img {
    object-fit: contain;
    max-height: 500px;
    width: 100%;
    border-radius: 5px;
  }

  .carousel-indicators {
    justify-content: center;
    overflow-x: auto;
    white-space: nowrap;
    padding: 0;
    margin: 10px auto 0;
  }

  .carousel-indicators li {
    display: inline-block;
    margin: 0 5px;
    cursor: pointer;
  }

  .carousel-indicators img {
    width: auto;
    height: 60px;
    border-radius: 3px;
  }

  @media (max-width: 576px) {
    .carousel-item img {
      max-height: 300px;
    }

    .carousel-indicators img {
      height: 40px;
    }
  }
</style>
