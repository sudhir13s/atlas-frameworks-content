---
id: framework/ollama
type: framework
slug: ollama
schema_version: 1.1
title: Ollama
kind: tool
category: framework-category/llm-frameworks
subcategory: inference-runtime
tagline: Get up and running with large language models locally
description: User-friendly runtime for running LLMs locally. Wraps llama.cpp with a simple CLI and REST API. One-command model pulling and serving. The easiest way to run open-source LLMs on a local machine.
best_for: Developers wanting the easiest path to local LLM inference
not_ideal_for: Production serving at scale, fine-tuning, custom inference optimization
key_features:
- One-command model download and run
- REST API for local serving
- Modelfile for custom models
- Multi-model concurrency
- Automatic GPU detection
- OpenAI-compatible API
use_cases:
- Local AI development and testing
- Privacy-preserving AI applications
- Developer tooling integration
- Offline AI assistants
pros:
- Simplest setup for local LLMs
- Large model library
- Great developer experience
- Active development
cons:
- Not designed for production serving at scale
- Limited customization compared to raw llama.cpp
- No distributed serving
language: Go
languages_supported:
- Go
- Python
- JavaScript
maintained_by: Ollama Inc.
first_release: '2023-08-01'
license_spdx: MIT
github_url: https://github.com/ollama/ollama
docs_url: https://ollama.com/docs
website_url: https://ollama.com/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: very-low
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Ollama Inc
alternatives:
- framework/llama-cpp
ecosystem_connections:
- framework/llama-cpp
- framework/langchain
registry_signals:
  github_stars: 187735
  downloads_monthly: 5000000
  latest_version: 0.40.16
  latest_release_date: '2026-11-09'
  observed_at: '2026-11-20'
  source: https://github.com/ollama/ollama
aliases:
- ollama/ollama
tags:
- llm
- local
- developer-tools
- inference
- easy-setup
updated: '2026-11-20'
sources:
- url: https://github.com/ollama/ollama
  title: GitHub repository
- url: https://ollama.com/docs
  title: Documentation
---

## Overview

User-friendly runtime for running LLMs locally. Wraps llama.cpp with a simple CLI and REST API. One-command model pulling and serving. The easiest way to run open-source LLMs on a local machine.
