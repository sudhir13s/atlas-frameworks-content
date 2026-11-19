---
id: framework/onnx-runtime-mobile
type: framework
slug: onnx-runtime-mobile
schema_version: 1.1
title: ONNX Runtime Mobile
kind: library
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: Cross-platform mobile inference with ONNX models
description: Mobile-optimized version of ONNX Runtime for running ONNX models on iOS, Android, and embedded devices. Framework-agnostic since any model can be exported to ONNX format.
best_for: Mobile deployment of models from any training framework
not_ideal_for: Projects already in TensorFlow ecosystem (use TF Lite)
key_features:
- Framework-agnostic (any ONNX model)
- iOS and Android support
- NNAPI and CoreML delegates
- Quantization support
- Minimal binary size
use_cases:
- Cross-platform mobile ML
- Framework-agnostic mobile deployment
- Embedded device inference
pros:
- Works with any framework via ONNX
- Good platform coverage
- Backed by Microsoft
cons:
- ONNX conversion can be lossy
- Less mature mobile tooling than TF Lite
language: C++
languages_supported:
- C++
- Java
- Swift
- Objective-C
- Python
maintained_by: Microsoft
first_release: '2020-01-01'
license_spdx: MIT
github_url: https://github.com/microsoft/onnxruntime
docs_url: https://onnxruntime.ai/docs/tutorials/mobile/
website_url: https://onnxruntime.ai/
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
  - Microsoft
alternatives:
- framework/tensorflow-lite
- framework/coreml-tools
ecosystem_connections:
- framework/onnx-runtime
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 15500
  downloads_monthly: 500000
  latest_version: '1.20'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/microsoft/onnxruntime
tags:
- edge-mobile
- mobile
- cross-platform
- onnx
updated: '2026-11-19'
sources:
- url: https://github.com/microsoft/onnxruntime
  title: GitHub repository
- url: https://onnxruntime.ai/docs/tutorials/mobile/
  title: Documentation
---

## Overview

Mobile-optimized version of ONNX Runtime for running ONNX models on iOS, Android, and embedded devices. Framework-agnostic since any model can be exported to ONNX format.
