---
layout: page
title: Human Mentor–Mentee Matching System
description: NLP-based matching system for pairing alumni mentors with mentees based on holistic life experience — built for the IIT Madras alumni mentoring programme.
img: assets/img/human_match_app.png
importance: 4
category: side-projects
related_publications: false
---

Most matching systems — job boards, recommendation engines, dating apps — work on
structured data: keywords, categories, ratings. Mentor–mentee matching in an alumni
network is a harder problem. The data is unstructured (free-text descriptions of career
journeys, interests, goals), the relationship is long-term, and the match quality depends
on compatibility across dimensions that don't map neatly to any single feature vector.

This project builds a matching pipeline for the **IIT Madras alumni mentoring programme**,
developed in collaboration with a team of senior alumni. My role covers the matching
algorithm and automation end of the system.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/human_match_app.png" alt="human response match app" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

#### The problem

Given a set of mentee profiles (goals, background, areas seeking guidance) and mentor
profiles (expertise, experience, availability), find pairings that maximise compatibility
— not just on surface-level keywords, but on the underlying substance of what each person
brings and needs. No off-the-shelf solution exists for this specific formulation.

#### Approach

- **NLP-based profile encoding**: free-text responses processed using sentence
  transformers to generate dense semantic embeddings
- **Similarity scoring**: cosine similarity between mentee and mentor embedding vectors,
  weighted by configurable priority dimensions
- **Batch matching**: automated assignment across the full cohort, with output rankings
  for human review before finalisation
- Deployed as a Streamlit web app for programme coordinators to upload data and
  generate matches without touching code

#### Stack

`Python` · `sentence-transformers` · `scikit-learn` · `Pandas` · `Streamlit`. `tf-idf`

#### Links

- GitHub: [Deep7285/human-response-matching-app](https://github.com/Deep7285/human-response-matching-app)
- Live demo: [hrmiitmaa.streamlit.app](https://hrmiitmaa.streamlit.app/#upload-data-files)