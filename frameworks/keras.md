---
id: framework/keras
type: framework
slug: keras
schema_version: 1.1
title: Keras
kind: framework
category: framework-category/training
subcategory: high-level-api
tagline: Deep learning for humans — simple, consistent, high-level API
description: High-level neural network API that now supports multiple backends (TensorFlow, JAX, PyTorch). Keras 3 is backend-agnostic, letting users write models once and run on any framework. Known for the fastest path from idea to working model.
best_for: Rapid prototyping, education, teams wanting backend portability
not_ideal_for: Highly custom architectures requiring low-level control
key_features:
- Multi-backend support (TF, JAX, PyTorch)
- Sequential, Functional, and Subclassing APIs
- Pre-built layers and model zoo
- Built-in training loops with callbacks
- Automatic mixed precision
- Model serialization and export
use_cases:
- Rapid prototyping
- Teaching and learning deep learning
- Standard architectures (CNNs, RNNs, Transformers)
- Transfer learning
- Backend-agnostic model development
pros:
- Simplest API in deep learning
- Excellent documentation and tutorials
- Backend-agnostic in Keras 3
- Large community and ecosystem
- Great for beginners and production alike
cons:
- Less flexibility for highly custom research
- Debugging can be opaque when backend abstractions leak
- Some advanced features require dropping to backend-specific code
language: Python
languages_supported:
- Python
maintained_by: Google (Francois Chollet)
first_release: '2015-03-27'
license_spdx: Apache-2.0
github_url: https://github.com/keras-team/keras
docs_url: https://keras.io/api/
website_url: https://keras.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: true
  google_tpu: true
learning_curve: low
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google (created by Francois Chollet)
ecosystem_connections:
- framework/tensorflow
- framework/jax
- framework/pytorch
- framework/keras-tuner
registry_signals:
  github_stars: 64442
  downloads_monthly: 12107636
  latest_version: 3.15.1
  latest_release_date: '2026-07-29'
  observed_at: '2026-11-20'
  source: https://github.com/keras-team/keras
aliases:
- keras-team/keras
tags:
- deep-learning
- high-level
- beginner-friendly
- multi-backend
updated: '2026-11-20'
sources:
- url: https://github.com/keras-team/keras
  title: GitHub repository
- url: https://keras.io/api/
  title: Documentation
---

## Overview

High-level neural network API that now supports multiple backends (TensorFlow, JAX, PyTorch). Keras 3 is backend-agnostic, letting users write models once and run on any framework. Known for the fastest path from idea to working model.
