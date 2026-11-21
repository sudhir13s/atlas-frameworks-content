---
id: framework/detectron2
type: framework
slug: detectron2
schema_version: 1.1
title: Detectron2
kind: framework
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: Detectron2 is a platform for object detection, segmentation and other visual recognition tasks.
description: Detectron2 is Facebook AI Research's library of detection and segmentation algorithms and the successor of Detectron and maskrcnn-benchmark. It runs on PyTorch and includes panoptic segmentation, DensePose, Cascade R-CNN, rotated bounding boxes and PointRend. Models can be exported to TorchScript or Caffe2 format for deployment.
best_for: Research on object detection and segmentation
not_ideal_for: Windows (no official support)
key_features:
- Mask R-CNN, RetinaNet, Panoptic FPN
- Yacs and lazy configuration systems
- Training and evaluation tools
- Model zoo with pre-trained weights
- Data augmentation pipelines
- Export to TorchScript and Caffe2
use_cases:
- Object detection and instance segmentation
- Panoptic segmentation
- Research on detection architectures
pros:
- Used as a library for building research projects
- Pre-trained baselines in the Detectron2 Model Zoo
cons:
- Pre-built packages are Linux only
- No official support for Windows
language: Python
languages_supported:
- Python
maintained_by: Facebook AI Research
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
backing:
  type: corporate
  orgs:
  - Facebook AI Research
alternatives:
- framework/mmdetection
- framework/ultralytics-yolo
ecosystem_connections:
- framework/pytorch
- framework/torchvision
registry_signals:
  github_stars: 34995
  downloads_monthly: 300000
  latest_version: '0.6'
  latest_release_date: '2023-01-01'
  observed_at: '2026-11-20'
  source: https://github.com/facebookresearch/detectron2
aliases:
- facebookresearch/detectron2
tags:
- computer-vision
- object-detection
- segmentation
- research
updated: '2026-11-21'
sources:
- url: https://github.com/facebookresearch/detectron2
  title: GitHub repository
- url: https://detectron2.readthedocs.io/
  title: Documentation
- url: https://detectron2.readthedocs.io/en/latest/tutorials/install.html
  title: Documentation — Installation
- url: https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md
  title: Detectron2 Model Zoo
---

## Overview

Detectron2 is Facebook AI Research's library of detection and segmentation algorithms and the successor of Detectron and maskrcnn-benchmark. It runs on PyTorch and includes panoptic segmentation, DensePose, Cascade R-CNN, rotated bounding boxes and PointRend. Models can be exported to TorchScript or Caffe2 format for deployment.
