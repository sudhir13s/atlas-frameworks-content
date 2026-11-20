---
id: framework/llama-cpp
type: framework
slug: llama-cpp
schema_version: 1.1
title: llama.cpp
kind: library
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: LLM inference in pure C/C++ — run models on consumer hardware
description: Minimal C/C++ implementation for running LLMs on consumer hardware including CPUs, Apple Silicon, and modest GPUs. Pioneered the GGUF quantization format. Enables running 7B-70B parameter models on laptops and desktops.
best_for: Running LLMs locally on consumer hardware, privacy-focused applications
not_ideal_for: High-throughput production serving, training
key_features:
- CPU inference with AVX/ARM NEON optimization
- GGUF quantization format (2-8 bit)
- Apple Metal GPU acceleration
- CUDA and Vulkan GPU backends
- OpenAI-compatible server mode
- Supports 100+ model architectures
- Low memory footprint
use_cases:
- Local LLM inference on consumer hardware
- Privacy-preserving on-device AI
- Offline AI applications
- Edge deployment
pros:
- Runs on consumer hardware without GPU
- Excellent Apple Silicon performance
- Active community and rapid model support
- Very low resource requirements with quantization
cons:
- Lower throughput than GPU-optimized solutions
- Quality degrades with aggressive quantization
- C++ codebase harder to contribute to
language: C++
languages_supported:
- C
- C++
- Python
maintained_by: Georgi Gerganov + community
first_release: '2023-03-10'
license_spdx: MIT
github_url: https://github.com/ggerganov/llama.cpp
docs_url: https://github.com/ggerganov/llama.cpp/blob/master/README.md
website_url: https://github.com/ggerganov/llama.cpp
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: true
  google_tpu: false
learning_curve: low
community_size: large
maturity: production
signal_strength: high
backing:
  type: community
  funding_or_parent: Created by Georgi Gerganov; community-driven (ggml.ai ecosystem)
alternatives:
- framework/ollama
- framework/vllm
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 135819
  downloads_monthly: 2000000
  latest_version: b4000+
  latest_release_date: '2025-03-01'
  observed_at: '2026-11-20'
  source: https://github.com/ggerganov/llama.cpp
aliases:
- ggerganov/llama.cpp
tags:
- llm
- inference
- local
- cpu
- quantization
- edge
updated: '2026-11-20'
sources:
- url: https://github.com/ggerganov/llama.cpp
  title: GitHub repository
- url: https://github.com/ggerganov/llama.cpp/blob/master/README.md
  title: Documentation
---

## Overview

Minimal C/C++ implementation for running LLMs on consumer hardware including CPUs, Apple Silicon, and modest GPUs. Pioneered the GGUF quantization format. Enables running 7B-70B parameter models on laptops and desktops.
