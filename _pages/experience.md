---
layout: page
title: experience
permalink: /experience/
description: My professional and research journey — from experimental materials science to interdisciplinary ML and data science.
nav: true
nav_order: 4
---

<style>
.exp-card {
  border: 1px solid var(--global-divider-color);
  border-radius: 8px;
  padding: 1.5rem 1.5rem 1.2rem 1.5rem;
  margin-bottom: 1.8rem;
  background: var(--global-card-bg-color);
}
.exp-title {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0 0 0.2rem 0;
  color: var(--global-text-color);
}
.exp-org {
  font-size: 0.97rem;
  color: var(--global-theme-color);
  font-weight: 500;
  margin: 0 0 0.15rem 0;
}
.exp-meta {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
  margin: 0 0 1rem 0;
}
.exp-body p {
  font-size: 0.93rem;
  margin-bottom: 0.6rem;
}
.exp-body ul {
  padding-left: 1.2rem;
  margin-bottom: 0.6rem;
}
.exp-body li {
  font-size: 0.93rem;
  margin-bottom: 0.3rem;
}
.exp-gallery {
  display: flex;
  gap: 0.6rem;
  flex-wrap: wrap;
  margin-top: 1.1rem;
}
.exp-gallery img {
  height: 140px;
  width: auto;
  max-width: 100%;
  object-fit: cover;
  border-radius: 5px;
  border: 1px solid var(--global-divider-color);
}
.section-label {
  font-size: 0.74rem;
  font-weight: 600;
  letter-spacing: 0.09em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  margin: 2.4rem 0 0.9rem 0;
  padding-bottom: 0.4rem;
  border-bottom: 1px solid var(--global-divider-color);
}
</style>

<p class="mt-2 mb-4" style="color: var(--global-text-color-light); font-size: 0.94rem;">
  My path has been deliberately non-linear — starting with hands-on experimental engineering,
  moving through industry, then back into research. Each step informed the next, and the
  combination of physical intuition with computational methods is what I now try to bring to
  every problem I work on.
</p>

<!-- ============================================================ -->
<p class="section-label">Research & Academic</p>
<!-- ============================================================ -->

<!-- 1. Data Scientist — IIT Delhi -->
<div class="exp-card">
  <p class="exp-title">Data Scientist</p>
  <p class="exp-org">Indian Institute of Technology Delhi</p>
  <p class="exp-meta">New Delhi, India &nbsp;·&nbsp; Jan 2025 – Present</p>
  <div class="exp-body">
    <p>
      I work on a problem at the intersection of geophysical science and applied machine learning:
      how do you build models that reliably detect and forecast rare, extreme events from
      high-dimensional, noisy observational data — when the underlying physics is partially
      understood but too complex to model analytically?
    </p>
    <p>
      My approach is physics-first. Before modelling, I study the documented physical mechanisms
      behind marine heatwave formation — mixed layer dynamics, air-sea heat flux anomalies,
      oceanic circulation patterns. That understanding shapes every modelling decision: which
      features to engineer, what architecture makes physical sense, where to constrain the model,
      and how to interpret what it learns.
    </p>
    <ul>
      <li>Designing and evaluating deep learning architectures (ConvLSTM, temporal CNNs)
          for spatiotemporal sequence modelling on gridded ocean reanalysis data</li>
      <li>Statistical characterisation of extreme event distributions — understanding tail
          behaviour before attempting prediction</li>
      <li>Physics-informed feature engineering: encoding domain knowledge as model inputs
          rather than expecting the network to discover physical relationships from scratch</li>
      <li>Evaluating model outputs against known physical drivers to ensure predictions
          are physically consistent, not just statistically accurate</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/convo_lstm.png" class="img-fluid" alt="ConvLSTM architecture for spatiotemporal modelling" %}
  </div>
</div>

<!-- 2. Associate Solution Leader — Brane Enterprises -->
<div class="exp-card">
  <p class="exp-title">Associate Solution Leader — Machine Learning Engineer</p>
  <p class="exp-org">Brane Enterprises Pvt. Ltd.</p>
  <p class="exp-meta">Hyderabad, India &nbsp;·&nbsp; Feb 2024 – Feb 2025</p>
  <div class="exp-body">
    <p>
      Worked within a 50-person team building ML-driven solutions for e-commerce and retail
      clients — from model development through to business impact measurement.
    </p>
    <ul>
      <li>Developed and optimised deep learning models (TensorFlow, PyTorch) for product
          price optimisation and customer segmentation, contributing to a
          <strong>15% increase in sales</strong> for e-commerce clients</li>
      <li>Built data analytics pipelines using Tableau and Apache Superset to extract
          actionable insights from large retail datasets, improving sales forecast
          accuracy by <strong>10%</strong></li>
      <li>Collaborated on model evaluation, feature engineering, and deployment workflows
          alongside senior engineers</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/data_processing_flow.png" class="img-fluid" alt="Data processing pipeline" %}
    {% include figure.liquid path="assets/img/rl_diagram.png" class="img-fluid" alt="Model architecture diagram" %}
    {% include figure.liquid path="assets/img/stats.png" class="img-fluid" alt="Analytics output" %}
  </div>
