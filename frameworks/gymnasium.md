---
id: framework/gymnasium
type: framework
slug: gymnasium
schema_version: 1.1
title: Gymnasium
kind: library
category: framework-category/reinforcement-learning
subcategory: environment
tagline: Standard API for reinforcement learning environments
description: Maintained fork of OpenAI Gym. Provides the standard API for RL environments used by virtually all RL libraries. Includes classic control, Atari, MuJoCo, and box2d environments.
best_for: Defining RL environments, benchmarking RL algorithms
not_ideal_for: Complex simulation environments (use Unity ML-Agents, MuJoCo directly)
key_features:
- Standard RL environment API (reset, step, render)
- Classic control environments
- Atari game environments
- MuJoCo physics environments
- Environment wrappers and vectorization
use_cases:
- RL environment definition
- RL algorithm benchmarking
- Custom RL environment creation
pros:
- Industry standard API
- Used by all major RL libraries
- Good built-in environments
cons:
- Environments are simple — real-world RL needs custom envs
- Some legacy API complexity
language: Python
languages_supported:
- Python
maintained_by: Farama Foundation
first_release: '2022-10-01'
license_spdx: MIT
github_url: https://github.com/Farama-Foundation/Gymnasium
docs_url: https://gymnasium.farama.org/
website_url: https://gymnasium.farama.org/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: large
maturity: production
signal_strength: high
backing:
  type: foundation
  orgs:
  - Farama Foundation
  funding_or_parent: Nonprofit that took over OpenAI Gym maintenance in 2022
ecosystem_connections:
- framework/stable-baselines3
- framework/rllib
- framework/cleanrl
registry_signals:
  github_stars: 12842
  downloads_monthly: 4435816
  latest_version: 1.4.0
  latest_release_date: '2026-10-05'
  observed_at: '2026-11-20'
  source: https://github.com/Farama-Foundation/Gymnasium
aliases:
- Farama-Foundation/Gymnasium
tags:
- reinforcement-learning
- environment
- standard-api
updated: '2026-11-20'
sources:
- url: https://github.com/Farama-Foundation/Gymnasium
  title: GitHub repository
- url: https://gymnasium.farama.org/
  title: Documentation
---

## Overview

Maintained fork of OpenAI Gym. Provides the standard API for RL environments used by virtually all RL libraries. Includes classic control, Atari, MuJoCo, and box2d environments.
