---
id: framework/tensorflow-lite
type: framework
slug: tensorflow-lite
schema_version: 1.1
title: TensorFlow Lite
kind: library
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: Deploy ML models on mobile and edge devices
description: Google's solution for running ML models on mobile phones, embedded devices, and microcontrollers. Provides model optimization (quantization, pruning), a lightweight runtime, and delegate system for hardware acceleration.
best_for: Mobile and embedded device ML deployment
not_ideal_for: Server-side inference, PyTorch-trained models without conversion
key_features:
- Post-training quantization (INT8, FP16)
- Delegates for GPU, DSP, NPU acceleration
- Android and iOS SDKs
- Microcontroller support (TF Lite Micro)
- Model optimization toolkit
- On-device training support
use_cases:
- On-device ML inference
- Mobile app AI features
- IoT and microcontroller ML
- Edge computing
pros:
- Gold standard for mobile ML
- Wide device support
- Good quantization tools
- Mature ecosystem
cons:
- TensorFlow model conversion required
- Some ops not supported on all delegates
- Future unclear as Google shifts to AI Edge
language: C++
languages_supported:
- Python
- C++
- Java
- Swift
- Objective-C
maintained_by: Google
first_release: '2017-11-01'
license_spdx: Apache-2.0
github_url: https://github.com/tensorflow/tensorflow
docs_url: https://www.tensorflow.org/lite
website_url: https://www.tensorflow.org/lite
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google (rebranded to LiteRT under Google AI Edge in 2024)
alternatives:
- framework/onnx-runtime-mobile
- framework/coreml-tools
- framework/executorch
ecosystem_connections:
- framework/tensorflow
registry_signals:
  github_stars: 187000
  downloads_monthly: 3000000
  latest_version: '2.18'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/tensorflow/tensorflow
tags:
- edge-mobile
- mobile
- quantization
- deployment
updated: '2026-11-19'
sources:
- url: https://github.com/tensorflow/tensorflow
  title: GitHub repository
- url: https://www.tensorflow.org/lite
  title: Documentation
---

## Overview

Google's solution for running ML models on mobile phones, embedded devices, and microcontrollers. Provides model optimization (quantization, pruning), a lightweight runtime, and delegate system for hardware acceleration.
