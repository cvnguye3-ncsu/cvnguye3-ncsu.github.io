---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

[Download resume (PDF)]({{ site.baseurl }}/calvin-nguyen-resume-updated.pdf){: .btn .btn--primary}

Cary, NC · [cvnguye3@ncsu.edu](mailto:cvnguye3@ncsu.edu)

Education
======

- **PhD, Computer Science**, North Carolina State University — anticipated December 2027
- **MCS, Computer Science**, North Carolina State University — May 2024
- **BS, Computer Science**, North Carolina State University — May 2019

Work experience
======

### Natrx — Data Scientist, Geospatial ML & Remote Sensing

*August 2023 – July 2026*

- Developed a geospatial machine-learning pipeline for land/water classification and shoreline-change detection, supporting analysis of 2,909 shoreline miles across 39 North Carolina study areas and 93,017 measurement locations.
- Developed and validated Guyana's PlanetScope-based shoreline classification workflow, achieving 97.9–99.2% accuracy across 300 bootstrapped evaluations and enabling erosion and accretion mapping along 682 km of coastline.
- Created an experimental submerged-mudbank detection method using Canny edge detection and support vector machines on 50 cm satellite imagery to identify wave-damping and wave-breaking signatures associated with fluid and consolidated mud.
- Produced land/water segmentation for Biscayne Bay erosion analysis and assembled a property-level geospatial dataset enriched with ownership, zoning, land use, address, and permitting-related attributes.
- Evaluated eight physical datasets for Billion Oyster Project across six quality and integration criteria; implemented literature-derived rules for depth, velocity, wave exposure, erosion, and infrastructure proximity within a prioritization analysis of 78 candidate restoration sites.
- Processed topo-bathymetric LiDAR, water-level datums, submerged aquatic vegetation, and soil-carbon data for coastal restoration planning; derived shoreline elevations, slopes, and cross-sections and produced graphics supporting preliminary design and permitting.

### Wake County Library — Page

*June 2023 – August 2023*

- Sorted and shelved library materials in alphabetic and numerical order.
- Checked in materials using the library's automated computer system.
- Boxed and unboxed materials and assisted library members with book donations.

Research
======

### Foundation Models for Semantic Segmentation of Thick/Thin Clouds and Cloud Shadows: A Comparative Study

*ACM SIGSPATIAL 2025 short paper*

- Converts raw L8-Biome Landsat scenes into non-overlapping 224 × 224 RGB image/label pairs, filters no-data crops, computes class statistics, and serializes fixed 60/15/25 split metadata.
- Runs FMask, prompt-based HQ-SAM, Prithvi, SatlasNet, and LSKNet/UNetFormer through Hydra-configured preparation, training, checkpointing, and evaluation workflows.
- Includes TorchScript-compatible model rewrites and reports class, boundary, small-object, and snow/ice transfer metrics across feature-extraction, half-frozen, and full fine-tuning settings.

[ACM Digital Library](https://dl.acm.org/doi/10.1145/3748636.3762766) · [GitHub repository](https://github.com/cvnguye3-ncsu/l8-biome)

### Evaluating Geospatial Foundational Models for Cloud Segmentation: A Comparative Study of Performance, Calibration, and Representations

*Submitted to IEEE DSAA 2026*

- Crops and serializes metadata for L8-Biome, CloudSEN12+, Landsat 8 C1 CCA, and the Sentinel-2 Cloud Mask Catalogue, with the latter two reserved for out-of-distribution evaluation.
- Loads 17 frozen geospatial encoders with model-specific RGB normalization and routes their features through a shared ViT-Adapter where needed, UPerNet head, and DySample upsampler.
- Uses PyTorch Lightning and Hydra to control splits, seeds, initialization, batching, optimization, and evaluation of IoU, expected calibration error, adversarial cloud-shadow error, and mutual-information density.

[GitHub repository](https://github.com/cvnguye3-ncsu/gfm-cloud-segmentation)

**Advisor:** [Ranga Raju Vatsavai](https://csc.ncsu.edu/people/rrvatsav/), Professor, North Carolina State University

Volunteering
======

### JC Raulston Arboretum

*Spring/Summer 2023*

- Audited plant locations and labels from bed maps.
- Replaced stakes and labels for plants.
- Consulted on updating a deprecated database connector.
- Demonstrated RESTful API usage for connecting to PostgreSQL/PostGIS.

Technical skills
======

- **Programming and data:** Python, pandas
- **Geospatial:** GIS, remote sensing, spatial analysis, GeoPandas, Rasterio, GDAL
- **Machine learning:** scikit-learn, XGBoost, computer vision
