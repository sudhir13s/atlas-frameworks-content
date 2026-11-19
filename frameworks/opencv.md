---
id: framework/opencv
type: framework
slug: opencv
schema_version: 1.1
title: OpenCV
kind: library
category: framework-category/computer-vision
subcategory: core-library
tagline: Open-source computer vision and image processing library
description: The foundational computer vision library with 2500+ algorithms for image processing, object detection, video analysis, and camera calibration. Available in multiple languages. Used in robotics, autonomous vehicles, medical imaging, and more.
best_for: Classical computer vision, image processing, video analysis
not_ideal_for: Training deep learning models (use PyTorch + torchvision)
key_features:
- 2500+ CV algorithms
- Image and video I/O
- Object detection and tracking
- Camera calibration
- DNN module for inference
- CUDA acceleration
use_cases:
- Image processing pipelines
- Real-time video analysis
- Robotics and autonomous vehicles
- Medical image processing
pros:
- Most comprehensive CV library
- Massive community and resources
- Multi-language support
- Battle-tested in production
cons:
- API can be inconsistent across modules
- Deep learning support is basic (use PyTorch for training)
- Large dependency
language: C++
languages_supported:
- C++
- Python
- Java
- JavaScript
maintained_by: OpenCV Foundation / Intel
first_release: '2000-06-01'
license_spdx: Apache-2.0
github_url: https://github.com/opencv/opencv
docs_url: https://docs.opencv.org/
website_url: https://opencv.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: true
  google_tpu: false
learning_curve: medium
community_size: massive
maturity: production
signal_strength: high
backing:
  type: foundation
  orgs:
  - OpenCV Foundation
  funding_or_parent: Originated at Intel; now a nonprofit foundation with corporate sponsors (Intel, Huawei, Xperi)
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 80000
  downloads_monthly: 10000000
  latest_version: '4.10'
  latest_release_date: '2024-06-01'
  observed_at: '2026-06-15'
  source: https://github.com/opencv/opencv
aliases:
- opencv/opencv
tags:
- computer-vision
- image-processing
- video
- classical-cv
updated: '2026-11-19'
sources:
- url: https://github.com/opencv/opencv
  title: GitHub repository
- url: https://docs.opencv.org/
  title: Documentation
---

## Overview

The foundational computer vision library with 2500+ algorithms for image processing, object detection, video analysis, and camera calibration. Available in multiple languages. Used in robotics, autonomous vehicles, medical imaging, and more.
