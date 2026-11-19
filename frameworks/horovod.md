---
id: framework/horovod
type: framework
slug: horovod
schema_version: 1.1
title: Horovod
kind: framework
category: framework-category/distributed-training
subcategory: training-framework
tagline: Distributed training framework for TensorFlow, Keras, PyTorch, and MXNet
description: Uber's distributed training framework using ring-allreduce. Framework-agnostic, supporting TensorFlow, PyTorch, and MXNet. Enables distributed training with minimal code changes. Usage has declined with native framework support improving.
best_for: Legacy multi-framework distributed training setups
not_ideal_for: New projects — use PyTorch DDP/FSDP or DeepSpeed instead
key_features:
- Ring-allreduce distributed training
- Multi-framework support
- Minimal code changes required
- Elastic training
- Spark integration
use_cases:
- Multi-framework distributed training
- Spark-based ML pipelines
pros:
- Easy to add to existing code
- Multi-framework support
cons:
- Development has slowed significantly
- Native framework solutions (DDP, FSDP) have caught up
- Less relevant for modern LLM training
language: Python
languages_supported:
- Python
- C++
maintained_by: Linux Foundation AI (originally Uber)
first_release: '2017-12-01'
license_spdx: Apache-2.0
github_url: https://github.com/horovod/horovod
docs_url: https://horovod.readthedocs.io/
website_url: https://horovod.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: small
maturity: stable
signal_strength: low
backing:
  type: foundation
  orgs:
  - LF AI & Data Foundation
  funding_or_parent: Originated at Uber; donated to Linux Foundation AI in 2018
alternatives:
- framework/pytorch-fsdp
- framework/deepspeed
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 14200
  downloads_monthly: 200000
  latest_version: '0.28'
  latest_release_date: '2023-10-01'
  observed_at: '2026-06-15'
  source: https://github.com/horovod/horovod
aliases:
- horovod/horovod
tags:
- distributed-training
- multi-framework
- legacy
updated: '2026-11-19'
sources:
- url: https://github.com/horovod/horovod
  title: GitHub repository
- url: https://horovod.readthedocs.io/
  title: Documentation
---

## Overview

Uber's distributed training framework using ring-allreduce. Framework-agnostic, supporting TensorFlow, PyTorch, and MXNet. Enables distributed training with minimal code changes. Usage has declined with native framework support improving.
