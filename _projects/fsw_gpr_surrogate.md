---
layout: page
title: Physics-Informed Surrogate Modelling for Dissimilar FSW
description: Gaussian Process Regression surrogate model with Bayesian optimisation for navigating the process–structure–property design space of dissimilar Friction Stir Welding.
img: assets/img/gpr_results.png
importance: 3
category: research
related_publications: true
---

Friction stir welding (FSW) of dissimilar materials — particularly aluminium alloys and
high-strength steels — involves a large process parameter space (rotation speed, traverse
speed, plunge depth, tool geometry) with non-linear, coupled effects on the resulting
microstructure and mechanical properties. Running full experimental campaigns to explore
this space is costly and time-consuming. Surrogate modelling offers a computationally
efficient alternative: build a model that approximates the process–property relationships
and use it to guide experiments intelligently.

This project develops a **physics-informed surrogate modelling framework** for dissimilar
FSW, grounded in the process-structure-property chain established from experimental thesis
work on AA6082-T6 / DP780 steel joints.

#### Why Gaussian Process Regression

GPR is well-suited to this problem for two reasons. First, it provides **uncertainty
estimates** alongside predictions — critical when making decisions about which experiments
to run next. Second, it naturally incorporates prior physical knowledge through the choice
of kernel function, allowing the model to reflect known smoothness and correlation
structure in the FSW process space.

#### Framework components

- **GPR surrogate model** trained on process parameter inputs (rotation speed, traverse
  speed, plunge depth) with ultimate tensile strength (UTS) and hardness as outputs
- **Bayesian optimisation** using the surrogate's uncertainty estimates to propose the
  next-best experiment (exploration vs. exploitation trade-off)
- **Process-structure-property chain** encoding the physical relationships between
  IMC layer thickness, grain refinement, and joint efficiency as constraints

#### Stack

`Python` · `scikit-learn` · `GPy` · `NumPy` · `Matplotlib` · `SciPy`

#### Links

- GitHub: [Deep7285/Physics-Informed-Surrogate-Modelling-for-Dissimilar-FSW](https://github.com/Deep7285/Physics-Informed-Surrogate-Modelling-for-Dissimilar-FSW)
- Related paper: {% cite kumar2026fsw %}