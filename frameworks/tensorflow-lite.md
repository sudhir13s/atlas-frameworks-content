---
id: framework/tensorflow-lite
type: framework
slug: tensorflow-lite
schema_version: 1.1
title: LiteRT
kind: library
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: 'Successor to TensorFlow Lite: Google''s on-device framework for ML and GenAI deployment on edge platforms, via conversion, runtime, and optimization.'
description: LiteRT is Google's on-device runtime for ML and GenAI deployment on edge platforms and continues TensorFlow Lite. It converts PyTorch, TensorFlow and JAX models to the .tflite format, quantizes them after training, and runs them with CPU, GPU and NPU acceleration on Android, iOS, the web, desktop and IoT devices.
best_for: On-device ML and GenAI inference, Mobile and embedded deployment
key_features:
- Conversion from PyTorch, TensorFlow and JAX models
- Post-training quantization
- GPU and NPU acceleration through the Compiled Model API
- Runtimes for Android, iOS, web, desktop and IoT
- Microcontroller and embedded deployment
- On-device training
- LLM inference through LiteRT-LM
use_cases:
- On-device ML inference
- On-device LLM and GenAI applications
- IoT and microcontroller ML
- Browser inference with LiteRT.js
pros:
- Runs on Android, iOS, web, desktop and IoT
- Built-in post-training quantizer
cons:
- Models must be converted to the .tflite or .litertlm format
- Not every operator runs on every accelerator
- Legacy TensorFlow Lite packages are in maintenance mode and receive only critical fixes
language: C++
languages_supported:
- Python
- C++
- Java
- Kotlin
- Swift
- JavaScript
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/google-ai-edge/LiteRT
docs_url: https://developers.google.com/edge/litert
website_url: https://developers.google.com/edge/litert
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
maturity: production
backing:
  type: corporate
  orgs:
  - Google
alternatives:
- framework/coreml-tools
- framework/executorch
ecosystem_connections:
- framework/tensorflow
registry_signals:
  github_stars: 3604
  downloads_monthly: 3000000
  latest_version: '2.18'
  latest_release_date: '2025-01-15'
  observed_at: '2026-11-20'
  source: https://github.com/google-ai-edge/LiteRT
aliases:
- TensorFlow Lite
- TFLite
- LiteRT (TensorFlow Lite)
tags:
- edge-mobile
- mobile
- quantization
- deployment
updated: '2026-11-21'
sources:
- url: https://github.com/google-ai-edge/LiteRT
  title: GitHub repository
- url: https://developers.google.com/edge/litert
  title: Documentation
- url: https://developers.google.com/edge/litert/overview
  title: LiteRT overview
- url: https://pypi.org/project/ai-edge-litert/
  title: ai-edge-litert — PyPI
---

## Overview

LiteRT is Google's on-device runtime for ML and GenAI deployment on edge platforms and continues TensorFlow Lite. It converts PyTorch, TensorFlow and JAX models to the .tflite format, quantizes them after training, and runs them with CPU, GPU and NPU acceleration on Android, iOS, the web, desktop and IoT devices.
