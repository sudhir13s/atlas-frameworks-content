---
id: framework/pytorch-fsdp
type: framework
slug: pytorch-fsdp
schema_version: 1.1
title: PyTorch FSDP
kind: library
category: framework-category/distributed-training
subcategory: training-optimization
tagline: Fully Sharded Data Parallel — native PyTorch distributed training
description: PyTorch's native fully sharded data parallel training, inspired by DeepSpeed ZeRO. Shards model parameters, gradients, and optimizer states across GPUs. Part of PyTorch core — no additional library needed.
best_for: PyTorch users wanting native distributed training without external dependencies
not_ideal_for: Extreme-scale training needing NVMe offloading (use DeepSpeed ZeRO-Infinity)
key_features:
- Full parameter sharding across GPUs
- Gradient and optimizer state sharding
- Native PyTorch integration
- Mixed precision support
- CPU offloading
- Activation checkpointing
use_cases:
- Training large models in PyTorch natively
- Multi-GPU training without external libraries
- Production training pipelines
pros:
- No external dependency — part of PyTorch
- Tight integration with PyTorch ecosystem
- Simpler than configuring DeepSpeed
cons:
- Less mature than DeepSpeed for extreme scale
- Configuration can still be tricky
- Fewer optimizations than DeepSpeed ZeRO-Infinity
language: Python
languages_supported:
- Python
maintained_by: Meta AI (PyTorch Foundation)
first_release: '2022-03-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/pytorch
docs_url: https://pytorch.org/docs/stable/fsdp.html
website_url: https://pytorch.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Meta
  - PyTorch Foundation
alternatives:
- framework/deepspeed
- framework/colossalai
ecosystem_connections:
- framework/pytorch
- framework/hugging-face-transformers
registry_signals:
  github_stars: 87000
  downloads_monthly: 15000000
  latest_version: '2.6'
  latest_release_date: '2025-01-29'
  observed_at: '2026-06-15'
  source: https://github.com/pytorch/pytorch
tags:
- distributed-training
- pytorch
- native
- sharding
updated: '2026-11-19'
sources:
- url: https://github.com/pytorch/pytorch
  title: GitHub repository
- url: https://pytorch.org/docs/stable/fsdp.html
  title: Documentation
---

## Overview

PyTorch's native fully sharded data parallel training, inspired by DeepSpeed ZeRO. Shards model parameters, gradients, and optimizer states across GPUs. Part of PyTorch core — no additional library needed.
