---
layout: page
title: Machine Learning-Driven Optimization in Biodegradable Mg Alloys
description: Using interpretable machine learning to optimize microstructure, processing, and properties of biodegradable magnesium alloys.
img: /assets/img/thrmbnail_ML.png
importance: 1
category: work
---

In this project, we develop a machine learning–guided strategy to simultaneously optimize **corrosion resistance** and **hardness** in biodegradable magnesium alloys, crucial for applications such as **resorbable vascular scaffolds**.

Working with (Prof. Paulette Clancy)[https://engineering.jhu.edu/faculty/paulette-clancy/] from Johns Hopkins University, Prof. Maitreyee Sharma Priyadharshini](https://www.aoe.vt.edu/people/faculty/maitreyee-sharma-priyadarshini.html) at **Virginia Tech**, and [Mr. Adam Griebel](https://www.linkedin.com/in/adam-griebel-19663717/) at **Fort Wayne Metals**, we integrate **physics-informed LASSO models** and the **PAL 2.0 Bayesian optimization framework** to uncover structure–property linkages and suggest optimal processing paths.

---

### Goals

- **Accelerate discovery** of microstructure–property relationships in Mg alloys.
- **Optimize processing parameters** (extrusion, ECAP, rolling, annealing) using Bayesian learning to minimize corrosion and maximize hardness.
- Translate laboratory discoveries to **industry-relevant processing** with Fort Wayne Metals.

---

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_structure.jpg" title="Physics-Informed Workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Our pipeline combines high-throughput experiments, feature engineering grounded in physics, and interpretable ML to guide structure–property understanding.
</div>

### Interpretable ML with LASSO

We use **physics-based LASSO regression** to isolate key microstructural features controlling corrosion and hardness—going beyond black-box ML approaches. This work is supported by our publication:

- 📄 *Machine learning-guided accelerated discovery of structure-property correlations in lean magnesium alloys for biomedical applications* [J. Magnes. Alloys, 2024](https://doi.org/10.1016/j.jma.2024.06.008)

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Corrosion_LASSO.png" title="Corrosion-related microstructural features" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Hardness_LASSO.png" title="Hardness-related microstructural features" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Key features governing corrosion behavior. Right: Critical predictors of mechanical hardness.
</div>

---

### Establishing Corrosion Testing Standards

Given the lack of standardized corrosion protocols for biodegradable Mg alloys, we conducted a systematic evaluation of test media, buffering, and volume—essential for reliable ML training data. Our findings, published in *JOM*:

- 📄 *Evaluating In-Vitro Corrosion Testing of ECAP-Processed Lean Magnesium Alloys: The Critical Role of Degradation Media Composition, Buffering, and Volume* [JOM, 2025](https://doi.org/10.1007/s11837-025-07176-7):contentReference[oaicite:0]{index=0}

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/fwm.png" title="Translation Partner: Fort Wayne Metals" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Partnering with Fort Wayne Metals to bridge ML insights and scalable implant development.
</div>

---

### Process Optimization with PAL 2.0

We implemented **PAL 2.0**, a physics-aware Bayesian optimization framework, to iteratively explore processing pathways and optimize the tradeoff between hardness and corrosion. Unlike brute-force design of experiments, PAL learns from each round and proposes new experiments most likely to improve the property balance.

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_Process_Optimization.png" title="PAL 2.0 Workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Multi-objective optimization: PAL 2.0 learns from sparse data and converges on optimal processing windows.
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/ML_Process.png" title="ML-guided experimental planning" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  ML-driven exploration of process space across extrusion, ECAP, rolling, and annealing routes.
</div>

---

### Preliminary Outcomes

- Structure–property links revealed through LASSO show processing effects on grain size, precipitate area, and GND density dominate performance.
- PAL 2.0 suggests new conditions not initially tested that outperform original processing routes.
- Corrosion standards and testing variability have been addressed to ensure **robust training datasets** for ML models.

Results were presented at **TMS 2025**, and a comprehensive manuscript integrating ML and experimental frameworks is **in preparation**.

---
### Collaboration

In partnership with [Mr. Adam Griebel](https://www.linkedin.com/in/adam-griebel-19663717/) from Fort Wayne Metals, [Prof. Paulette Clancy](https://engineering.jhu.edu/faculty/paulette-clancy/) from Johns Hopkins University, and [Prof. Maitreyee Sharma Priyadharshini](https://www.aoe.vt.edu/people/faculty/maitreyee-sharma-priyadarshini.html) from Virginia Tech, this work explores scalable process development for orthopedic screw application.

---

### References

1. S. Raguraman et al., *Machine learning-guided accelerated discovery of structure-property correlations in lean magnesium alloys for biomedical applications*, Journal of Magnesium and Alloys, 2024. [https://doi.org/10.1016/j.jma.2024.06.008](https://doi.org/10.1016/j.jma.2024.06.008)

2. S. Raguraman et al., *Evaluating In-Vitro Corrosion Testing of ECAP-Processed Lean Magnesium Alloys: The Critical Role of Degradation Media Composition, Buffering, and Volume*, JOM, 2025. [https://doi.org/10.1007/s11837-025-07176-7](https://doi.org/10.1007/s11837-025-07176-7)

---

