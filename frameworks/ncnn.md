---
id: framework/ncnn
type: framework
slug: ncnn
schema_version: 1.1
title: ncnn
kind: framework
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: ncnn is a neural network inference framework optimized for the mobile platform.
description: ncnn is a neural network inference framework optimized for mobile, embedded and desktop deployment. It is a pure C++ implementation with no third-party runtime dependencies, runs on CPU and Vulkan GPU backends, and converts PyTorch and ONNX models to ncnn through its pnnx tool.
best_for: Neural network inference on mobile and embedded devices
key_features:
- No third-party runtime dependencies
- ARM NEON optimized CPU inference
- Vulkan GPU acceleration
- int8 quantized inference
- PyTorch and ONNX model conversion through pnnx
use_cases:
- Mobile inference on ARM devices
- Embedded and edge device inference
pros:
- No third-party runtime dependencies
- Low memory footprint
- C API and Python binding alongside C++
language: C++
languages_supported:
- C++
- C
- Python
maintained_by: Tencent
license_spdx: BSD-3-Clause
github_url: https://github.com/Tencent/ncnn
docs_url: https://github.com/Tencent/ncnn/wiki
website_url: https://github.com/Tencent/ncnn
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: corporate
  orgs:
  - Tencent
alternatives:
- framework/tensorflow-lite
registry_signals:
  github_stars: 24080
  downloads_monthly: 100000
  latest_version: '20240820'
  latest_release_date: '2024-08-20'
  observed_at: '2026-11-20'
  source: https://github.com/Tencent/ncnn
aliases:
- Tencent/ncnn
tags:
- edge-mobile
- arm
- lightweight
- mobile
updated: '2026-11-21'
sources:
- url: https://github.com/Tencent/ncnn
  title: GitHub repository
- url: https://github.com/Tencent/ncnn/wiki
  title: Documentation
- url: https://pypi.org/project/ncnn/
  title: ncnn — PyPI
---

## Overview

ncnn is a neural network inference framework optimized for mobile, embedded and desktop deployment. It is a pure C++ implementation with no third-party runtime dependencies, runs on CPU and Vulkan GPU backends, and converts PyTorch and ONNX models to ncnn through its pnnx tool.
