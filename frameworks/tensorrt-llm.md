---
id: framework/tensorrt-llm
type: framework
slug: tensorrt-llm
schema_version: 1.1
title: TensorRT-LLM
kind: library
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: NVIDIA's optimized inference library for LLMs on GPUs
description: NVIDIA's purpose-built library for optimized LLM inference on NVIDIA GPUs. Compiles models into highly optimized TensorRT engines with custom CUDA kernels. Achieves the lowest latency on NVIDIA hardware.
best_for: Enterprises committed to NVIDIA infrastructure needing lowest latency
not_ideal_for: Multi-vendor GPU environments, quick prototyping
key_features:
- Custom CUDA kernels for maximum NVIDIA GPU performance
- FP8/INT8/INT4 quantization
- Inflight batching
- Multi-GPU tensor parallelism
- KV-cache optimization
- Speculative decoding
use_cases:
- Lowest-latency LLM inference on NVIDIA GPUs
- Enterprise LLM deployment
- NVIDIA Triton integration
pros:
- Best latency on NVIDIA hardware
- Deep integration with NVIDIA ecosystem
- Production-grade reliability
cons:
- NVIDIA-only — no AMD/Apple support
- Complex build and compilation process
- Model support lags behind vLLM
language: Python
languages_supported:
- Python
- C++
- CUDA
maintained_by: NVIDIA
first_release: '2023-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/NVIDIA/TensorRT-LLM
docs_url: https://nvidia.github.io/TensorRT-LLM/
website_url: https://developer.nvidia.com/tensorrt
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: medium
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - NVIDIA
alternatives:
- framework/vllm
- framework/llama-cpp
ecosystem_connections:
- framework/triton-inference-server
registry_signals:
  github_stars: 9500
  downloads_monthly: 500000
  latest_version: '0.17'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/NVIDIA/TensorRT-LLM
aliases:
- NVIDIA/TensorRT-LLM
tags:
- llm
- inference
- nvidia
- optimization
- production
updated: '2026-11-19'
sources:
- url: https://github.com/NVIDIA/TensorRT-LLM
  title: GitHub repository
- url: https://nvidia.github.io/TensorRT-LLM/
  title: Documentation
---

## Overview

NVIDIA's purpose-built library for optimized LLM inference on NVIDIA GPUs. Compiles models into highly optimized TensorRT engines with custom CUDA kernels. Achieves the lowest latency on NVIDIA hardware.
