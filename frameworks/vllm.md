---
id: framework/vllm
type: framework
slug: vllm
schema_version: 1.1
title: vLLM
kind: tool
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: A high-throughput and memory-efficient inference and serving engine for LLMs.
description: vLLM is a community-maintained library for LLM inference and serving. It manages attention key and value memory with PagedAttention, batches incoming requests continuously, and serves models through an OpenAI-compatible API server. It runs on NVIDIA, AMD and Intel GPUs and on x86, ARM and PowerPC CPUs, with plugins for other hardware such as Google TPUs.
best_for: LLM inference and serving
key_features:
- PagedAttention for attention key and value memory
- Continuous batching, chunked prefill and prefix caching
- Tensor, pipeline, data, expert and context parallelism
- OpenAI-compatible API server with Anthropic Messages API and gRPC support
- Speculative decoding (n-gram, suffix, EAGLE, DFlash)
- Quantization (FP8, INT8, INT4, GPTQ, AWQ, GGUF and more)
- Multi-LoRA serving
- Structured outputs and tool calling
use_cases:
- Production LLM serving
- OpenAI-compatible API deployment
- Offline batch inference
- Distributed multi-node inference
pros:
- OpenAI-compatible API server
- Integrates with Hugging Face models
- Runs on GPUs from several vendors and on CPUs
language: Python
languages_supported:
- Python
maintained_by: vLLM project
license_spdx: Apache-2.0
github_url: https://github.com/vllm-project/vllm
docs_url: https://docs.vllm.ai/
website_url: https://vllm.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: true
  google_tpu: true
backing:
  type: foundation
  orgs:
  - PyTorch Foundation
alternatives:
- framework/tensorrt-llm
- framework/llama-cpp
ecosystem_connections:
- framework/hugging-face-transformers
- framework/pytorch
- framework/ray-serve
registry_signals:
  github_stars: 97264
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
updated: '2026-11-21'
sources:
- url: https://github.com/vllm-project/vllm
  title: GitHub repository
- url: https://docs.vllm.ai/
  title: Documentation
- url: https://docs.vllm.ai/en/latest/models/supported_models/
  title: Supported models
- url: https://vllm.ai/
  title: vLLM website
- url: https://pytorch.org/projects/vllm/
  title: vLLM — PyTorch Foundation project page
- url: https://pypi.org/project/vllm/
  title: vllm — PyPI
---

## Overview

vLLM is a community-maintained library for LLM inference and serving. It manages attention key and value memory with PagedAttention, batches incoming requests continuously, and serves models through an OpenAI-compatible API server. It runs on NVIDIA, AMD and Intel GPUs and on x86, ARM and PowerPC CPUs, with plugins for other hardware such as Google TPUs.
