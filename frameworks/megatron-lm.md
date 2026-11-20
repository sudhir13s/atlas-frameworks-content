---
id: framework/megatron-lm
type: framework
slug: megatron-lm
schema_version: 1.1
title: Megatron-LM
kind: framework
category: framework-category/distributed-training
subcategory: training-framework
tagline: NVIDIA's framework for training massive transformer models
description: NVIDIA's library for efficient large-scale transformer training. Implements tensor parallelism, pipeline parallelism, and sequence parallelism. Used to train many of the largest language models including Megatron-Turing NLG.
best_for: Large-scale LLM pre-training on NVIDIA GPU clusters
not_ideal_for: Small-scale training, non-NVIDIA hardware, beginners
key_features:
- 3D parallelism (tensor, pipeline, data)
- Sequence parallelism
- Flash attention integration
- Optimized CUDA kernels
- Mixed precision training
- Efficient data loading
use_cases:
- Pre-training large language models
- Multi-node transformer training
- NVIDIA GPU cluster training
pros:
- Best performance on NVIDIA GPU clusters
- Proven at the largest scales
- Optimized CUDA kernels
cons:
- NVIDIA-only
- Complex codebase
- Not beginner-friendly
- Less modular than alternatives
language: Python
languages_supported:
- Python
- CUDA
maintained_by: NVIDIA
first_release: '2019-09-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/NVIDIA/Megatron-LM
docs_url: https://github.com/NVIDIA/Megatron-LM
website_url: https://github.com/NVIDIA/Megatron-LM
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: very-high
community_size: medium
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - NVIDIA
alternatives:
- framework/deepspeed
- framework/colossalai
ecosystem_connections:
- framework/deepspeed
- framework/pytorch
registry_signals:
  github_stars: 18445
  downloads_monthly: 200000
  latest_version: core_v0.20.1
  latest_release_date: '2026-11-19'
  observed_at: '2026-11-20'
  source: https://github.com/NVIDIA/Megatron-LM
aliases:
- NVIDIA/Megatron-LM
tags:
- distributed-training
- large-models
- nvidia
- transformers
updated: '2026-11-20'
sources:
- url: https://github.com/NVIDIA/Megatron-LM
  title: GitHub repository
---

## Overview

NVIDIA's library for efficient large-scale transformer training. Implements tensor parallelism, pipeline parallelism, and sequence parallelism. Used to train many of the largest language models including Megatron-Turing NLG.
