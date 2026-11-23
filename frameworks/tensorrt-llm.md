---
id: framework/tensorrt-llm
type: framework
slug: tensorrt-llm
schema_version: 3.0
title: TensorRT LLM
status: curated
kind: library
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: Open-sourced library for optimizing LLM and Visual Gen inference on NVIDIA GPUs.
description: TensorRT LLM is NVIDIA's open-source library for optimizing LLM and visual generation inference on NVIDIA GPUs. It is architected on PyTorch and provides a high-level Python LLM API for single-GPU, multi-GPU and multi-node deployments, with custom kernels for attention, GEMM and MoE operations and runtime optimizations such as speculative decoding and disaggregated serving.
best_for: LLM inference on NVIDIA GPUs
not_ideal_for: Hardware other than NVIDIA GPUs
key_features:
- Custom kernels for attention, GEMM and MoE operations
- FP8, FP4 and INT4 (AWQ, GPTQ) quantization
- In-flight batching
- Tensor, pipeline and expert parallelism across GPUs and nodes
- Paged KV cache with block reuse
- Speculative decoding (EAGLE, MTP, n-gram)
use_cases:
- LLM inference on NVIDIA GPUs
- Serving with NVIDIA Dynamo or Triton Inference Server
- Visual generation model inference
pros:
- Integrates with NVIDIA Dynamo and Triton Inference Server
- PyTorch-native model definitions that can be customized
cons:
- Runs only on NVIDIA GPUs
- The TensorRT engine backend has been removed; PyTorch is the only execution backend
- Collects anonymous telemetry by default (opt-out available)
language: Python
languages_supported:
- Python
maintained_by: NVIDIA
license_spdx: Apache-2.0
github_url: https://github.com/NVIDIA/TensorRT-LLM
docs_url: https://nvidia.github.io/TensorRT-LLM/
website_url: https://developer.nvidia.com/tensorrt
maturity: experimental
backing:
  type: corporate
  orgs:
  - organization/nvidia
alternatives:
- framework/vllm
- framework/llama-cpp
ecosystem_connections:
- framework/triton-inference-server
registry_signals:
  github_stars: 15108
  downloads_monthly: 5720
  latest_version: 1.3.0
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/NVIDIA/TensorRT-LLM
aliases:
- NVIDIA/TensorRT-LLM
- TensorRT-LLM
tags:
- llm
- inference
- nvidia
- optimization
- production
updated: '2026-11-21'
sources:
- url: https://github.com/NVIDIA/TensorRT-LLM
  title: GitHub repository
- url: https://nvidia.github.io/TensorRT-LLM/
  title: Documentation
- url: https://nvidia.github.io/TensorRT-LLM/overview.html
  title: TensorRT LLM overview
- url: https://nvidia.github.io/TensorRT-LLM/features/quantization.html
  title: Quantization
- url: https://nvidia.github.io/TensorRT-LLM/reference/support-matrix.html
  title: Support matrix
- url: https://nvidia.github.io/TensorRT-LLM/legacy/tensorrt-backend-removal.html
  title: 'Migration guide: TensorRT backend removed'
- url: https://pypi.org/project/tensorrt-llm/
  title: tensorrt-llm — PyPI
---


