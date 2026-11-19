---
id: framework/torchvision
type: framework
slug: torchvision
schema_version: 1.1
title: torchvision
kind: library
category: framework-category/computer-vision
subcategory: pytorch-ecosystem
tagline: Datasets, models, and transforms for computer vision in PyTorch
description: Official PyTorch package for computer vision. Provides pre-trained models (ResNet, VGG, EfficientNet, ViT), standard datasets (ImageNet, COCO, VOC), and image transforms. The go-to starting point for CV in PyTorch.
best_for: Standard CV tasks in PyTorch, transfer learning starting point
not_ideal_for: Cutting-edge model architectures (use timm)
key_features:
- Pre-trained models (50+ architectures)
- Standard CV datasets
- Image and video transforms
- Detection and segmentation models
- Automatic mixed precision support
use_cases:
- Image classification
- Object detection
- Transfer learning
- CV data loading and preprocessing
pros:
- Tight PyTorch integration
- Comprehensive model zoo
- Standard datasets built-in
cons:
- Model zoo less comprehensive than timm
- Transforms API changed between versions
language: Python
languages_supported:
- Python
- C++
maintained_by: PyTorch Foundation
first_release: '2017-01-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/vision
docs_url: https://pytorch.org/vision/stable/
website_url: https://pytorch.org/vision/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Meta
  - PyTorch Foundation
alternatives:
- framework/albumentations
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 16500
  downloads_monthly: 10000000
  latest_version: '0.21'
  latest_release_date: '2025-01-29'
  observed_at: '2026-06-15'
  source: https://github.com/pytorch/vision
aliases:
- pytorch/vision
tags:
- computer-vision
- pytorch
- models
- datasets
updated: '2026-11-19'
sources:
- url: https://github.com/pytorch/vision
  title: GitHub repository
- url: https://pytorch.org/vision/stable/
  title: Documentation
---

## Overview

Official PyTorch package for computer vision. Provides pre-trained models (ResNet, VGG, EfficientNet, ViT), standard datasets (ImageNet, COCO, VOC), and image transforms. The go-to starting point for CV in PyTorch.
