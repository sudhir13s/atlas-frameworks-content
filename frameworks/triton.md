---
id: framework/triton
type: framework
slug: triton
schema_version: 3.0
title: Triton
status: curated
kind: library
category: framework-category/gpu-programming
subcategory: kernel-language
tagline: A language and compiler for parallel programming.
description: Triton is an open-source, Python-based language and compiler for writing custom deep-learning compute kernels that run at high throughput on GPUs. It aims to be more productive than CUDA and more flexible than other domain-specific languages, and its compiler handles memory coalescing, shared memory management and scheduling inside streaming multiprocessors. It grew out of a 2019 MAPL paper by Philippe Tillet, and OpenAI released Triton 1.0 in July 2021. It is not Triton Inference Server, NVIDIA's model-serving software.
best_for: Writing custom GPU kernels in Python without hand-written CUDA
not_ideal_for: Platforms other than Linux, or NVIDIA GPUs below compute capability 8.0
key_features:
- Python-based kernel language with the triton.language module
- Compiler that automates memory coalescing, shared memory management and scheduling
- Runs on NVIDIA GPUs (compute capability 8.0 or higher) and AMD GPUs (ROCm 6.2 or higher)
- Testing and benchmarking helpers in triton.testing
- Kernels can be debugged with Python breakpoints
use_cases:
- Custom fused kernels for deep-learning models
- Matrix multiplication and attention kernels
- Research on new GPU operators
pros:
- Installs with pip install triton, with binary wheels for CPython 3.10 to 3.14
- One kernel language for NVIDIA and AMD GPUs
- OpenAI reported FP16 matrix multiplication matching cuBLAS in under 25 lines of code
cons:
- Linux only
- CPU support is still under development
languages_supported:
- Python
maintained_by: triton-lang
license_spdx: MIT
github_url: https://github.com/triton-lang/triton
docs_url: https://triton-lang.org/main/index.html
website_url: https://triton-lang.org/
alternatives:
- framework/rocm
- framework/oneapi
registry_signals:
  github_stars: 20637
  downloads_monthly: 47071319
  latest_version: 3.9.0
  latest_release_date: '2026-10-27'
  observed_at: '2026-11-25'
  source: https://github.com/triton-lang/triton
aliases:
- OpenAI Triton
- triton-lang/triton
- Triton language
tags:
- gpu-programming
- kernels
- compiler
- gpu
updated: '2026-11-25'
sources:
- url: https://github.com/triton-lang/triton
  title: GitHub repository
- url: https://triton-lang.org/main/index.html
  title: Documentation
- url: https://openai.com/index/triton/
  title: 'Introducing Triton: Open-source GPU programming for neural networks (OpenAI)'
- url: https://pypistats.org/api/packages/triton/recent
  title: triton — PyPI download statistics
---


