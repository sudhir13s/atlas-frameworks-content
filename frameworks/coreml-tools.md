---
id: framework/coreml-tools
type: framework
slug: coreml-tools
schema_version: 1.1
title: Core ML Tools
kind: library
category: framework-category/edge-mobile
subcategory: apple-ecosystem
tagline: Convert and optimize ML models for Apple devices
description: Apple's toolkit for converting ML models from PyTorch, TensorFlow, and other frameworks to Core ML format. Optimized for Apple Neural Engine, GPU, and CPU on iPhone, iPad, Mac, and Apple Watch.
best_for: ML deployment on Apple devices
not_ideal_for: Cross-platform deployment, Android
key_features:
- PyTorch and TF model conversion
- Apple Neural Engine optimization
- Quantization and compression
- On-device model fine-tuning
- Model visualization
use_cases:
- iOS/macOS ML deployment
- Apple Neural Engine optimization
- On-device Apple ML features
pros:
- Best performance on Apple devices
- Neural Engine acceleration
- Tight Apple ecosystem integration
cons:
- Apple-only
- Some operations not supported in conversion
- Debugging conversion issues is difficult
language: Python
languages_supported:
- Python
- Swift
maintained_by: Apple
first_release: '2017-06-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/apple/coremltools
docs_url: https://coremltools.readme.io/
website_url: https://developer.apple.com/machine-learning/core-ml/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Apple
alternatives:
- framework/tensorflow-lite
- framework/onnx-runtime-mobile
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 5456
  downloads_monthly: 1470427
  latest_version: '9.0'
  latest_release_date: '2025-11-10'
  observed_at: '2026-11-20'
  source: https://github.com/apple/coremltools
aliases:
- apple/coremltools
tags:
- edge-mobile
- apple
- ios
- macos
- neural-engine
updated: '2026-11-20'
sources:
- url: https://github.com/apple/coremltools
  title: GitHub repository
- url: https://coremltools.readme.io/
  title: Documentation
---

## Overview

Apple's toolkit for converting ML models from PyTorch, TensorFlow, and other frameworks to Core ML format. Optimized for Apple Neural Engine, GPU, and CPU on iPhone, iPad, Mac, and Apple Watch.
