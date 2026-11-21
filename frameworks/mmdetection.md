---
id: framework/mmdetection
type: framework
slug: mmdetection
schema_version: 1.1
title: MMDetection
kind: framework
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: OpenMMLab Detection Toolbox and Benchmark.
description: MMDetection is an open source object detection toolbox based on PyTorch and part of the OpenMMLab project. Its modular design decomposes the detection framework into components that can be combined into customized detectors, and it supports object detection, instance segmentation, panoptic segmentation and semi-supervised object detection, with pre-trained models in a model zoo.
best_for: Detection research that reimplements and compares methods, Building customized detectors from modular components
key_features:
- Modular design for building customized detection frameworks
- Object detection, instance segmentation, panoptic segmentation and semi-supervised detection
- Model zoo with pre-trained models
- Config system for defining models and training
- Bounding box and mask operations on GPUs
- Built on MMEngine and MMCV
use_cases:
- Object detection research and benchmarking
- Training detectors on custom datasets
- Finetuning pre-trained detection models
pros:
- Many detection methods in one codebase
- Runs on Linux, Windows and macOS
cons:
- CPU-only builds lack some operations (deformable convolution, ROI pooling, CARAFE, SyncBatchNorm)
language: Python
languages_supported:
- Python
maintained_by: OpenMMLab
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
maturity: production
alternatives:
- framework/detectron2
- framework/ultralytics-yolo
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 33045
  downloads_monthly: 200000
  latest_version: '3.3'
  latest_release_date: '2024-06-01'
  observed_at: '2026-11-20'
  source: https://github.com/open-mmlab/mmdetection
aliases:
- open-mmlab/mmdetection
tags:
- computer-vision
- object-detection
- model-zoo
- research
updated: '2026-11-21'
sources:
- url: https://github.com/open-mmlab/mmdetection
  title: GitHub repository
- url: https://mmdetection.readthedocs.io/
  title: Documentation
- url: https://mmdetection.readthedocs.io/en/latest/get_started.html
  title: Get started
- url: https://pypi.org/project/mmdet/
  title: mmdet — PyPI
---

## Overview

MMDetection is an open source object detection toolbox based on PyTorch and part of the OpenMMLab project. Its modular design decomposes the detection framework into components that can be combined into customized detectors, and it supports object detection, instance segmentation, panoptic segmentation and semi-supervised object detection, with pre-trained models in a model zoo.
