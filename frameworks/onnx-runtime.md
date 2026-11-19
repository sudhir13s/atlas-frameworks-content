---
id: framework/onnx-runtime
type: framework
slug: onnx-runtime
schema_version: 1.1
title: ONNX Runtime
kind: library
category: framework-category/llm-serving
subcategory: inference-runtime
tagline: Cross-platform, high-performance ML inference engine
description: Microsoft's high-performance inference engine for ONNX models. Supports models from PyTorch, TensorFlow, scikit-learn, and more via ONNX format. Runs on CPU, GPU, mobile, and edge with hardware-specific optimizations.
best_for: Cross-platform model deployment from any training framework
not_ideal_for: Models with operations not supported in ONNX, training workloads
key_features:
- Cross-platform inference (cloud, mobile, edge, browser)
- Hardware-specific optimizations
- Quantization and graph optimization
- Multi-language bindings
- ONNX model format support
- Mobile and web runtime
use_cases:
- Cross-platform model deployment
- Optimized inference across hardware
- Mobile and edge deployment
- Converting PyTorch/TF models for production
pros:
- Best cross-platform inference story
- Wide hardware support
- Good optimization passes
- Production-proven at Microsoft scale
cons:
- ONNX conversion can lose model features
- Not all operations supported in ONNX format
- Less community momentum than native framework serving
language: C++
languages_supported:
- Python
- C++
- C#
- Java
- JavaScript
maintained_by: Microsoft
first_release: '2019-05-01'
license_spdx: MIT
github_url: https://github.com/microsoft/onnxruntime
docs_url: https://onnxruntime.ai/docs/
website_url: https://onnxruntime.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: true
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Microsoft
  funding_or_parent: Microsoft (ONNX format is an LF AI & Data Foundation project)
alternatives:
- framework/tensorrt-llm
- framework/triton-inference-server
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 15500
  downloads_monthly: 8000000
  latest_version: '1.20'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/microsoft/onnxruntime
tags:
- serving
- inference
- cross-platform
- optimization
- onnx
updated: '2026-11-19'
sources:
- url: https://github.com/microsoft/onnxruntime
  title: GitHub repository
- url: https://onnxruntime.ai/docs/
  title: Documentation
---

## Overview

Microsoft's high-performance inference engine for ONNX models. Supports models from PyTorch, TensorFlow, scikit-learn, and more via ONNX format. Runs on CPU, GPU, mobile, and edge with hardware-specific optimizations.
