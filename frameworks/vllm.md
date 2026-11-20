---
id: framework/vllm
type: framework
slug: vllm
schema_version: 1.1
title: vLLM
kind: tool
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: High-throughput and memory-efficient inference engine for LLMs
description: State-of-the-art LLM serving engine featuring PagedAttention for efficient memory management. Achieves 2-4x higher throughput than naive HF Transformers inference. Supports continuous batching, tensor parallelism, and OpenAI-compatible API serving.
best_for: Production LLM serving with maximum throughput
not_ideal_for: CPU inference, edge/mobile deployment, non-LLM models
key_features:
- PagedAttention for efficient KV-cache management
- Continuous batching for maximum throughput
- Tensor parallelism for multi-GPU serving
- OpenAI-compatible API server
- Speculative decoding
- Quantization support (AWQ, GPTQ, FP8)
- LoRA serving without model reloading
use_cases:
- Production LLM serving
- ChatGPT-like API deployment
- High-throughput batch inference
- Multi-tenant LLM hosting
pros:
- Best throughput for LLM serving
- Drop-in OpenAI API replacement
- Active development and fast adoption
- Supports most popular LLM architectures
cons:
- GPU-only (no CPU inference)
- Memory requirements still high for large models
- API can change rapidly between versions
language: Python
languages_supported:
- Python
- C++
- CUDA
maintained_by: vLLM team (UC Berkeley origin)
first_release: '2023-06-01'
license_spdx: Apache-2.0
github_url: https://github.com/vllm-project/vllm
docs_url: https://docs.vllm.ai/
website_url: https://vllm.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
learning_curve: low
community_size: large
maturity: production
signal_strength: high
backing:
  type: foundation
  orgs:
  - UC Berkeley Sky Computing Lab
  funding_or_parent: Originated at UC Berkeley; community-governed with contributions from Anyscale, Neural Magic, and others
alternatives:
- framework/tensorrt-llm
- framework/llama-cpp
ecosystem_connections:
- framework/hugging-face-transformers
- framework/pytorch
- framework/ray-serve
registry_signals:
  github_stars: 97259
  downloads_monthly: 2732584
  latest_version: 0.34.0
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-20'
  source: https://github.com/vllm-project/vllm
aliases:
- vllm-project/vllm
tags:
- llm
- inference
- serving
- high-throughput
- production
updated: '2026-11-20'
sources:
- url: https://github.com/vllm-project/vllm
  title: GitHub repository
- url: https://docs.vllm.ai/
  title: Documentation
---

## Overview

State-of-the-art LLM serving engine featuring PagedAttention for efficient memory management. Achieves 2-4x higher throughput than naive HF Transformers inference. Supports continuous batching, tensor parallelism, and OpenAI-compatible API serving.
