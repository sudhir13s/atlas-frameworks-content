---
id: framework/ray-train
type: framework
slug: ray-train
schema_version: 1.1
title: Ray Train
kind: library
category: framework-category/distributed-training
subcategory: training-framework
tagline: Scalable distributed ML training on Ray
description: Ray's distributed training library that provides a unified API for distributed training across PyTorch, TensorFlow, and Horovod. Handles cluster management, fault tolerance, and checkpointing automatically.
best_for: Teams using Ray for the full ML lifecycle
not_ideal_for: Teams not using Ray, maximum training throughput
key_features:
- Unified distributed training API
- Automatic fault tolerance
- Checkpoint management
- Integration with Ray ecosystem
- Multi-framework support
- Elastic scaling
use_cases:
- Distributed training on Ray clusters
- Fault-tolerant training
- Integration with Ray Tune and Ray Serve
pros:
- Good fault tolerance and checkpointing
- Unified API across frameworks
- Part of the Ray ecosystem
cons:
- Requires Ray cluster overhead
- Less optimized than DeepSpeed for very large models
- Another abstraction layer
language: Python
languages_supported:
- Python
maintained_by: Anyscale
first_release: '2021-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/train/train.html
website_url: https://www.ray.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
learning_curve: medium
community_size: large
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Anyscale
  funding_or_parent: Anyscale (Ray originated at UC Berkeley RISELab)
alternatives:
- framework/deepspeed
ecosystem_connections:
- framework/ray-tune
- framework/ray-serve
- framework/pytorch
- framework/deepspeed
registry_signals:
  github_stars: 35000
  downloads_monthly: 3000000
  latest_version: '2.43'
  latest_release_date: '2025-02-15'
  observed_at: '2026-06-15'
  source: https://github.com/ray-project/ray
tags:
- distributed-training
- ray
- fault-tolerance
- scalable
updated: '2026-11-19'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/train/
  title: Documentation
---

## Overview

Ray's distributed training library that provides a unified API for distributed training across PyTorch, TensorFlow, and Horovod. Handles cluster management, fault tolerance, and checkpointing automatically.
