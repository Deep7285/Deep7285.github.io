---
layout: page
title: GeoCalc
description: Interactive geometry calculator for areas and volumes of standard 3D shapes — deployed on Hugging Face Spaces.
img: assets/img/geocalc.png
importance: 2
category: side-projects
related_publications: false
---

A lightweight, browser-based calculator for computing areas and volumes of standard
geometric shapes. Built as a practical exercise in building and deploying a clean,
usable tool end-to-end — from Python logic to a live public interface via Hugging Face Spaces.

#### What it does

- Computes surface area and volume for standard 3D geometries
  (spheres, cylinders, cones, cubes, rectangular prisms, and more)
- Clean input form with instant output — no page reloads
- Fully deployed and publicly accessible, no installation required

#### Why it exists

This was a deliberate exercise in the full deployment workflow:
writing clean Python, wrapping it in a Gradio interface, and pushing it to Hugging Face
Spaces as a publicly hosted app. Small in scope, but the deployment pattern — local code
to live web app in a reproducible way — is directly transferable to more complex tools.

#### Stack

`Python` · `Gradio` · `Hugging Face Spaces`

#### Links

- GitHub: [Deep7285/GeoCalc](https://github.com/Deep7285/GeoCalc)
- Live app: [huggingface.co/spaces/Deep7285/Geometry-Calculator](https://huggingface.co/spaces/Deep7285/Geometry-Calculator)