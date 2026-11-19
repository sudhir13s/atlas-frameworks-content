---
id: framework/cleanrl
type: framework
slug: cleanrl
schema_version: 1.1
title: CleanRL
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: Single-file implementations of deep RL algorithms for educational clarity
description: Single-file, self-contained implementations of popular RL algorithms. Designed for understanding — each algorithm is one Python file with no abstraction layers. Excellent for learning RL implementation details.
best_for: Learning RL implementation details, reproducible research
not_ideal_for: Production RL, complex environments
key_features:
- Single-file algorithm implementations
- PPO, DQN, SAC, TD3, and more
- W&B integration for tracking
- Reproducible benchmarks
- Educational design
use_cases:
- Learning RL implementations
- Reproducible RL research
- Algorithm comparison
pros:
- Best for understanding RL code
- No hidden abstractions
- Good benchmarks and reproducibility
cons:
- Not designed for production use
- Limited algorithm variants
language: Python
languages_supported:
- Python
maintained_by: CleanRL team (Costa Huang)
first_release: '2020-07-01'
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
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: community
  funding_or_parent: Maintained by Costa Huang (Hugging Face) and community
alternatives:
- framework/stable-baselines3
- framework/rllib
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
- framework/wandb
registry_signals:
  github_stars: 5800
  downloads_monthly: 100000
  latest_version: '1.2'
  latest_release_date: '2024-06-01'
  observed_at: '2026-06-15'
  source: https://github.com/vwxyzjn/cleanrl
aliases:
- vwxyzjn/cleanrl
tags:
- reinforcement-learning
- education
- clean-code
- research
updated: '2026-11-19'
sources:
- url: https://github.com/vwxyzjn/cleanrl
  title: GitHub repository
- url: https://docs.cleanrl.dev/
  title: Documentation
---

## Overview

Single-file, self-contained implementations of popular RL algorithms. Designed for understanding — each algorithm is one Python file with no abstraction layers. Excellent for learning RL implementation details.
