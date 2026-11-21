---
id: framework/cleanrl
type: framework
slug: cleanrl
schema_version: 1.1
title: CleanRL
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: Single-file implementation of deep reinforcement learning algorithms with research-friendly features (PPO, DQN, C51, DDPG, TD3, SAC, PPG).
description: CleanRL is a deep reinforcement learning library that provides single-file implementations with research-friendly features, putting every detail of an algorithm variant into one standalone file. It is not a modular library and is not meant to be imported. Its implementations are benchmarked and support TensorBoard logging, seeding for local reproducibility and experiment tracking with Weights and Biases.
best_for: Understanding every implementation detail of an RL algorithm variant, Prototyping features that modular RL libraries do not support
not_ideal_for: Use as an importable library (the docs state it is not meant to be imported)
key_features:
- Single-file algorithm implementations
- PPO, DQN, C51, SAC, DDPG, TD3, PPG, RND and Qdagger variants
- PyTorch implementations with JAX variants for several algorithms
- Benchmarked implementations
- TensorBoard logging
- Local reproducibility via seeding
- Gameplay video capture
- Experiment management with Weights and Biases
- Cloud integration with Docker and AWS
use_cases:
- Learning how RL algorithms are implemented
- Reproducible RL research
- Comparing tracked experiments through Open RL Benchmark
pros:
- No subclassing or modular abstractions to trace
- Benchmarked implementations with tracked experiments
cons:
- Not meant to be imported as a library
- Duplicates code across files by design
language: Python
languages_supported:
- Python
maintained_by: CleanRL contributors
license_spdx: MIT
github_url: https://github.com/vwxyzjn/cleanrl
docs_url: https://docs.cleanrl.dev/
website_url: https://docs.cleanrl.dev/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: community
alternatives:
- framework/stable-baselines3
- framework/rllib
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
- framework/wandb
registry_signals:
  github_stars: 10704
  downloads_monthly: 100000
  latest_version: '1.2'
  latest_release_date: '2024-06-01'
  observed_at: '2026-11-20'
  source: https://github.com/vwxyzjn/cleanrl
aliases:
- vwxyzjn/cleanrl
tags:
- reinforcement-learning
- education
- clean-code
- research
updated: '2026-11-21'
sources:
- url: https://github.com/vwxyzjn/cleanrl
  title: GitHub repository
- url: https://docs.cleanrl.dev/
  title: Documentation
- url: https://docs.cleanrl.dev/rl-algorithms/ppo/
  title: PPO documentation
- url: https://pypi.org/project/cleanrl/
  title: cleanrl — PyPI
---

## Overview

CleanRL is a deep reinforcement learning library that provides single-file implementations with research-friendly features, putting every detail of an algorithm variant into one standalone file. It is not a modular library and is not meant to be imported. Its implementations are benchmarked and support TensorBoard logging, seeding for local reproducibility and experiment tracking with Weights and Biases.