</div>

<!-- 3. Research Assistant — MSME Lab IIT Madras -->
<div class="exp-card">
  <p class="exp-title">Research Assistant — MS by Research</p>
  <p class="exp-org">MEMS Lab, Dept. of Metallurgical & Materials Engineering, IIT Madras</p>
  <p class="exp-meta">Chennai, India &nbsp;·&nbsp; Feb 2021 – May 2025 &nbsp;·&nbsp; Guide: Prof. Ranjit Bauri</p>
  <div class="exp-body">
    <p>
      Four years of hands-on research in the Materials Energy Manufacturing Sustainability (MEMS)
      Lab. My thesis focused on friction stir welding (FSW) of dissimilar materials —
      AA6082-T6 aluminium alloy and DP780 dual-phase steel — targeting lightweight automotive
      applications.
    </p>
    <ul>
      <li>Designed and executed FSW process parameter studies; characterised joints using
          HR-SEM, EDS, XRD, EBSD, nano-indentation, and UTM mechanical testing</li>
      <li>Correlated intermetallic compound (IMC) formation at the weld interface with
          joint failure mechanisms and mechanical performance under varying process parameters</li>
      <li>Developed ML models (Random Forest, SVM, linear regression) to predict UTS
          from process parameters — connecting data-driven methods to physical understanding</li>
      <li>Presented at <strong>THERMEC'23</strong> (University of Technology Vienna, Austria);
          secured 3rd place at IIT Madras national symposium</li>
      <li>Teaching Assistant for MM2010 (Physical Metallurgy) and NOC24-MM14 (NDT) —
          led weekly lab sessions for a batch of 70 students</li>
    </ul>
    <p><em>1st-author manuscript under review — Journal of Manufacturing Processes.</em></p>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/uts_testing.png" class="img-fluid" alt="UTS mechanical testing" %}
    {% include figure.liquid path="assets/img/msme_group.png" class="img-fluid" alt="MSME Lab group" %}
    {% include figure.liquid path="assets/img/vianna_presentation.png" class="img-fluid" alt="THERMEC23 Vienna presentation" %}
  </div>
</div>

<!-- 4. Student Leadership — IIT Madras -->
<div class="exp-card">
  <p class="exp-title">Student Leadership & University Engagement</p>
  <p class="exp-org">IIT Madras — CDC-R · Placement Cell · Departmental Activities</p>
  <p class="exp-meta">Chennai, India &nbsp;·&nbsp; 2021 – 2025</p>
  <div class="exp-body">
    <p>
      Alongside research, I contributed to the broader IIT Madras student community through
      structured roles in career development and departmental engagement.
    </p>
    <ul>
      <li>Active member of CDC-R (Career Development Cell – Research) — supporting research
          scholars with career planning, industry connections, and professional development</li>
      <li>Participated in departmental placement cell activities, connecting students with
          research and industry opportunities</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/CDC-R.jpg" class="img-fluid" alt="CDC-R activities" %}
    {% include figure.liquid path="assets/img/placement_cell.png" class="img-fluid" alt="Placement cell" %}
    {% include figure.liquid path="assets/img/department_logo.png" class="img-fluid" alt="Department activities" %}
  </div>
</div>

<!-- ============================================================ -->
<p class="section-label">Industry</p>
<!-- ============================================================ -->

<!-- 5. Technical Consultant — OSN Consulting -->
<div class="exp-card">
  <p class="exp-title">Technical Consultant</p>
  <p class="exp-org">OSN Consulting & Associates</p>
  <p class="exp-meta">Uttar Pradesh, India &nbsp;·&nbsp; Oct 2019 – Dec 2020</p>
  <div class="exp-body">
    <p>
      Conducted technical and financial valuations of large-scale plant and machinery
      projects (INR 150–200 Cr range), providing assessments that supported strategic
      procurement and investment decisions across manufacturing and infrastructure sectors.
      Developed rigorous cross-functional reporting skills working across engineering
      and finance teams.
    </p>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/OSN.png" class="img-fluid" alt="OSN Consulting" %}
  </div>
</div>

<!-- 6. Assistant Engineer — Dynamic Infratech -->
<div class="exp-card">
  <p class="exp-title">Assistant Engineer</p>
  <p class="exp-org">Dynamic Intra-tech Pvt. Ltd.</p>
  <p class="exp-meta">Kota, Rajasthan, India &nbsp;·&nbsp; Jul 2018 – Sep 2019</p>
  <div class="exp-body">
    <p>
      Managed a production team in steel bridge fabrication. Optimised machining parameters
      through data-driven analysis of production records, contributing to a
      <strong>9–10% improvement in production throughput</strong>. First hands-on exposure
      to manufacturing process data and the value of systematic parameter analysis.
    </p>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/dynamic_enggs_work.png" class="img-fluid" alt="Dynamic Infratech engineering work" %}
  </div>
</div>