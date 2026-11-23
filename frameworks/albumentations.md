---
id: framework/albumentations
type: framework
slug: albumentations
schema_version: 3.0
title: AlbumentationsX
status: curated
kind: library
category: framework-category/computer-vision
subcategory: augmentation
tagline: Image augmentation for computer vision.
description: AlbumentationsX is a Python library for image augmentation, which creates new training samples from existing data. One consistent interface covers RGB, grayscale and multispectral images, masks, bounding boxes and keypoints, and the library also has 3D and medical-imaging transforms.
best_for: Training data augmentation for computer vision models
key_features:
- One interface for images, masks, bounding boxes and keypoints
- Pixel-level and spatial-level transforms
- 3D volume and medical-imaging transforms
- Serialization of augmentation pipelines
- Works with PyTorch, TensorFlow and other frameworks
use_cases:
- Training data augmentation for classification and segmentation
- Object detection data augmentation
- Medical image augmentation
pros:
- Applies the same transform to an image and its annotations
- Broad transform catalog
- Works with any OpenCV package variant
cons:
- Free use is under AGPL-3.0-only terms; a commercial license is sold separately
- Collects usage statistics by default (opt-out documented)
- Importing the library requires a separately installed PyTorch build
language: Python
languages_supported:
- Python
maintained_by: Albumentations team
license_spdx: AGPL-3.0-only
github_url: https://github.com/albumentations-team/AlbumentationsX
docs_url: https://albumentations.ai/docs/
website_url: https://albumentations.ai/
maturity: production
backing:
  type: community
ecosystem_connections:
- framework/pytorch
- framework/opencv
registry_signals:
  github_stars: 598
  downloads_monthly: 144070
  latest_version: 2.6.7
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/albumentations-team/AlbumentationsX
aliases:
- albumentations-team/albumentations
- Albumentations
tags:
- computer-vision
- augmentation
- data-processing
updated: '2026-11-21'
sources:
- url: https://github.com/albumentations-team/AlbumentationsX
  title: GitHub repository
- url: https://albumentations.ai/docs/
  title: Documentation
- url: https://pypi.org/project/albumentationsx/
  title: albumentationsx — PyPI
---


