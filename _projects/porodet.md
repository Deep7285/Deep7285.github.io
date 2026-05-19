---
layout: page
title: PoroDet
description: Open-source Python package for automated nano-porosity detection in TEM images — developed in collaboration with Oxford Nano Analysis, University of Oxford.
img: assets/img/porosity_detection.png
importance: 1
category: research
related_publications: true
---

{% include figure.liquid path="assets/img/porosity_detection.png" alt="TEM image detection" class="img-fluid rounded z-depth-1" %}

Nuclear reactor cladding materials degrade over time through nano-scale porosity formation.
Detecting and quantifying these features manually in transmission electron microscopy (TEM)
images is time-consuming and operator-dependent. This project automates that process.

In collaboration with [Rajat Nama](https://nanoanalysis.web.ox.ac.uk/people/rajat-nama)
at Oxford Nano Analysis (University of Oxford), we developed **PoroDet** — an end-to-end
Python workflow for supervised segmentation of nano-porosities in Fresnel-contrast TEM images
of Zr-alloy nuclear cladding.

#### What the package does

- Accepts raw TEM images and user-supplied mask annotations as input
- Runs a full pipeline: data augmentation → U-Net CNN training → batch inference → quantitative output
- Designed to work with limited training data (a common constraint in materials TEM work)
- Supports both training from scratch and transfer learning (fine-tuning)

#### Key technical results

- U-Net architecture achieved **92% feature detection accuracy** with 80% less training data compared to classical methods
- Random Forest baseline: 95% training accuracy, 80% detection accuracy
- Model performance validated using ROC-AUC, precision-recall curves, and confusion matrices

#### Links

- GitHub: [Deep7285/PoroDet](https://github.com/Deep7285/PoroDet)
- Zenodo DOI: [10.5281/zenodo.19342741](https://doi.org/10.5281/zenodo.19342741)
- Submitted to {% cite nama2025porodet %}
