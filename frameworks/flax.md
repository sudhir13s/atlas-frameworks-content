---
id: framework/flax
type: framework
slug: flax
schema_version: 1.1
title: Flax
kind: library
category: framework-category/training
subcategory: high-level-api
tagline: A neural network library for JAX designed for flexibility
description: Google DeepMind's neural network library built on JAX. Provides the nn.Module abstraction and training utilities while maintaining JAX's functional purity. The recommended high-level API for JAX-based ML research.
best_for: JAX-based research projects, TPU training
not_ideal_for: Teams unfamiliar with functional programming, rapid prototyping
key_features:
- Functional nn.Module with explicit state
- NNX API for more Pythonic development
- Linen API for pure-functional style
- Serialization and checkpointing
- Tight JAX integration
- Pre-built layers and attention mechanisms
use_cases:
- ML research on JAX
- Large language model training
- TPU-optimized research
- Custom architecture development
pros:
- Clean functional design
- Official JAX neural network library
- Growing adoption in research
- NNX API reduces boilerplate
cons:
- Smaller ecosystem than PyTorch nn
- Learning curve for functional paradigm
- Fewer pre-built models than torchvision/timm
language: Python
languages_supported:
- Python
maintained_by: Google DeepMind
first_release: '2020-03-01'
license_spdx: Apache-2.0
github_url: https://github.com/google/flax
docs_url: https://flax.readthedocs.io/
website_url: https://flax.readthedocs.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
learning_curve: high
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google DeepMind
ecosystem_connections:
- framework/jax
registry_signals:
  github_stars: 7368
  downloads_monthly: 2752480
  latest_version: 0.12.12
  latest_release_date: '2026-10-27'
  observed_at: '2026-11-20'
  source: https://github.com/google/flax
aliases:
- google/flax
tags:
- deep-learning
- jax
- research
- functional
updated: '2026-11-20'
sources:
- url: https://github.com/google/flax
  title: GitHub repository
- url: https://flax.readthedocs.io/
  title: Documentation
---

## Overview

Google DeepMind's neural network library built on JAX. Provides the nn.Module abstraction and training utilities while maintaining JAX's functional purity. The recommended high-level API for JAX-based ML research.
