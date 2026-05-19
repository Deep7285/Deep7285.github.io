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
  padding: 1.5rem;
  margin-bottom: 1.8rem;
  background: var(--global-card-bg-color);
}
.exp-header {
  display: flex;
  align-items: flex-start;
  gap: 1.2rem;
  margin-bottom: 1rem;
}
.exp-logo {
  width: 64px;
  height: 64px;
  object-fit: contain;
  border-radius: 6px;
  flex-shrink: 0;
  background: var(--global-bg-color);
}
.exp-title {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0 0 0.15rem 0;
  color: var(--global-text-color);
}
.exp-org {
  font-size: 0.95rem;
  color: var(--global-theme-color);
  font-weight: 500;
  margin: 0 0 0.15rem 0;
}
.exp-meta {
  font-size: 0.83rem;
  color: var(--global-text-color-light);
  margin: 0;
}
.exp-gallery {
  display: flex;
  gap: 0.6rem;
  flex-wrap: wrap;
  margin-top: 1rem;
}
.exp-gallery img {
  height: 130px;
  width: auto;
  object-fit: cover;
  border-radius: 5px;
  border: 1px solid var(--global-divider-color);
}
.exp-body ul {
  padding-left: 1.2rem;
  margin-bottom: 0.5rem;
}
.exp-body li {
  margin-bottom: 0.3rem;
  font-size: 0.93rem;
}
.section-label {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--global-text-color-light);
  margin: 2.2rem 0 0.8rem 0;
  padding-bottom: 0.4rem;
  border-bottom: 1px solid var(--global-divider-color);
}
</style>

<p class="mt-2 mb-4" style="color: var(--global-text-color-light); font-size: 0.95rem;">
  My path has been deliberately non-linear — starting with hands-on experimental engineering,
  moving through industry, then back into research. Each step informed the next, and the
  combination of physical intuition with computational methods is what I now try to bring to
  every problem I work on.
</p>

<!-- ==================== RESEARCH ==================== -->
<p class="section-label">Research & Academic</p>

<!-- IIT Delhi -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/iitd_logo.png" class="exp-logo" alt="IIT Delhi logo" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Data Scientist</p>
      <p class="exp-org">Indian Institute of Technology Delhi</p>
      <p class="exp-meta">New Delhi, India &nbsp;·&nbsp; Jan 2025 – Present</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      I work on a problem that sits at the intersection of geophysical science and machine learning:
      how do you build models that can reliably detect and forecast rare, extreme events from
      high-dimensional, noisy observational data — when the underlying physics is partially
      understood but far too complex to model analytically?
    </p>
    <p>
      My approach is physics-first. Before writing a single line of ML code, I study the
      documented physical mechanisms behind marine heatwave formation — mixed layer dynamics,
      air-sea heat flux anomalies, oceanic circulation patterns. That understanding shapes
      every modelling decision: which features to engineer, what architecture makes physical
      sense, where the model should be constrained, and how to interpret what it learns.
    </p>
    <ul>
      <li>Designing and evaluating deep learning architectures (ConvLSTM, temporal CNNs)
          for spatiotemporal sequence modelling on gridded ocean reanalysis data</li>
      <li>Statistical characterisation of extreme event distributions — understanding the
          tail behaviour before trying to predict it</li>
      <li>Physics-informed feature engineering: encoding domain knowledge as model inputs
          rather than expecting the network to discover physical relationships from scratch</li>
      <li>Evaluating model decisions against known physical drivers to ensure outputs are
          physically consistent, not just statistically accurate</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/convo_lstm.png" class="img-fluid" alt="ConvLSTM architecture for spatiotemporal modelling" %}
  </div>
</div>

<!-- MSME Lab IIT Madras -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/iitm_logo.png" class="exp-logo" alt="IIT Madras logo" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Research Assistant — MS by Research</p>
      <p class="exp-org">MEMS Lab, Dept. of Metallurgical & Materials Engineering, IIT Madras</p>
      <p class="exp-meta">Chennai, India &nbsp;·&nbsp; Feb 2021 – May 2025 &nbsp;·&nbsp; Guide: Prof. Ranjit Bauri</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      Four years of hands-on research in the Materials Energy Manufacturing Sustainability (MEMS)
      Lab under Prof. Ranjit Bauri. My thesis focused on friction stir welding (FSW) of
      dissimilar materials — AA6082-T6 aluminium alloy and DP780 dual-phase steel — targeting
      lightweight automotive applications.
    </p>
    <ul>
      <li>Designed and executed FSW process parameter studies; characterised joints using
          HR-SEM, EDS, XRD, EBSD, nano-indentation, and UTM mechanical testing</li>
      <li>Correlated intermetallic compound (IMC) formation at the weld interface with
          joint failure mechanisms and mechanical performance</li>
      <li>Developed ML models (Random Forest, SVM, linear regression) to predict UTS
          from process parameters — connecting data science to physical understanding</li>
      <li>Presented at <strong>THERMEC'23</strong> (University of Technology Vienna, Austria)
          and two IIT Madras national symposia, including a 3rd place finish</li>
      <li>Co-supervised lab sessions for a batch of 70 students as Teaching Assistant
          for MM2010 (Physical Metallurgy) and NOC24-MM14 (NDT)</li>
    </ul>
    <p><em>1st author manuscript under review at Journal of Manufacturing Processes.</em></p>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/uts_testing.png" class="img-fluid" alt="UTS mechanical testing" %}
    {% include figure.liquid path="assets/img/msme_group.png" class="img-fluid" alt="MSME Lab group" %}
    {% include figure.liquid path="assets/img/vianna_preseantation.png" class="img-fluid" alt="THERMEC23 Vienna presentation" %}
  </div>
