---
id: framework/albumentations
type: framework
slug: albumentations
schema_version: 1.1
title: AlbumentationsX
kind: library
category: framework-category/computer-vision
subcategory: augmentation
tagline: Fast image augmentation library for deep learning
description: High-performance image augmentation library optimized for deep learning. Provides 70+ augmentation transforms that work with images, masks, bounding boxes, and keypoints simultaneously. Built on OpenCV for speed.
best_for: CV model training data augmentation
not_ideal_for: Non-image data, GPU-only augmentation pipelines
key_features:
- 70+ augmentation transforms
- Simultaneous image + mask + bbox augmentation
- Fast (OpenCV backend)
- Serialization of augmentation pipelines
- Integration with PyTorch and TF data loaders
use_cases:
- Training data augmentation for CV models
- Object detection data augmentation
- Medical image augmentation
pros:
- Very fast augmentations
- Handles bboxes and masks correctly
- Wide range of transforms
cons:
- Image-only (no text/audio augmentation)
- Some transforms are CPU-only
language: Python
languages_supported:
- Python
maintained_by: Albumentations team
first_release: '2018-06-01'
license_spdx: AGPL-3.0-only
github_url: https://github.com/albumentations-team/AlbumentationsX
docs_url: https://albumentations.ai/docs/
website_url: https://albumentations.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: large
maturity: production
signal_strength: medium
backing:
  type: community
  funding_or_parent: Community-maintained by a team of Kaggle Grandmasters
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
updated: '2026-11-20'
sources:
- url: https://github.com/albumentations-team/AlbumentationsX
  title: GitHub repository
- url: https://albumentations.ai/docs/
  title: Documentation
---

## Overview

High-performance image augmentation library optimized for deep learning. Provides 70+ augmentation transforms that work with images, masks, bounding boxes, and keypoints simultaneously. Built on OpenCV for speed.
