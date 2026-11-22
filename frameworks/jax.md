---
id: framework/jax
type: framework
slug: jax
schema_version: 1.1
title: JAX
kind: library
category: framework-category/training
subcategory: core-framework
tagline: 'Composable transformations of Python+NumPy programs: differentiate, vectorize, JIT to GPU/TPU, and more.'
description: Python library for accelerator-oriented array computation and program transformation, designed for high-performance numerical computing and large-scale machine learning. It automatically differentiates native Python and NumPy functions and uses XLA to compile programs for TPUs, GPUs and other accelerators. Its transformations, including grad, jit and vmap, compose arbitrarily.
best_for: High-performance numerical computing, Large-scale machine learning on GPUs and TPUs
not_ideal_for: GPU work on native Windows (NVIDIA and AMD GPUs are not supported there)
key_features:
- Composable function transformations (grad, jit, vmap)
- Forward- and reverse-mode automatic differentiation to any order
- XLA compilation for TPUs and GPUs
- NumPy-compatible API (jax.numpy)
- Compiler-based automatic parallelization across devices
- Explicit sharding and manual per-device programming with collectives
use_cases:
- Machine learning research
- Large-scale distributed training
- Numerical and scientific computing
- TPU workloads
pros:
- Transformations compose with each other and with Python control flow
- The same code runs on CPU, GPU and TPU backends
- Ecosystem libraries such as Flax, Optax and Orbax
cons:
- The README calls it a research project, not an official Google product, and warns of sharp edges
- Code under jax.jit is limited in the Python control flow it can use
language: Python
languages_supported:
- Python
maintained_by: JAX team (jax-ml)
license_spdx: Apache-2.0
github_url: https://github.com/jax-ml/jax
docs_url: https://docs.jax.dev/en/latest/
website_url: https://github.com/jax-ml/jax
alternatives:
- framework/pytorch
- framework/tensorflow
ecosystem_connections:
- framework/flax
registry_signals:
  github_stars: 36657
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
updated: '2026-11-21'
sources:
- url: https://github.com/jax-ml/jax
  title: GitHub repository
- url: https://docs.jax.dev/en/latest/
  title: Documentation
- url: https://pypi.org/project/jax/
  title: jax — PyPI
---

## Overview

Python library for accelerator-oriented array computation and program transformation, designed for high-performance numerical computing and large-scale machine learning. It automatically differentiates native Python and NumPy functions and uses XLA to compile programs for TPUs, GPUs and other accelerators. Its transformations, including grad, jit and vmap, compose arbitrarily.
