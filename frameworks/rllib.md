---
id: framework/rllib
type: framework
slug: rllib
schema_version: 1.1
title: RLlib
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: RLlib is an open source library for reinforcement learning (RL).
description: RLlib is an open source reinforcement learning library built on Ray. It supports production-grade, scalable and fault-tolerant RL workloads with simple, unified APIs. It covers multi-agent training, learning from historic offline data and externally connected simulators.
best_for: Multi-agent RL, Offline RL, Distributed RL training
key_features:
- Multi-agent reinforcement learning
- Distributed training on Ray
- On-policy and off-policy algorithms
- Custom environment support
- Offline RL and behavior cloning
- Model-based RL
- Multi-GPU training
- External environment clients
use_cases:
- Multi-agent RL
- Distributed RL training
- Production RL systems
pros:
- Native multi-agent RL support
- Fault-tolerant sample collection
- Supports production-grade workloads
language: Python
languages_supported:
- Python
maintained_by: The Ray Team
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
maturity: production
backing:
  type: foundation
  orgs:
  - LF Projects
  - Anyscale
alternatives:
- framework/stable-baselines3
- framework/cleanrl
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
registry_signals:
  github_stars: 44348
  downloads_monthly: 15757870
  latest_version: 2.60.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/ray-project/ray
tags:
- reinforcement-learning
- multi-agent
- distributed
- ray
updated: '2026-11-21'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/rllib/
  title: Documentation
- url: https://docs.ray.io/en/latest/rllib/index.html
  title: RLlib documentation
- url: https://docs.ray.io/en/latest/ray-governance/index.html
  title: Ray governance
- url: https://www.ray.io/
  title: Website
aliases:
- RLlib (Ray)
---

## Overview

RLlib is an open source reinforcement learning library built on Ray. It supports production-grade, scalable and fault-tolerant RL workloads with simple, unified APIs. It covers multi-agent training, learning from historic offline data and externally connected simulators.
