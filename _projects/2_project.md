---
layout: page
title: Machine Learning-Driven Optimization in Biodegradable Mg Alloys
description: Using machine learning to optimize corrosion resistance and hardness in biodegradable magnesium alloys.
img: /assets/img/thrmbnail_ML.png
importance: 2
category: work
---

This project aims to develop a machine learning-driven approach to rapidly identify optimal processing parameters and structure–property relationships in biodegradable magnesium alloys, with an emphasis on simultaneously optimizing **corrosion resistance** and **mechanical hardness**.

In collaboration with **Prof. Paulette Clancy**, **Prof. Maitreyee Sharma**, and **Dr. Adam Griebel** from **Fort Wayne Metals**, we have created an integrated experimental-computational framework combining physics-informed LASSO modeling and Bayesian optimization (PAL 2.0).

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_Process_Optimization.png" title="PAL 2.0 Workflow for Mg Alloy Optimization" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Overview of our machine learning framework combining accelerated data acquisition with PAL 2.0 for multi-objective optimization.
</div>

### Project Goals
- Learn the **relationship between microstructure and properties** using interpretable physics-based LASSO models.
- Use PAL 2.0 to iteratively **identify and test new processing conditions** that achieve the best compromise between **low corrosion rate** and **high hardness**.
- Guide development of high-performance biodegradable implants with tailored properties.

### Approach and Framework

We combine:
- **Experimental data** from controlled processing (ECAP, extrusion, heat treatment, rolling), microstructural analysis, and corrosion/hardness testing.
- **Physics-informed feature engineering**, grounded in classical strengthening and corrosion models.
- **LASSO regression**, regularized with physical intuition, to isolate key microstructure–property descriptors.
- **PAL 2.0 optimization algorithm**, to identify optimal process parameters from a wide design space.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Corrosion_LASSO.png" title="LASSO output for corrosion" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Hardness_LASSO.png" title="LASSO output for hardness" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/fwm.png" title="Fort Wayne Metals Collaboration" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left and Center: Physics-based LASSO reveals dominant microstructure descriptors governing corrosion and hardness. Right: Our collaboration with Fort Wayne Metals supports translation of ML insights into industry.
</div>

### Iterative Optimization
<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_Process.png" title="Iterative ML-Guided Optimization" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The PAL 2.0 algorithm iteratively explores new processing conditions to refine the process window for optimal properties.
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_structure.jpg" title="Physics-informed ML workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Integrated approach: microstructural quantification, physics-informed feature engineering, and validation via SEM/EDS/EBSD.
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-7 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/thrmbnail_ML.png" title="PAL 2.0 Output" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Output plot showing evolution of property space—Round 2 samples approach target zone with low corrosion and high hardness.
</div>

### In Preparation
Preliminary results were presented at **TMS 2025**, and we are currently preparing a journal manuscript on the full integration of ML and experimental workflows.

---
**Keywords:** magnesium alloys, corrosion, hardness, machine learning, Bayesian optimization, LASSO, structure–property, biodegradable implants, Fort Wayne Metals
