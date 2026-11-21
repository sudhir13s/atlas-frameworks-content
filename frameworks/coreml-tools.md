---
id: framework/coreml-tools
type: framework
slug: coreml-tools
schema_version: 1.1
title: Core ML Tools
kind: library
category: framework-category/edge-mobile
subcategory: apple-ecosystem
tagline: Core ML tools contain supporting tools for Core ML model conversion, editing, and validation.
description: Core ML Tools (coremltools) is a Python package that converts machine learning models from third-party libraries such as TensorFlow, PyTorch, scikit-learn, XGBoost and LibSVM to the Core ML format. It also reads, writes and optimizes Core ML models, and verifies conversions on macOS by making predictions with Core ML. Converted models are integrated into apps with Xcode.
best_for: Converting trained models for apps that use Apple's Core ML
key_features:
- Conversion from PyTorch and TensorFlow
- Conversion from scikit-learn, XGBoost and LibSVM
- Reading and writing Core ML models
- Palettization, linear quantization and pruning
- Conversion verification through Core ML predictions on macOS
use_cases:
- Preparing models for Core ML apps built in Xcode
- Compressing models for the Neural Engine and GPU
pros:
- Converts both neural network and non-neural network models
- Converted models run on device through Core ML on the CPU, GPU and Neural Engine
cons:
- Output targets Apple's Core ML framework only
language: Python
languages_supported:
- Python
maintained_by: Apple
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
maturity: production
backing:
  type: corporate
  orgs:
  - Apple
alternatives:
- framework/tensorflow-lite
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
updated: '2026-11-21'
sources:
- url: https://github.com/apple/coremltools
  title: GitHub repository
- url: https://coremltools.readme.io/
  title: Documentation
- url: https://apple.github.io/coremltools/docs-guides/source/overview-coremltools.html
  title: Core ML Tools overview
- url: https://apple.github.io/coremltools/docs-guides/source/opt-overview.html
  title: Model compression overview
- url: https://pypi.org/project/coremltools/
  title: coremltools — PyPI
---

## Overview

Core ML Tools (coremltools) is a Python package that converts machine learning models from third-party libraries such as TensorFlow, PyTorch, scikit-learn, XGBoost and LibSVM to the Core ML format. It also reads, writes and optimizes Core ML models, and verifies conversions on macOS by making predictions with Core ML. Converted models are integrated into apps with Xcode.
