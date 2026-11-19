---
id: framework/detectron2
type: framework
slug: detectron2
schema_version: 1.1
title: Detectron2
kind: framework
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: Meta AI's next-generation library for object detection and segmentation
description: Meta AI's modular object detection and segmentation library built on PyTorch. Provides implementations of state-of-the-art models (Mask R-CNN, RetinaNet, Panoptic FPN) with a flexible configuration system.
best_for: Research on object detection and segmentation
not_ideal_for: Quick production deployment (use Ultralytics YOLO), beginners
key_features:
- Mask R-CNN, RetinaNet, Panoptic FPN
- Modular design and configuration
- Training and evaluation tools
- Model zoo with pre-trained weights
- Data augmentation pipelines
use_cases:
- Object detection and instance segmentation
- Panoptic segmentation
- Research on detection architectures
pros:
- High-quality implementations
- Modular and extensible
- Good pre-trained models
cons:
- Development has slowed
- Complex configuration system
- Installation can be finicky
language: Python
languages_supported:
- Python
maintained_by: Meta AI Research
first_release: '2019-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/facebookresearch/detectron2
docs_url: https://detectron2.readthedocs.io/
website_url: https://github.com/facebookresearch/detectron2
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
  type: corporate
  orgs:
  - Meta
  funding_or_parent: Meta AI Research (FAIR)
alternatives:
- framework/mmdetection
- framework/ultralytics-yolo
ecosystem_connections:
- framework/pytorch
- framework/torchvision
registry_signals:
  github_stars: 30500
  downloads_monthly: 300000
  latest_version: '0.6'
  latest_release_date: '2023-01-01'
  observed_at: '2026-06-15'
  source: https://github.com/facebookresearch/detectron2
aliases:
- facebookresearch/detectron2
tags:
- computer-vision
- object-detection
- segmentation
- research
updated: '2026-11-19'
sources:
- url: https://github.com/facebookresearch/detectron2
  title: GitHub repository
- url: https://detectron2.readthedocs.io/
  title: Documentation
---

## Overview

Meta AI's modular object detection and segmentation library built on PyTorch. Provides implementations of state-of-the-art models (Mask R-CNN, RetinaNet, Panoptic FPN) with a flexible configuration system.
