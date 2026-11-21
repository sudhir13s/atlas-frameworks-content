---
id: framework/flax
type: framework
slug: flax
schema_version: 1.1
title: Flax
kind: library
category: framework-category/training
subcategory: high-level-api
tagline: Flax is a neural network library for JAX that is designed for flexibility.
description: Flax is a neural network library and ecosystem for JAX designed for flexibility, developed in close collaboration with the JAX team. Its current API, Flax NNX, adds first class support for Python reference semantics so models are regular Python objects, and it evolved from the Flax Linen API, which is not being deprecated. It ships a neural network API, utilities for replicated training, serialization, checkpointing and metrics, and educational examples.
best_for: Neural network research in JAX
key_features:
- NNX API with Python reference semantics
- Linen API for existing codebases
- Serialization and checkpointing
- Integration with regular JAX code
- Pre-built layers and attention mechanisms
use_cases:
- ML research on JAX
- Custom architecture development
pros:
- Developed in close collaboration with the JAX team
- Models are written as regular Python objects in Flax NNX
language: Python
languages_supported:
- Python
maintained_by: Google DeepMind
license_spdx: Apache-2.0
github_url: https://github.com/google/flax
docs_url: https://flax.readthedocs.io/
website_url: https://flax.readthedocs.io/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
maturity: experimental
backing:
  type: corporate
  orgs:
  - Google DeepMind
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
updated: '2026-11-21'
sources:
- url: https://github.com/google/flax
  title: GitHub repository
- url: https://flax.readthedocs.io/
  title: Documentation
- url: https://pypi.org/project/flax/
  title: flax — PyPI
---

## Overview

Flax is a neural network library and ecosystem for JAX designed for flexibility, developed in close collaboration with the JAX team. Its current API, Flax NNX, adds first class support for Python reference semantics so models are regular Python objects, and it evolved from the Flax Linen API, which is not being deprecated. It ships a neural network API, utilities for replicated training, serialization, checkpointing and metrics, and educational examples.
