---
id: framework/mlx
type: framework
slug: mlx
schema_version: 3.0
title: MLX
status: curated
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: An array framework for Apple silicon.
description: MLX is an array framework for machine learning on Apple silicon, created by Apple's machine learning research team. Its Python API closely follows NumPy, and its mlx.nn and mlx.optimizers packages follow PyTorch-style APIs. It offers composable function transformations for automatic differentiation, vectorization and graph optimization, evaluates arrays lazily and builds graphs dynamically. Arrays live in unified memory, so operations run on the CPU or GPU without copying data. Besides macOS, it installs on Linux with a CUDA backend or for the CPU alone.
best_for: Training and running models on Apple silicon Macs
not_ideal_for: Projects that need the wider PyTorch or JAX library ecosystem
key_features:
- NumPy-like Python API, with C++, C and Swift APIs
- Composable automatic differentiation, vectorization and graph optimization
- Lazy computation and dynamic graph construction
- Unified memory shared by CPU and GPU
- Neural network layers (mlx.nn) and optimizers (mlx.optimizers)
- Distributed communication operations
- Metal and CUDA backends
use_cases:
- Training and fine-tuning models on a Mac
- Local LLM text generation and LoRA fine-tuning
- Machine-learning research on Apple silicon
pros:
- No data copies between CPU and GPU, thanks to unified memory
- Changing argument shapes does not trigger slow recompilation
- Example repository covers language models, LoRA fine-tuning, Stable Diffusion and Whisper
language: C++
languages_supported:
- Python
- C++
- C
- Swift
maintained_by: Apple machine learning research
license_spdx: MIT
github_url: https://github.com/ml-explore/mlx
docs_url: https://ml-explore.github.io/mlx/build/html/index.html
backing:
  type: corporate
  orgs:
  - organization/apple
alternatives:
- framework/pytorch
- framework/jax
registry_signals:
  github_stars: 29281
  downloads_monthly: 1518405
  latest_version: 0.32.4
  latest_release_date: '2026-10-14'
  observed_at: '2026-11-25'
  source: https://github.com/ml-explore/mlx
aliases:
- Apple MLX
- ml-explore/mlx
tags:
- deep-learning
- apple-silicon
- arrays
- autograd
updated: '2026-11-25'
sources:
- url: https://github.com/ml-explore/mlx
  title: GitHub repository
- url: https://ml-explore.github.io/mlx/build/html/index.html
  title: Documentation
- url: https://pypistats.org/api/packages/mlx/recent
  title: mlx — PyPI download statistics
---


