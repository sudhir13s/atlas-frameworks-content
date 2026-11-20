---
id: framework/jax
type: framework
slug: jax
schema_version: 1.1
title: JAX
kind: library
category: framework-category/training
subcategory: core-framework
tagline: 'Composable transformations of NumPy programs: differentiate, vectorize, JIT, parallelize'
description: Google's functional numerical computing library that combines NumPy's API with automatic differentiation and XLA compilation. Designed for high-performance ML research with composable function transformations (grad, jit, vmap, pmap). Powers cutting-edge research at Google DeepMind.
best_for: Research labs needing maximum performance and mathematical elegance, TPU users
not_ideal_for: Teams new to ML, rapid prototyping, projects needing large third-party ecosystem
key_features:
- Composable function transformations (grad, jit, vmap, pmap)
- XLA compilation for accelerators
- NumPy-compatible API
- Automatic vectorization (vmap)
- Multi-device parallelism (pmap/pjit)
- Functional programming paradigm
- Reproducible PRNG system
use_cases:
- Cutting-edge ML research
- Large-scale distributed training
- Scientific computing
- TPU-optimized workloads
- Custom neural network architectures
pros:
- Best performance on TPUs
- Elegant composable transformations
- Excellent for custom research
- Growing ecosystem (Flax, Optax, Orbax)
- Pure functional approach eliminates side-effect bugs
cons:
- Steep learning curve — functional paradigm is different
- Smaller community than PyTorch
- Debugging JIT-compiled code is challenging
- Ecosystem still maturing compared to PyTorch
language: Python
languages_supported:
- Python
- C++
maintained_by: Google DeepMind
first_release: '2018-12-01'
license_spdx: Apache-2.0
github_url: https://github.com/jax-ml/jax
docs_url: https://jax.readthedocs.io/
website_url: https://github.com/jax-ml/jax
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
learning_curve: high
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google DeepMind
alternatives:
- framework/pytorch
- framework/tensorflow
ecosystem_connections:
- framework/flax
registry_signals:
  github_stars: 36656
  downloads_monthly: 12994367
  latest_version: 0.12.1
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-20'
  source: https://github.com/jax-ml/jax
aliases:
- jax-ml/jax
tags:
- deep-learning
- research
- tpu
- functional
- scientific-computing
updated: '2026-11-20'
sources:
- url: https://github.com/jax-ml/jax
  title: GitHub repository
- url: https://jax.readthedocs.io/
  title: Documentation
---

## Overview

Google's functional numerical computing library that combines NumPy's API with automatic differentiation and XLA compilation. Designed for high-performance ML research with composable function transformations (grad, jit, vmap, pmap). Powers cutting-edge research at Google DeepMind.
