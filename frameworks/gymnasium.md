---
id: framework/gymnasium
type: framework
slug: gymnasium
schema_version: 1.1
title: Gymnasium
kind: library
category: framework-category/reinforcement-learning
subcategory: environment
tagline: A standard API for single-agent reinforcement learning environments, with reference environments and related utilities (formerly Gym).
description: Open-source Python library for developing and comparing reinforcement learning algorithms. It provides a standard API between learning algorithms and environments and a set of reference environments compliant with that API. It is a maintained fork of OpenAI's Gym.
best_for: Defining reinforcement learning environments, Developing and comparing RL algorithms
key_features:
- Standard environment API built on reset and step
- Classic Control, Box2D and Toy Text environments
- Atari environments
- MuJoCo physics environments
- Environment wrappers and vectorized environments
- Versioned environments for reproducibility
use_cases:
- RL environment definition
- Comparing RL algorithms
- Custom RL environment creation
pros:
- Environments are strictly versioned for reproducibility
- Third-party environments built on the same API
language: Python
languages_supported:
- Python
maintained_by: Farama Foundation
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
maturity: production
backing:
  type: foundation
  orgs:
  - Farama Foundation
ecosystem_connections:
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
updated: '2026-11-21'
sources:
- url: https://github.com/Farama-Foundation/Gymnasium
  title: GitHub repository
- url: https://gymnasium.farama.org/
  title: Documentation
- url: https://pypi.org/project/gymnasium/
  title: gymnasium — PyPI
---

## Overview

Open-source Python library for developing and comparing reinforcement learning algorithms. It provides a standard API between learning algorithms and environments and a set of reference environments compliant with that API. It is a maintained fork of OpenAI's Gym.
