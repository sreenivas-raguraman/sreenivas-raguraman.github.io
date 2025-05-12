---
layout: page
title: gallery
permalink: /gallery/
---

<div class="container">
  <div class="row">
    {% assign images = "Biometal_Beril_Poster.jpeg,Biometal_Sreeni_Poster.jpeg,Biometal_Talk.jpeg,DOM_2022.jpeg,GRS-GRC2023.jpeg,MACH.jpeg,MGS_Talk.jpeg,MS_Graduation_Cohort.jpeg,MS_Graduation.jpeg,PNWAVS.jpeg,TMS_2022_Weihs_Group.jpeg,TMS_2023_BG.jpeg,TMS_2024_Advanced.jpeg,TMS_2024_Mg_Tech.jpeg,TMS_2024_Weihsgroup.jpeg,TMS2022_Talk.jpeg,TMS2022_Background.jpeg" | split: "," %}
    {% for image in images %}
      <div class="col-lg-3 col-md-4 col-sm-6 mb-4">
        <div class="card border-0">
          {% include figure.liquid path="assets/img/gallery/{{ image | strip }}" class="img-fluid rounded" alt=image %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>
