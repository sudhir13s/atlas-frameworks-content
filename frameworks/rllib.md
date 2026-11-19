---
id: framework/rllib
type: framework
slug: rllib
schema_version: 1.1
title: RLlib (Ray)
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: Scalable reinforcement learning on Ray
description: Scalable RL library in the Ray ecosystem. Supports multi-agent RL, distributed training, and a wide range of algorithms. Designed for production-scale RL workloads.
best_for: Multi-agent RL, large-scale distributed RL
not_ideal_for: Simple single-agent RL (use SB3), quick prototyping
key_features:
- Multi-agent reinforcement learning
- Distributed training on Ray
- Wide algorithm support
- Custom environment support
- Offline RL
- Model-based RL
use_cases:
- Multi-agent RL
- Distributed RL training
- Production RL systems
pros:
- Best for multi-agent RL
- Scales to large clusters
- Production-grade
cons:
- Complex setup
- Ray overhead for simple tasks
- API changes frequently
language: Python
languages_supported:
- Python
maintained_by: Anyscale
first_release: '2018-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/rllib/
website_url: https://www.ray.io/rllib
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: large
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Anyscale
alternatives:
- framework/stable-baselines3
- framework/cleanrl
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 35000
  downloads_monthly: 3000000
  latest_version: '2.43'
  latest_release_date: '2025-02-15'
  observed_at: '2026-06-15'
  source: https://github.com/ray-project/ray
tags:
- reinforcement-learning
- multi-agent
- distributed
- ray
updated: '2026-11-19'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/rllib/
  title: Documentation
---

## Overview

Scalable RL library in the Ray ecosystem. Supports multi-agent RL, distributed training, and a wide range of algorithms. Designed for production-scale RL workloads.
