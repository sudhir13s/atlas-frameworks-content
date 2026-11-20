---
id: framework/mnn
type: framework
slug: mnn
schema_version: 1.1
title: MNN
kind: framework
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: Alibaba's lightweight deep neural network inference engine for mobile
description: Alibaba's mobile inference engine optimized for on-device AI. Supports multiple platforms and hardware accelerators with automatic optimization. Used in production at Alibaba across mobile apps.
best_for: Mobile inference with multi-platform needs
not_ideal_for: Teams needing extensive English documentation
key_features:
- Multi-platform support
- Automatic optimization
- On-device training support
- Multiple backend (CPU, GPU, NPU)
- LLM inference support
use_cases:
- Mobile AI at Alibaba scale
- On-device inference
- Edge AI applications
pros:
- Good performance across platforms
- On-device training support
- Production-proven at Alibaba scale
cons:
- Smaller community outside China
- Documentation gaps in English
language: C++
languages_supported:
- C++
- Python
maintained_by: Alibaba
first_release: '2019-05-01'
license_spdx: Apache-2.0
github_url: https://github.com/alibaba/MNN
docs_url: https://www.yuque.com/mnn/en
website_url: https://github.com/alibaba/MNN
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: small-medium
maturity: production
signal_strength: low
backing:
  type: corporate
  orgs:
  - Alibaba
alternatives:
- framework/ncnn
- framework/tensorflow-lite
ecosystem_connections:
- framework/tensorflow
registry_signals:
  github_stars: 16583
  downloads_monthly: 50680
  latest_version: 3.6.2
  latest_release_date: '2026-10-29'
  observed_at: '2026-11-20'
  source: https://github.com/alibaba/MNN
aliases:
- alibaba/MNN
tags:
- edge-mobile
- mobile
- alibaba
- multi-platform
updated: '2026-11-20'
sources:
- url: https://github.com/alibaba/MNN
  title: GitHub repository
- url: https://www.yuque.com/mnn/en
  title: Documentation
---

## Overview

Alibaba's mobile inference engine optimized for on-device AI. Supports multiple platforms and hardware accelerators with automatic optimization. Used in production at Alibaba across mobile apps.
