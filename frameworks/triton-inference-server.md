---
id: framework/triton-inference-server
type: framework
slug: triton-inference-server
schema_version: 1.1
title: Triton Inference Server
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: Open source inference serving software that streamlines AI inferencing.
description: Triton Inference Server is open source inference serving software from NVIDIA. It deploys models from multiple deep learning and machine learning frameworks, including TensorRT, PyTorch, ONNX, OpenVINO, Python and RAPIDS FIL, across cloud, data center, edge and embedded devices on NVIDIA GPUs, x86 and ARM CPUs, or AWS Inferentia.
best_for: Serving models from multiple frameworks in one server
key_features:
- Backends for TensorRT, PyTorch, ONNX Runtime, OpenVINO, Python and more
- Dynamic batching and sequence batching
- Concurrent model execution
- Model pipelines with ensembles and Business Logic Scripting
- HTTP/REST and gRPC inference protocols based on the KServe protocol
- C and Java APIs for in-process use
- Metrics for GPU utilization, throughput and latency
use_cases:
- Multi-framework production serving
- Inference pipelines with ensembles
- Real-time, batched and audio/video streaming inference
pros:
- Supports multiple frameworks through backends
- Custom backends in C/C++ or Python
- Runs on GPUs and CPUs
cons:
- Not every backend is supported on every platform
language: C++
languages_supported:
- C++
- Python
- Java
maintained_by: NVIDIA
license_spdx: BSD-3-Clause
github_url: https://github.com/triton-inference-server/server
docs_url: https://docs.nvidia.com/deeplearning/triton-inference-server/
website_url: https://developer.nvidia.com/triton-inference-server
maturity: production
backing:
  type: corporate
  orgs:
  - NVIDIA
alternatives:
- framework/bentoml
- framework/ray-serve
- framework/kserve
ecosystem_connections:
- framework/tensorrt-llm
- framework/onnx-runtime
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 11156
  downloads_monthly: 800000
  latest_version: 2.75.0
  latest_release_date: '2026-11-17'
  observed_at: '2026-11-20'
  source: https://github.com/triton-inference-server/server
aliases:
- triton-inference-server/server
- NVIDIA Triton Inference Server
tags:
- serving
- multi-framework
- nvidia
- production
- enterprise
updated: '2026-11-21'
sources:
- url: https://github.com/triton-inference-server/server
  title: GitHub repository
- url: https://docs.nvidia.com/deeplearning/triton-inference-server/
  title: Documentation
- url: https://developer.nvidia.com/dynamo-triton
  title: NVIDIA Dynamo-Triton product page
- url: https://github.com/triton-inference-server/backend
  title: Triton backends
- url: https://pypi.org/project/tritonclient/
  title: tritonclient — PyPI
---

## Overview

Triton Inference Server is open source inference serving software from NVIDIA. It deploys models from multiple deep learning and machine learning frameworks, including TensorRT, PyTorch, ONNX, OpenVINO, Python and RAPIDS FIL, across cloud, data center, edge and embedded devices on NVIDIA GPUs, x86 and ARM CPUs, or AWS Inferentia.
