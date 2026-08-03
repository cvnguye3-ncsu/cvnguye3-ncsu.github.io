---
title: "Evaluating Geospatial Foundational Models for Cloud Segmentation: A Comparative Study of Performance, Calibration, and Representations"
collection: publications
category: manuscripts
permalink: /publication/geospatial-foundation-models-cloud-segmentation
excerpt: "This study asks which broad choices in geospatial foundation-model design lead to accurate, trustworthy cloud segmentation and whether the internal representations of cloud-related phenomena can anticipate downstream quality. It evaluates a diverse set of pre-trained encoders through a shared segmentation framework so that differences in sensor modalities, architectures, and learning objectives can be studied consistently across familiar imagery and new datasets. The central findings suggest that neither radar-informed pre-training nor a particular architecture family is a reliable shortcut to better performance or calibration. The way a model learns during pre-training matters more for generalization, with self-distillation approaches transferring more effectively than reconstruction or contrastive objectives. Measures based on cloud-shadow robustness provide some insight into model behavior, but representation-compression measurements do not reliably explain performance, showing that foundation-model selection still requires direct evaluation rather than a simple proxy."
date: 2026-01-01
venue: "IEEE DSAA"
status: "Submitted to"
paperurl: "https://assets-eu.researchsquare.com/files/rs-9434428/v1_covered_5c617795-55a5-485a-9718-140e6649d7c4.pdf?c=1778253492"
githuburl: "https://github.com/cvnguye3-ncsu/gfm-cloud-segmentation"
---

{{ page.excerpt }}

<p><a href="{{ page.paperurl }}">Preprint</a> · <a href="{{ page.githuburl }}">GitHub repository</a></p>
