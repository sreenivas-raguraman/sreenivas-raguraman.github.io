---
layout: page
title: research
permalink: /research/
description: A growing collection of multi-scale, interdisciplinary research projects on microstructural and defect engineering, and advanced materials for biomedical purposes.
nav: true
nav_order: 3
display_categories: [work]
horizontal: false
_styles: |
  .projects .card img {
    max-height: 160px;
    object-fit: cover;
  }

  .projects .card-title {
    font-size: 1rem;
    font-weight: 600;
    line-height: 1.2;
  }

  .projects .card-text {
    font-size: 0.85rem;
    line-height: 1.4;
    max-height: 4.2em;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  .projects .card {
    height: 100%;
    padding-bottom: 0.5rem;
  }

  .projects .col, .projects .col-md-4, .projects .col-sm {
    padding-bottom: 1rem;
  }
---


### Research Vision

My research centers on <strong>mechanism-driven, processing-aware materials design</strong>. I seek to understand the physical mechanisms that control material behavior, then use that understanding to deliberately engineer composition, defects, interfaces, microstructure, and processing pathways around the needs of a specific application.

I approach these problems experimentally across length scales, from atomic-scale defects to bulk performance. A central theme in my work is understanding how materials evolve under <strong>non-equilibrium processing and demanding service conditions</strong>, and how changes at the atomic and microstructural levels ultimately translate into macroscopic behavior. Rather than treating processing, characterization, properties, and application requirements as separate questions, I bring them together to identify what truly limits performance and how that limitation can be overcome.

This philosophy has shaped my work on <strong>biodegradable magnesium alloys</strong>, where mechanical integrity, degradation, biological response, and manufacturability must be considered simultaneously. It also underpins my work in <strong>defect and vacancy engineering</strong>, where controlling atomic-scale defect populations provides a route to influence diffusion, phase evolution, and microstructural stability. Building on these foundations, I am interested in extending the same mechanistic framework toward <strong>nuclear and irradiation-resistant materials</strong>, <strong>materials for extreme environments</strong>, and <strong>sustainable materials design and processing</strong>.

To address these questions, I combine <strong>advanced characterization, non-equilibrium processing, and data-driven experimental design</strong>. I view these as complementary tools for connecting fundamental mechanisms with practical design decisions. Ultimately, my goal is to move from understanding <em>why</em> a material behaves the way it does to determining <em>how to make it perform better</em>, from <strong>atoms to applications</strong>.

---

### Collaborators & Institutional Affiliations

<style>
  .affiliations-scroll {
    display: flex;
    overflow-x: auto;
    gap: 30px;
    padding: 1rem 0;
    scrollbar-width: thin;
  }

  .affiliations-scroll::-webkit-scrollbar {
    height: 8px;
  }

  .affiliations-scroll::-webkit-scrollbar-thumb {
    background: #ccc;
    border-radius: 4px;
  }

  .logo-container {
    flex: 0 0 auto;
    width: 130px;
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .logo-container img {
    max-height: 60px;
    max-width: 120px;
    object-fit: contain;
  }
</style>

<div class="affiliations-scroll">
  <div class="logo-container">
    <img src="/assets/img/PNNL_logo.png" alt="PNNL">
  </div>
  <div class="logo-container">
    <img src="/assets/img/NIST_logo.png" alt="NIST">
  </div>
  <div class="logo-container">
    <img src="/assets/img/HEMI_logo.png" alt="HEMI">
  </div>
  <div class="logo-container">
    <img src="/assets/img/chembe.webp" alt="JHU ChemBE">
  </div>
  <div class="logo-container">
    <img src="/assets/img/Physics.jpg" alt="JHU Physics & Astronomy">
  </div>
  <div class="logo-container">
    <img src="/assets/img/AI-X.jpg" alt="AI-X Foundry">
  </div>
  <div class="logo-container">
    <img src="/assets/img/mcw.jpg" alt="MCW-Marquette BME">
  </div>
  <div class="logo-container">
    <img src="/assets/img/monash.png" alt="Monash University">
  </div>
  <div class="logo-container">
    <img src="/assets/img/WSU_Pullman.jpeg" alt="Washington State University">
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
