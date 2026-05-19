---
layout: page
title: Marine Heatwave Detection & Forecasting
description: Physics-aware ML/DL for detecting and forecasting extreme marine heatwave events in the North Indian Ocean using high-dimensional spatio-temporal sea surface temperature data.
img: assets/img/convo_lstm.png
importance: 3
category: research
related_publications: false
---

Extreme marine heatwave (MHW) events are becoming more frequent and intense in the North
Indian Ocean, with significant consequences for marine ecosystems, fisheries, and regional
climate patterns. Detecting and forecasting these events reliably requires working with
high-dimensional, spatio-temporal oceanographic data — a problem where standard statistical
approaches quickly run into their limits.

This project, carried out as a Data Scientist at IIT Delhi, applies machine learning
and deep learning to sea surface temperature (SST) datasets to identify the physical
signatures of MHW onset, propagation, and intensification.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/convo_lstm.png" alt="Convo-LSTM for Climate forecasting" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

#### The core challenge

The dataset is inherently high-dimensional — gridded SST fields across the North Indian
Ocean with spatial and temporal structure that needs to be preserved. Simply flattening the
data and feeding it into a classifier loses the physical relationships that drive
heatwave dynamics. The approach here is to let the physics guide how the ML is applied,
not to treat it as a black-box prediction problem.

#### Approach

- Spatiotemporal analysis of SST anomalies using the MHW detection framework
  (Hobday et al. definition) to identify and characterise historical MHW events
- Feature engineering grounded in the physical drivers of MHW formation
  (mixed layer depth, wind stress curl, heat flux anomalies)
- Comparative evaluation of ML/DL architectures for event detection and forecasting
- Ongoing work on understanding which physical signals the models are actually picking up

#### Stack

`Python` · `TensorFlow` · `NumPy` · `Xarray` · `MHW analysis` · `Matplotlib` · `Pandas`

#### Links

- GitHub: [Deep7285/Climate-code-files](https://github.com/Deep7285/Climate-code-files)