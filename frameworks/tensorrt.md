---
id: framework/tensorrt
type: framework
slug: tensorrt
schema_version: 3.0
title: TensorRT
status: curated
kind: library
category: framework-category/inference
subcategory: inference-optimizer
tagline: An SDK for high-performance deep learning inference on NVIDIA GPUs.
description: TensorRT is NVIDIA's SDK for optimizing deep learning inference on NVIDIA GPUs. It takes a trained model from a framework such as PyTorch, or an ONNX file, and compiles it into an engine tuned for one deployment configuration, using quantization, layer and tensor fusion and kernel tuning. It offers C++ and Python APIs, and its GitHub repository holds the open-source parts of the SDK, namely the plugins, the ONNX parser and sample applications.
best_for: Compiling trained models into optimized inference engines for NVIDIA GPUs
not_ideal_for: Hardware other than NVIDIA GPUs
key_features:
- Builds engines optimized for a specific deployment configuration
- Mixed precision across FP32, FP16, BF16, FP8, INT8, FP4 and INT4
- Quantization, layer and tensor fusion, and kernel tuning
- ONNX parser for importing models
- Custom layers through a plugin API
- C++ and Python APIs, plus the trtexec command-line tool
- Dynamic input shapes and weight refitting
use_cases:
- Low-latency inference on NVIDIA data-center GPUs
- Deploying models to workstations, laptops and Jetson edge devices
- A backend for Triton Inference Server
pros:
- Python package installs with pip install tensorrt
- Builds for Linux x86-64 and aarch64, Windows x86-64 and Jetson
- Used as a backend by Triton Inference Server and NVIDIA Dynamo
cons:
- Runs only on NVIDIA GPUs
- The SDK is under NVIDIA's own licence agreement; only the plugins, ONNX parser and samples are open source
- Version 11 removed weakly-typed networks, implicit quantization and IPluginV2, so older code may need changes
language: C++
languages_supported:
- C++
- Python
maintained_by: NVIDIA
license_note: 'TensorRT SDK: License Agreement for NVIDIA Software Development Kits. Open-source components in the GitHub repository (plugins, ONNX parser, samples): Apache-2.0'
github_url: https://github.com/NVIDIA/TensorRT
docs_url: https://docs.nvidia.com/deeplearning/tensorrt/latest/index.html
website_url: https://developer.nvidia.com/tensorrt
maturity: production
backing:
  type: corporate
  orgs:
  - organization/nvidia
alternatives:
- framework/onnx-runtime
ecosystem_connections:
- framework/tensorrt-llm
- framework/triton-inference-server
- framework/pytorch
- framework/onnx
registry_signals:
  github_stars: 13481
  downloads_monthly: 227930
  latest_version: '11.5'
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-25'
  source: https://github.com/NVIDIA/TensorRT
aliases:
- NVIDIA TensorRT
- NVIDIA/TensorRT
tags:
- inference
- nvidia
- optimization
- quantization
- gpu
updated: '2026-11-25'
sources:
- url: https://github.com/NVIDIA/TensorRT
  title: GitHub repository
- url: https://docs.nvidia.com/deeplearning/tensorrt/latest/index.html
  title: Documentation
- url: https://developer.nvidia.com/tensorrt
  title: NVIDIA TensorRT product page
- url: https://docs.nvidia.com/deeplearning/tensorrt/latest/reference/sla.html
  title: License Agreement for NVIDIA Software Development Kits
- url: https://pypistats.org/api/packages/tensorrt/recent
  title: tensorrt — PyPI download statistics
---


