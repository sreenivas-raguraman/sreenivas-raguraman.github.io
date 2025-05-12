---
layout: page
title: research
permalink: /research/
description: A growing collection of multi-scale, interdisciplinary research projects on microstructural and defect engineering, and advanced materials for biomedical purposes.
nav: true
nav_order: 4
display_categories: [work]
horizontal: false
---

### Research Vision

My research focuses on building fundamental understanding and advancing applied technologies for metallic systems. I study **vacancy-mediated clustering, precipitation, and recrystallization** at the atomic scale and develop **engineering solutions** for **biodegradable magnesium implants**, linking microstructure to **mechanical performance, corrosion resistance**, and **ion release behavior**.

This work spans **fundamental investigations** of solute-vacancy interactions to **data-driven optimization** of processing-microstructure-property relationships, and is conducted in close collaboration with national labs, universities, and industry partners.

---

### Collaborators & Institutional Affiliations

<div class="row justify-content-center">
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/PNNL_logo.png" title="PNNL" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/NIST_logo.png" title="NIST" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/HEMI_logo.png" title="HEMI" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/chembe.webp" title="JHU ChemBE" class="img-fluid rounded" style="height: 80px;" %}
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/Physics.jpg" title="JHU Physics" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/AI-X.jpg" title="AI-X Foundry" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/mcw.jpg" title="MCW-Marquette Biomedical" class="img-fluid rounded" style="height: 80px;" %}
  </div>
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/monash.png" title="Monash University" class="img-fluid rounded" style="height: 80px;" %}
  </div>
</div>
<div class="row justify-content-center">
  <div class="col-sm-3 mt-2">
    {% include figure.liquid path="assets/img/WSU_Pullman.jpeg" title="Washington State University" class="img-fluid rounded" style="height: 80px;" %}
  </div>
</div>

---

### Research Projects

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      <a id="{{ category }}" href=".#{{ category }}">
        <h2 class="category">{{ category }}</h2>
      </a>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1 row-cols-md-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.liquid %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="row row-cols-1 row-cols-md-3">
        {% for project in sorted_projects %}
          {% include projects.liquid %}
        {% endfor %}
        </div>
      {% endif %}
    {% endfor %}
  {% else %}
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
        {% for project in sorted_projects %}
          {% include projects_horizontal.liquid %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="row row-cols-1 row-cols-md-3">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
      </div>
    {% endif %}
  {% endif %}
</div>
