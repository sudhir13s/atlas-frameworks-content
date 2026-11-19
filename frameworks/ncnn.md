---
id: framework/ncnn
type: framework
slug: ncnn
schema_version: 1.1
title: ncnn
kind: framework
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: High-performance neural network inference framework for mobile
description: Tencent's high-performance neural network inference framework optimized for mobile platforms. Written in C++ with no third-party dependencies. Known for exceptional performance on ARM devices.
best_for: Ultra-lightweight mobile inference on ARM
not_ideal_for: Western teams needing English documentation
key_features:
- No third-party dependencies
- ARM NEON optimization
- Vulkan GPU acceleration
- Quantization support
- Extremely small binary size
use_cases:
- Mobile inference on ARM devices
- Embedded systems ML
- Resource-constrained deployment
pros:
- Excellent ARM performance
- No dependencies
- Tiny binary size
cons:
- Limited model format support
- Documentation mostly in Chinese
- Smaller community outside China
language: C++
languages_supported:
- C++
- Python
maintained_by: Tencent
first_release: '2017-07-01'
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
learning_curve: high
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Tencent
alternatives:
- framework/mnn
- framework/tensorflow-lite
registry_signals:
  github_stars: 20800
  downloads_monthly: 100000
  latest_version: '20240820'
  latest_release_date: '2024-08-20'
  observed_at: '2026-06-15'
  source: https://github.com/Tencent/ncnn
aliases:
- Tencent/ncnn
tags:
- edge-mobile
- arm
- lightweight
- mobile
updated: '2026-11-19'
sources:
- url: https://github.com/Tencent/ncnn
  title: GitHub repository
- url: https://github.com/Tencent/ncnn/wiki
  title: Documentation
---

## Overview

Tencent's high-performance neural network inference framework optimized for mobile platforms. Written in C++ with no third-party dependencies. Known for exceptional performance on ARM devices.
