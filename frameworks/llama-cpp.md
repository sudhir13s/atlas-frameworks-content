---
id: framework/llama-cpp
type: framework
slug: llama-cpp
schema_version: 1.1
title: llama.cpp
kind: library
category: framework-category/llm-frameworks
subcategory: inference-engine
tagline: LLM inference in C/C++.
description: llama.cpp is a C/C++ project for LLM and multimodal LLM inference with minimal setup on a wide range of hardware, locally and in the cloud. It is built on the ggml library, runs models in the GGUF format, and includes a command-line tool and an HTTP server with OpenAI-compatible routes.
best_for: LLM inference with minimal setup on local hardware, Running GGUF models on CPU or GPU
key_features:
- GGUF model format with quantization tool (llama-quantize)
- CPU inference with optional BLAS acceleration
- Metal GPU acceleration on macOS (enabled by default)
- CUDA, HIP (ROCm), SYCL, Vulkan, MUSA and CANN backends
- llama-server HTTP server with OpenAI-compatible chat completions and embeddings routes
- Multimodal input
- Multi-GPU usage
- GBNF grammars for constrained output
use_cases:
- Local LLM inference
- Self-hosted OpenAI-compatible API server
- On-device inference (Android and Apple platforms)
pros:
- Runs on CPU without a GPU
- Pre-built binaries and Docker images
- Wide range of hardware backends
language: C++
languages_supported:
- C
- C++
maintained_by: ggml
license_spdx: MIT
github_url: https://github.com/ggml-org/llama.cpp
docs_url: https://github.com/ggml-org/llama.cpp/blob/master/README.md
website_url: https://github.com/ggml-org/llama.cpp
backing:
  type: community
alternatives:
- framework/ollama
- framework/vllm
registry_signals:
  github_stars: 135826
  downloads_monthly: 2000000
  latest_version: b4000+
  latest_release_date: '2025-03-01'
  observed_at: '2026-11-20'
  source: https://github.com/ggerganov/llama.cpp
aliases:
- ggerganov/llama.cpp
- ggml-org/llama.cpp
tags:
- llm
- inference
- local
- cpu
- quantization
- edge
updated: '2026-11-21'
sources:
- url: https://github.com/ggml-org/llama.cpp
  title: GitHub repository
- url: https://github.com/ggml-org/llama.cpp/blob/master/README.md
  title: Documentation
- url: https://github.com/ggml-org/llama.cpp/blob/master/docs/build.md
  title: How to build
- url: https://github.com/ggml-org/llama.cpp/blob/master/tools/server/README.md
  title: llama-server
- url: https://github.com/ggml-org/llama.cpp/blob/master/tools/quantize/README.md
  title: llama-quantize
- url: https://github.com/ggml-org
  title: ggml organisation
---

## Overview

llama.cpp is a C/C++ project for LLM and multimodal LLM inference with minimal setup on a wide range of hardware, locally and in the cloud. It is built on the ggml library, runs models in the GGUF format, and includes a command-line tool and an HTTP server with OpenAI-compatible routes.
