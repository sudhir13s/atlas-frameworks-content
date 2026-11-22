---
id: framework/onnx-runtime
type: framework
slug: onnx-runtime
schema_version: 1.1
title: ONNX Runtime
kind: library
category: framework-category/llm-serving
subcategory: inference-runtime
tagline: ONNX Runtime is a runtime accelerator for Machine Learning models.
description: ONNX Runtime is a cross-platform machine-learning model accelerator with an interface for integrating hardware-specific libraries as execution providers. It runs models from PyTorch, TensorFlow/Keras, TFLite, scikit-learn and other frameworks once they are exported to the ONNX format, and it also supports on-device training.
best_for: Deploying models trained in different frameworks, Running one model across hardware and operating systems
key_features:
- Cross-platform inference on Windows, mobile, web and IoT devices
- Hardware execution providers such as CUDA, TensorRT, OpenVINO, DirectML and CoreML
- Quantization and graph optimization
- Multi-language bindings
- ONNX model format support
- On-device training
use_cases:
- Cross-platform model deployment
- Optimized inference across hardware
- Mobile and edge deployment
- Deploying Python-trained models in C#, C++ or Java apps
pros:
- Execution providers for NVIDIA, AMD, Intel, Apple, Qualcomm and Arm hardware
- Built-in graph optimizations and quantization tools
cons:
- ROCm execution provider removed; AMD GPUs now use the MIGraphX execution provider
language: C++
languages_supported:
- Python
- C++
- C
- C#
- Java
- JavaScript
- Objective-C
maintained_by: Microsoft
license_spdx: MIT
docs_url: https://onnxruntime.ai/docs/
website_url: https://onnxruntime.ai/
maturity: production
backing:
  type: corporate
  orgs:
  - Microsoft
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
updated: '2026-11-21'
sources:
- url: https://onnxruntime.ai/docs/
  title: Documentation
- url: https://onnxruntime.ai/docs/execution-providers/MIGraphX-ExecutionProvider.html
  title: AMD - MIGraphX execution provider
- url: https://onnxruntime.ai/docs/execution-providers/ROCm-ExecutionProvider.html
  title: AMD - ROCm execution provider
- url: https://onnxruntime.ai/docs/execution-providers/CoreML-ExecutionProvider.html
  title: Apple - CoreML execution provider
- url: https://onnxruntime.ai/docs/execution-providers/oneDNN-ExecutionProvider.html
  title: Intel - oneDNN execution provider
- url: https://onnxruntime.ai/
  title: Website
- url: https://pypi.org/project/onnxruntime/
  title: onnxruntime — PyPI
---

## Overview

ONNX Runtime is a cross-platform machine-learning model accelerator with an interface for integrating hardware-specific libraries as execution providers. It runs models from PyTorch, TensorFlow/Keras, TFLite, scikit-learn and other frameworks once they are exported to the ONNX format, and it also supports on-device training.
