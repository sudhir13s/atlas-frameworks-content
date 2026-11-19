---
id: framework/stable-baselines3
type: framework
slug: stable-baselines3
schema_version: 1.1
title: Stable Baselines3
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: Reliable implementations of RL algorithms in PyTorch
description: Reliable PyTorch implementations of popular RL algorithms (PPO, A2C, SAC, TD3, DQN). Clean code, well-documented, and thoroughly tested. The standard starting point for RL research and applications.
best_for: Standard RL algorithms, research, and education
not_ideal_for: Multi-agent RL, very large-scale distributed RL
key_features:
- PPO, A2C, SAC, TD3, DQN, HER implementations
- Gymnasium (OpenAI Gym) compatible
- Clean, tested, documented code
- Callback system for custom training
- Model saving and loading
- W&B and TensorBoard integration
use_cases:
- RL research and experimentation
- Robotics control
- Game AI
- Optimization problems
pros:
- Most reliable RL implementations
- Excellent documentation
- Clean codebase for learning
- Active maintenance
cons:
- Limited to single-agent RL
- Not the fastest for large-scale training
- No multi-agent support
language: Python
languages_supported:
- Python
maintained_by: DLR-RM / Antonin Raffin
first_release: '2020-06-01'
license_spdx: MIT
github_url: https://github.com/DLR-RM/stable-baselines3
docs_url: https://stable-baselines3.readthedocs.io/
website_url: https://stable-baselines3.readthedocs.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: foundation
  orgs:
  - DLR-RM (German Aerospace Center)
  funding_or_parent: Maintained by DLR Institute of Robotics and Mechatronics (Antonin Raffin)
alternatives:
- framework/rllib
- framework/cleanrl
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
- framework/wandb
registry_signals:
  github_stars: 9500
  downloads_monthly: 800000
  latest_version: '2.4'
  latest_release_date: '2024-12-01'
  observed_at: '2026-06-15'
  source: https://github.com/DLR-RM/stable-baselines3
aliases:
- DLR-RM/stable-baselines3
tags:
- reinforcement-learning
- algorithms
- pytorch
- research
updated: '2026-11-19'
sources:
- url: https://github.com/DLR-RM/stable-baselines3
  title: GitHub repository
- url: https://stable-baselines3.readthedocs.io/
  title: Documentation
---

## Overview

Reliable PyTorch implementations of popular RL algorithms (PPO, A2C, SAC, TD3, DQN). Clean code, well-documented, and thoroughly tested. The standard starting point for RL research and applications.
