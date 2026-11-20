---
id: framework/deepspeed
type: framework
slug: deepspeed
schema_version: 1.1
title: DeepSpeed
kind: library
category: framework-category/distributed-training
subcategory: training-optimization
tagline: Deep learning optimization library for distributed training and inference at scale
description: Microsoft's library for efficient distributed training and inference of large models. Pioneered ZeRO (Zero Redundancy Optimizer) for memory-efficient training. Enables training models with trillions of parameters across hundreds of GPUs.
best_for: Training very large models with limited GPU memory
not_ideal_for: Small models on single GPU, non-PyTorch frameworks
key_features:
- ZeRO stages 1-3 for memory optimization
- ZeRO-Infinity for NVMe offloading
- Mixed precision training
- Pipeline parallelism
- Sparse attention
- DeepSpeed-Inference for optimized serving
- DeepSpeed-Chat for RLHF training
use_cases:
- Training billion+ parameter models
- Memory-efficient distributed training
- RLHF training for LLMs
- Large-scale model fine-tuning
pros:
- Best memory efficiency for large model training
- ZeRO is widely adopted and proven
- Good Hugging Face integration
- Active development
cons:
- Configuration complexity
- Can conflict with other distributed training libraries
- Documentation could be better
language: Python
languages_supported:
- Python
- C++
- CUDA
maintained_by: Microsoft Research
first_release: '2020-02-01'
license_spdx: Apache-2.0
github_url: https://github.com/microsoft/DeepSpeed
docs_url: https://www.deepspeed.ai/getting-started/
website_url: https://www.deepspeed.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: true
  google_tpu: false
learning_curve: high
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Microsoft
  funding_or_parent: Microsoft Research
alternatives:
- framework/pytorch-fsdp
- framework/colossalai
- framework/megatron-lm
ecosystem_connections:
- framework/pytorch
- framework/hugging-face-transformers
- framework/megatron-lm
registry_signals:
  github_stars: 43347
  downloads_monthly: 2000000
  latest_version: 0.20.0
  latest_release_date: '2026-11-12'
  observed_at: '2026-11-20'
  source: https://github.com/microsoft/DeepSpeed
aliases:
- microsoft/DeepSpeed
tags:
- distributed-training
- optimization
- large-models
- zero
updated: '2026-11-20'
sources:
- url: https://github.com/microsoft/DeepSpeed
  title: GitHub repository
- url: https://www.deepspeed.ai/getting-started/
  title: Documentation
---

## Overview

Microsoft's library for efficient distributed training and inference of large models. Pioneered ZeRO (Zero Redundancy Optimizer) for memory-efficient training. Enables training models with trillions of parameters across hundreds of GPUs.
