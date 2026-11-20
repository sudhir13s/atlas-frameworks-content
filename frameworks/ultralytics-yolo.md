---
id: framework/ultralytics-yolo
type: framework
slug: ultralytics-yolo
schema_version: 1.1
title: Ultralytics YOLO
kind: library
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: YOLO for everyone — real-time object detection, segmentation, classification, and tracking
description: The most popular real-time object detection framework. YOLOv8/v11 provides state-of-the-art accuracy with exceptional speed. Simple CLI and Python API for training, inference, and export to multiple formats.
best_for: Production real-time detection, fastest path to working detection system
not_ideal_for: Novel architecture research, AGPL-averse commercial projects
key_features:
- Real-time detection, segmentation, classification
- Object tracking (BoT-SORT, ByteTrack)
- Pose estimation
- One-line training and inference
- Export to ONNX, TensorRT, CoreML, TF Lite
- Active learning and data management
use_cases:
- Real-time object detection
- Security and surveillance
- Industrial quality inspection
- Sports analytics
pros:
- Best speed/accuracy tradeoff
- Simplest API in detection
- Excellent export and deployment support
- Very active development
cons:
- AGPL license (commercial use requires license purchase)
- Less flexible for research on novel architectures
- Opinionated design
language: Python
languages_supported:
- Python
maintained_by: Ultralytics
first_release: '2023-01-10'
license_spdx: AGPL-3.0-only
github_url: https://github.com/ultralytics/ultralytics
docs_url: https://docs.ultralytics.com/
website_url: https://ultralytics.com/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: true
  intel_oneapi: true
  google_tpu: false
learning_curve: very-low
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Ultralytics
alternatives:
- framework/detectron2
- framework/mmdetection
ecosystem_connections:
- framework/pytorch
- framework/onnx-runtime
registry_signals:
  github_stars: 63623
  downloads_monthly: 5154997
  latest_version: 8.4.216
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/ultralytics/ultralytics
aliases:
- ultralytics/ultralytics
tags:
- computer-vision
- object-detection
- real-time
- yolo
- production
updated: '2026-11-20'
sources:
- url: https://github.com/ultralytics/ultralytics
  title: GitHub repository
- url: https://docs.ultralytics.com/
  title: Documentation
---

## Overview

The most popular real-time object detection framework. YOLOv8/v11 provides state-of-the-art accuracy with exceptional speed. Simple CLI and Python API for training, inference, and export to multiple formats.
