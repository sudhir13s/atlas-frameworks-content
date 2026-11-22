---
id: framework/deepspeed
type: framework
slug: deepspeed
schema_version: 1.1
title: DeepSpeed
kind: library
category: framework-category/distributed-training
subcategory: training-optimization
tagline: Deep learning optimization library that makes distributed training and inference easy, efficient, and effective.
description: DeepSpeed is a deep learning optimization library for distributed training and inference. Its API is a lightweight wrapper on PyTorch, and its system innovations include ZeRO, ZeRO-Infinity, 3D-Parallelism, Ulysses Sequence Parallelism and DeepSpeed-MoE. DeepSpeed-Inference serves transformer-based PyTorch models with model parallelism and inference-customized kernels.
best_for: Large model training with limited GPU memory
not_ideal_for: Models outside PyTorch
key_features:
- ZeRO memory optimizations
- ZeRO-Offload and ZeRO-Infinity
- Mixed precision training
- Pipeline parallelism
- Mixture of experts with DeepSpeed-MoE
- DeepSpeed-Inference for transformer models
use_cases:
- Training large models
- Memory-efficient distributed training
- Large model fine-tuning
pros:
- Enabled on a PyTorch model with a few lines of code changes
- Integrated with Hugging Face Transformers and Accelerate
cons:
- Async I/O and GDS are not supported on Windows
language: Python
languages_supported:
- Python
maintained_by: DeepSpeed Team
license_spdx: Apache-2.0
github_url: https://github.com/deepspeedai/DeepSpeed
docs_url: https://www.deepspeed.ai/getting-started/
website_url: https://www.deepspeed.ai/
backing:
  type: foundation
  orgs:
  - LF AI & Data
alternatives:
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
  source: https://github.com/deepspeedai/DeepSpeed
aliases:
- microsoft/DeepSpeed
tags:
- distributed-training
- optimization
- large-models
- zero
updated: '2026-11-21'
sources:
- url: https://github.com/deepspeedai/DeepSpeed
  title: GitHub repository
- url: https://www.deepspeed.ai/getting-started/
  title: Documentation
- url: https://www.deepspeed.ai/training/
  title: Documentation — Training overview and features
- url: https://www.deepspeed.ai/inference/
  title: Documentation — Inference overview and features
- url: https://github.com/deepspeedai/DeepSpeed/blob/master/GOVERNANCE.md
  title: DeepSpeed governance charter
- url: https://pypi.org/project/deepspeed/
  title: deepspeed — PyPI
---

## Overview

DeepSpeed is a deep learning optimization library for distributed training and inference. Its API is a lightweight wrapper on PyTorch, and its system innovations include ZeRO, ZeRO-Infinity, 3D-Parallelism, Ulysses Sequence Parallelism and DeepSpeed-MoE. DeepSpeed-Inference serves transformer-based PyTorch models with model parallelism and inference-customized kernels.
