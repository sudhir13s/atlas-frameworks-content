---
id: framework/mmdetection
type: framework
slug: mmdetection
schema_version: 1.1
title: MMDetection
kind: framework
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: OpenMMLab's comprehensive object detection toolbox
description: Part of OpenMMLab, a comprehensive detection toolbox containing 300+ pre-trained models and 80+ algorithms. Covers 2D/3D object detection, instance segmentation, and panoptic segmentation with a unified config system.
best_for: Detection research requiring comparison across many algorithms
not_ideal_for: Simple deployment (use YOLO), teams not familiar with OpenMMLab
key_features:
- 80+ detection algorithms
- 300+ pre-trained models
- Unified config system
- Rich data augmentation
- Multi-GPU training
- ONNX export support
use_cases:
- Object detection research and benchmarking
- Production detection models
- Detection algorithm comparison
pros:
- Most comprehensive detection model zoo
- Unified framework for comparing algorithms
- Active development
cons:
- OpenMMLab ecosystem adds learning overhead
- Config system is powerful but complex
- Documentation can lag behind code
language: Python
languages_supported:
- Python
maintained_by: OpenMMLab / Shanghai AI Lab
first_release: '2018-09-01'
license_spdx: Apache-2.0
github_url: https://github.com/open-mmlab/mmdetection
docs_url: https://mmdetection.readthedocs.io/
website_url: https://openmmlab.com/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: large
maturity: production
signal_strength: medium
backing:
  type: foundation
  orgs:
  - OpenMMLab
  - Shanghai AI Laboratory
alternatives:
- framework/detectron2
- framework/ultralytics-yolo
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 29800
  downloads_monthly: 200000
  latest_version: '3.3'
  latest_release_date: '2024-06-01'
  observed_at: '2026-06-15'
  source: https://github.com/open-mmlab/mmdetection
aliases:
- open-mmlab/mmdetection
tags:
- computer-vision
- object-detection
- model-zoo
- research
updated: '2026-11-19'
sources:
- url: https://github.com/open-mmlab/mmdetection
  title: GitHub repository
- url: https://mmdetection.readthedocs.io/
  title: Documentation
---

## Overview

Part of OpenMMLab, a comprehensive detection toolbox containing 300+ pre-trained models and 80+ algorithms. Covers 2D/3D object detection, instance segmentation, and panoptic segmentation with a unified config system.
