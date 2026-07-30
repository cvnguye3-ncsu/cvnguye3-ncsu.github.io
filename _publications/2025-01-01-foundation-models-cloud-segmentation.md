---
title: "Foundation Models for Semantic Segmentation of Thick/Thin Clouds and Cloud Shadows: A Comparative Study"
collection: publications
category: conferences
permalink: /publication/foundation-models-cloud-segmentation-comparative-study
excerpt: "This study examines how foundation-model design, pre-training, transfer learning, and prompt-based interaction shape the ability to distinguish clear areas, clouds, thin clouds, and cloud shadows in satellite imagery. It places conventional cloud masking, promptable segmentation, geospatial foundation models, and modern vision architectures within a common experimental framework, then evaluates not only overall segmentation quality but also behavior around boundaries, small features, and visually challenging landscapes. The broader findings show that learned models offer a substantial advantage over conventional masking, transformer-based representations are especially useful for fine spatial detail, and promptable models have subpar peroformance on geospatial phenomena without geospatial pre-training data. At the same time, thin clouds and cloud shadows remain difficult because they blend with the land beneath them, and the value of pre-training depends more on the kind of scene and feature being segmented than on a single universally superior model."
date: 2025-11-03
venue: "ACM SIGSPATIAL"
status: "Short paper at"
publicationurl: "https://dl.acm.org/doi/10.1145/3748636.3762766"
githuburl: "https://github.com/cvnguye3-ncsu/l8-biome"
research_image: "/2025_ACM_SIGSPATIAL_picture.png"
research_image_alt: "Satellite images, reference cloud masks, and predicted masks from the cloud-segmentation methods compared in the study"
research_image_caption: "Qualitative comparison of conventional, promptable, and foundation-model approaches to cloud segmentation."
---

{{ page.excerpt }}

<figure class="research-figure">
  <img src="{{ page.research_image }}" alt="{{ page.research_image_alt }}">
  <figcaption>{{ page.research_image_caption }}</figcaption>
</figure>

<p><a href="{{ page.publicationurl }}">ACM Digital Library</a> · <a href="{{ page.githuburl }}">GitHub repository</a></p>