</div>

<!-- ==================== INDUSTRY ==================== -->
<p class="section-label">Industry</p>

<!-- Brane -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/brane_logo.png" class="exp-logo" alt="Brane Enterprises logo" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Associate Solution Leader — Machine Learning Engineer</p>
      <p class="exp-org">Brane Enterprises Pvt. Ltd.</p>
      <p class="exp-meta">Hyderabad, India &nbsp;·&nbsp; Feb 2024 – Feb 2025</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      Worked within a 50-person team building ML-driven solutions for e-commerce and
      retail clients. My core work was in deep learning model development and
      data analytics — from model training to business impact reporting.
    </p>
    <ul>
      <li>Developed and optimised deep learning models (TensorFlow, PyTorch) for
          product price optimisation and customer segmentation —
          contributed to a <strong>15% sales increase</strong> for e-commerce clients</li>
      <li>Built analytical pipelines using Tableau and Apache Superset to surface
          actionable insights from large retail datasets, improving sales forecast
          accuracy by <strong>10%</strong></li>
      <li>Collaborated on model evaluation, feature engineering, and deployment
          pipelines alongside senior engineers</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/data_processing_flow.png" class="img-fluid" alt="Data processing pipeline" %}
    {% include figure.liquid path="assets/img/rl_diagram.png" class="img-fluid" alt="Model architecture" %}
    {% include figure.liquid path="assets/img/stats.png" class="img-fluid" alt="Analytics dashboard" %}
  </div>
</div>

<!-- OSN Consulting -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/OSN.png" class="exp-logo" alt="OSN Consulting logo" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Technical Consultant</p>
      <p class="exp-org">OSN Consulting & Associates</p>
      <p class="exp-meta">Uttar Pradesh, India &nbsp;·&nbsp; Oct 2019 – Dec 2020</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      Conducted technical and financial valuations of large-scale plant and machinery
      projects (INR 150–200 Cr range), providing assessments that supported strategic
      procurement and investment decisions. Built rigorous technical reporting and
      cross-functional communication skills working across engineering and finance teams.
    </p>
  </div>
</div>

<!-- Dynamic Infratech -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/dynamic_enggs_work.png" class="exp-logo" alt="Dynamic Infratech" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Assistant Engineer</p>
      <p class="exp-org">Dynamic Intra-tech Pvt. Ltd.</p>
      <p class="exp-meta">Kota, Rajasthan, India &nbsp;·&nbsp; Jul 2018 – Sep 2019</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      Managed a production team in steel bridge fabrication. Optimised machining parameters
      through data-driven analysis of production records, contributing to a
      <strong>9–10% improvement in production throughput</strong>.
      First exposure to the value of systematic data analysis in a manufacturing setting.
    </p>
  </div>
</div>

<!-- ==================== COMMUNITY ==================== -->
<p class="section-label">Leadership & University Engagement</p>

<!-- Student leadership IIT Madras -->
<div class="exp-card">
  <div class="exp-header">
    <img src="/assets/img/department_logo.png" class="exp-logo" alt="IIT Madras department" onerror="this.style.display='none'">
    <div>
      <p class="exp-title">Student Roles — IIT Madras</p>
      <p class="exp-org">CDC-R · Placement Cell · Departmental Activities</p>
      <p class="exp-meta">Chennai, India &nbsp;·&nbsp; 2021 – 2025</p>
    </div>
  </div>
  <div class="exp-body">
    <p>
      Alongside research, I was involved in the broader IIT Madras community through
      student-led initiatives. These roles developed skills in coordination, mentoring,
      and working across diverse groups that don't always show up in a research CV but
      genuinely shape how you work with people.
    </p>
    <ul>
      <li>Active member of the CDC-R (Career Development Cell – Research) — supporting
          research scholars in career planning and professional development</li>
      <li>Involvement in departmental placement cell activities, connecting students with
          industry and research opportunities</li>
    </ul>
  </div>
  <div class="exp-gallery">
    {% include figure.liquid path="assets/img/CDC-R.jpg" class="img-fluid" alt="CDC-R activities" %}
    {% include figure.liquid path="assets/img/placement_cell.png" class="img-fluid" alt="Placement cell" %}
  </div>
</div>