---
id: framework/ultralytics-yolo
type: framework
slug: ultralytics-yolo
schema_version: 1.1
title: Ultralytics YOLO
kind: library
category: framework-category/computer-vision
subcategory: detection-segmentation
tagline: YOLO models for object detection, instance segmentation, semantic segmentation, image classification, pose estimation and object tracking.
description: Ultralytics YOLO is a family of real-time computer vision models available through one Python package and CLI. It covers object detection, instance and semantic segmentation, depth estimation, classification, pose estimation and oriented bounding boxes, and can track detected objects across video frames. Models can be trained, validated, run and exported to deployment formats such as ONNX, TensorRT and OpenVINO.
best_for: Real-time object detection and segmentation, Training and exporting YOLO models
key_features:
- Detection, instance and semantic segmentation, classification and depth estimation
- Pose estimation and oriented bounding boxes
- Multi-object tracking (BoT-SORT, ByteTrack and others)
- Python API and yolo CLI for training, validation, prediction and export
- Export to ONNX, TensorRT, OpenVINO, CoreML, LiteRT and other formats
- Training on NVIDIA and AMD GPUs, Apple silicon and Intel XPU
use_cases:
- Real-time object detection
- Object tracking in video
- Edge deployment of exported models
pros:
- Same API across tasks in Python and CLI
- Wide choice of export formats
cons:
- AGPL-3.0 licence; commercial use outside its terms needs an Ultralytics Enterprise License
- Multi-GPU training does not work on Windows with official PyTorch wheels
language: Python
languages_supported:
- Python
maintained_by: Ultralytics
license_spdx: AGPL-3.0-only
github_url: https://github.com/ultralytics/ultralytics
docs_url: https://docs.ultralytics.com/
website_url: https://ultralytics.com/
maturity: production
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
  github_stars: 63624
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
updated: '2026-11-21'
sources:
- url: https://github.com/ultralytics/ultralytics
  title: GitHub repository
- url: https://docs.ultralytics.com/
  title: Documentation
- url: https://docs.ultralytics.com/modes/export/
  title: Export mode
- url: https://docs.ultralytics.com/modes/train/
  title: Train mode
- url: https://pypi.org/project/ultralytics/
  title: ultralytics — PyPI
---

## Overview

Ultralytics YOLO is a family of real-time computer vision models available through one Python package and CLI. It covers object detection, instance and semantic segmentation, depth estimation, classification, pose estimation and oriented bounding boxes, and can track detected objects across video frames. Models can be trained, validated, run and exported to deployment formats such as ONNX, TensorRT and OpenVINO.
