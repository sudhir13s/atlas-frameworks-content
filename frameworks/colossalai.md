---
id: framework/colossalai
type: framework
slug: colossalai
schema_version: 1.1
title: Colossal-AI
kind: framework
category: framework-category/distributed-training
subcategory: training-framework
tagline: Making large AI models cheaper, faster and more accessible.
description: Colossal-AI is a unified system that provides an integrated set of training skills and utilities for large models. It offers data, pipeline, tensor and sequence parallelism, the Zero Redundancy Optimizer (ZeRO), auto-parallelism and heterogeneous memory management, and injects these features into a PyTorch model and optimizer through its Booster.
best_for: Scaling PyTorch training of large models across NVIDIA GPUs and nodes
not_ideal_for: Non-Linux systems (only Linux is supported), Hardware without NVIDIA CUDA GPUs
key_features:
- Data and pipeline parallelism
- Multi-dimensional tensor parallelism
- Sequence parallelism
- Zero Redundancy Optimizer (ZeRO) with CPU offload
- Auto-parallelism
- Gemini plugin with chunk-based heterogeneous memory management
- Booster plugins including wrappers for PyTorch DDP and FSDP
- Mixed precision training and gradient accumulation
- RLHF pipeline in the ColossalChat application
use_cases:
- Large model pretraining and fine-tuning
- RLHF training with ColossalChat
- Training video generation models such as Open-Sora
pros:
- Parallelism configured from a configuration file
- Parallel strategies can be picked and combined in one plugin
- Docker images published on Docker Hub
cons:
- Only Linux is supported
- Requires CUDA and an NVIDIA GPU
- The Hybrid Parallel plugin works only with the Hugging Face Transformers models that Shardformer supports
- The Torch FSDP plugin does not support saving or loading sharded checkpoints
language: Python
languages_supported:
- Python
maintained_by: HPC-AI Tech
license_spdx: Apache-2.0
github_url: https://github.com/hpcaitech/ColossalAI
docs_url: https://colossalai.org/docs/get_started/installation/
website_url: https://colossalai.org/
backing:
  type: corporate
  orgs:
  - HPC-AI Tech
alternatives:
- framework/deepspeed
- framework/megatron-lm
ecosystem_connections:
- framework/pytorch
- framework/hugging-face-transformers
registry_signals:
  github_stars: 41420
  downloads_monthly: 5593
  latest_version: 0.5.0
  latest_release_date: '2025-06-04'
  observed_at: '2026-11-20'
  source: https://github.com/hpcaitech/ColossalAI
aliases:
- hpcaitech/ColossalAI
- ColossalAI
tags:
- distributed-training
- large-models
- accessible
- memory-optimization
updated: '2026-11-21'
sources:
- url: https://github.com/hpcaitech/ColossalAI
  title: GitHub repository
- url: https://colossalai.org/docs/get_started/installation/
  title: Documentation
- url: https://colossalai.org/docs/concepts/colossalai_overview
  title: Colossal-AI overview
- url: https://colossalai.org/docs/basics/booster_plugins
  title: Booster plugins
- url: https://pypi.org/project/colossalai/
  title: colossalai — PyPI
---

## Overview

Colossal-AI is a unified system that provides an integrated set of training skills and utilities for large models. It offers data, pipeline, tensor and sequence parallelism, the Zero Redundancy Optimizer (ZeRO), auto-parallelism and heterogeneous memory management, and injects these features into a PyTorch model and optimizer through its Booster.
