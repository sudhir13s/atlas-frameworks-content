---
id: framework/stable-baselines3
type: framework
slug: stable-baselines3
schema_version: 1.1
title: Stable Baselines3
kind: library
category: framework-category/reinforcement-learning
subcategory: algorithm-library
tagline: PyTorch version of Stable Baselines, reliable implementations of reinforcement learning algorithms.
description: Stable Baselines3 (SB3) is a set of reliable implementations of reinforcement learning algorithms in PyTorch and the next major version of Stable Baselines. It implements algorithms including PPO, A2C, SAC, TD3, DDPG, DQN and HER behind a common interface. Development now focuses on bug fixes and maintenance, and newer algorithms are added in the separate SB3 Contrib repository.
best_for: RL baselines, Replicating and comparing RL methods
not_ideal_for: Users without prior reinforcement learning knowledge
key_features:
- PPO, A2C, SAC, TD3, DDPG, DQN, HER implementations
- Gymnasium environment support
- Custom environments and policies
- Callback system for custom training
- Model saving and loading
- TensorBoard and Weights & Biases integration
- Model sharing on the Hugging Face Hub
use_cases:
- RL research and experimentation
- Baselines for comparing new RL methods
- Training agents on Gymnasium and Atari environments
pros:
- Performance of each algorithm tested and reported
- Common sklearn-like interface across algorithms
- Type hints and high test coverage
cons:
- Development limited to bug fixes and maintenance
- Recurrent policies only in SB3 Contrib
language: Python
languages_supported:
- Python
maintained_by: DLR-RM (German Aerospace Center, Institute of Robotics and Mechatronics)
license_spdx: MIT
github_url: https://github.com/DLR-RM/stable-baselines3
docs_url: https://stable-baselines3.readthedocs.io/
website_url: https://stable-baselines3.readthedocs.io/
maturity: production
alternatives:
- framework/rllib
- framework/cleanrl
ecosystem_connections:
- framework/gymnasium
- framework/pytorch
- framework/wandb
registry_signals:
  github_stars: 14038
  downloads_monthly: 794567
  latest_version: 2.9.2
  latest_release_date: '2026-10-26'
  observed_at: '2026-11-20'
  source: https://github.com/DLR-RM/stable-baselines3
aliases:
- DLR-RM/stable-baselines3
tags:
- reinforcement-learning
- algorithms
- pytorch
- research
updated: '2026-11-21'
sources:
- url: https://github.com/DLR-RM/stable-baselines3
  title: GitHub repository
- url: https://stable-baselines3.readthedocs.io/
  title: Documentation
- url: https://stable-baselines3.readthedocs.io/en/master/guide/integrations.html
  title: Integrations
- url: https://stable-baselines3.readthedocs.io/en/master/guide/install.html
  title: Installation
- url: https://pypi.org/project/stable-baselines3/
  title: stable-baselines3 — PyPI
- url: https://github.com/DLR-RM
  title: DLR-RM on GitHub
---

## Overview

Stable Baselines3 (SB3) is a set of reliable implementations of reinforcement learning algorithms in PyTorch and the next major version of Stable Baselines. It implements algorithms including PPO, A2C, SAC, TD3, DDPG, DQN and HER behind a common interface. Development now focuses on bug fixes and maintenance, and newer algorithms are added in the separate SB3 Contrib repository.
