---
id: framework/torchvision
type: framework
slug: torchvision
schema_version: 1.1
title: torchvision
kind: library
category: framework-category/computer-vision
subcategory: pytorch-ecosystem
tagline: Datasets, Transforms and Models specific to Computer Vision.
description: torchvision is the computer vision library of the PyTorch project. It provides popular datasets, model architectures with pre-trained weights, and common image transformations. Its models cover image classification, semantic segmentation, object detection, instance segmentation, keypoint detection, video classification and optical flow.
best_for: Computer vision with PyTorch, Loading pre-trained vision models
key_features:
- Pre-trained weights for every provided architecture
- Built-in computer vision datasets
- Transforms for images, videos and bounding boxes
- Classification, detection, segmentation, video and optical flow models
- Quantized models
- Detection and segmentation operators
use_cases:
- Image classification
- Object detection
- Semantic and instance segmentation
- Computer vision data loading and preprocessing
pros:
- Part of the PyTorch project
- Pre-trained weights for every provided architecture
- Built-in dataset loaders
cons:
- Pre-trained weights may carry their own licence terms (SWAG models are CC-BY-NC)
- The image decoding and encoding module is deprecated
language: Python
languages_supported:
- Python
maintained_by: PyTorch Foundation
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/vision
docs_url: https://docs.pytorch.org/vision/stable/
website_url: https://docs.pytorch.org/vision/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: foundation
  orgs:
  - PyTorch Foundation
alternatives:
- framework/albumentations
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 18023
  downloads_monthly: 18172848
  latest_version: 0.29.2
  latest_release_date: '2026-10-28'
  observed_at: '2026-11-20'
  source: https://github.com/pytorch/vision
aliases:
- pytorch/vision
tags:
- computer-vision
- pytorch
- models
- datasets
updated: '2026-11-21'
sources:
- url: https://github.com/pytorch/vision
  title: GitHub repository
- url: https://docs.pytorch.org/vision/stable/
  title: Documentation
- url: https://docs.pytorch.org/vision/stable/models.html
  title: Models and pre-trained weights
- url: https://pytorch.org/get-started/locally/
  title: PyTorch install guide
- url: https://pypi.org/project/torchvision/
  title: torchvision — PyPI
---

## Overview

torchvision is the computer vision library of the PyTorch project. It provides popular datasets, model architectures with pre-trained weights, and common image transformations. Its models cover image classification, semantic segmentation, object detection, instance segmentation, keypoint detection, video classification and optical flow.
