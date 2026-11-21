---
id: framework/megatron-lm
type: framework
slug: megatron-lm
schema_version: 1.1
title: Megatron-LM
kind: framework
category: framework-category/distributed-training
subcategory: training-framework
tagline: Ongoing research training transformer models at scale.
description: Megatron-LM is a GPU-optimized library from NVIDIA for training transformer models at scale. The repository contains Megatron Core, a composable library of transformer building blocks, parallelism strategies and mixed precision support for custom training frameworks, and Megatron-LM, a reference example with pre-configured training scripts.
best_for: Large-scale transformer training on NVIDIA GPUs, Building custom training frameworks from GPU-optimized building blocks
key_features:
- Tensor, pipeline, data, expert and context parallelism
- Mixed precision (FP16, BF16, FP8, FP4)
- Composable transformer building blocks
- Distributed optimizers and pipeline schedules
- Distributed checkpoint saving, loading and resharding
- Dataloaders and dataset utilities
- Model architectures including LLaMA, Qwen, DeepSeek, GPT and Mamba
use_cases:
- Pre-training large language models
- Multi-node transformer training
- Building custom training pipelines
pros:
- Megatron Core is installable on its own from PyPI
- Pre-configured training scripts for experimentation
cons:
- Documented hardware requirements cover NVIDIA GPUs only (Turing or later recommended; FP8 needs Hopper, Ada or Blackwell)
language: Python
languages_supported:
- Python
maintained_by: NVIDIA
github_url: https://github.com/NVIDIA/Megatron-LM
docs_url: https://github.com/NVIDIA/Megatron-LM
website_url: https://github.com/NVIDIA/Megatron-LM
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
maturity: production
backing:
  type: corporate
  orgs:
  - NVIDIA
alternatives:
- framework/deepspeed
- framework/colossalai
ecosystem_connections:
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
updated: '2026-11-21'
sources:
- url: https://github.com/NVIDIA/Megatron-LM
  title: GitHub repository
- url: https://docs.nvidia.com/megatron-core/developer-guide/latest/index.html
  title: Megatron Core developer guide
- url: https://docs.nvidia.com/megatron-core/developer-guide/latest/get-started/install.html
  title: Installation guide
- url: https://pypi.org/project/megatron-core/
  title: megatron-core — PyPI
- url: https://github.com/NVIDIA/Megatron-LM/blob/main/LICENSE
  title: Megatron-LM LICENSE
license_note: BSD-3-Clause for NVIDIA code per the LICENSE file, with Apache-2.0 and other licences for included third-party code (the README badge and the megatron-core PyPI licence field say Apache 2.0)
---

## Overview

Megatron-LM is a GPU-optimized library from NVIDIA for training transformer models at scale. The repository contains Megatron Core, a composable library of transformer building blocks, parallelism strategies and mixed precision support for custom training frameworks, and Megatron-LM, a reference example with pre-configured training scripts.
