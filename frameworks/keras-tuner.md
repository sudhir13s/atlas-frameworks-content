---
id: framework/keras-tuner
type: framework
slug: keras-tuner
schema_version: 1.1
title: Keras Tuner
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Hyperparameter tuning for Keras models
description: Google's hyperparameter tuning library specifically designed for Keras models. Simple API for defining search spaces within model building functions. Supports random search, Bayesian optimization, and Hyperband.
best_for: Keras users wanting simple hyperparameter tuning
not_ideal_for: Non-Keras frameworks, complex optimization needs
key_features:
- Tight Keras integration
- HyperBand, Bayesian, Random search
- Custom search spaces
- Oracle API for custom algorithms
use_cases:
- Tuning Keras neural networks
- Neural architecture search for Keras
pros:
- Simplest HPO for Keras users
- Good integration with TensorBoard
cons:
- Keras-only
- Less powerful than Optuna for general use
language: Python
languages_supported:
- Python
maintained_by: Google / Keras team
first_release: '2019-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/keras-team/keras-tuner
docs_url: https://keras.io/keras_tuner/
website_url: https://keras.io/keras_tuner/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
learning_curve: low
community_size: medium
maturity: stable
signal_strength: low
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google / Keras team
alternatives:
- framework/optuna
- framework/ray-tune
ecosystem_connections:
- framework/keras
- framework/tensorflow
registry_signals:
  github_stars: 2922
  downloads_monthly: 112252
  latest_version: 1.4.8
  latest_release_date: '2025-11-11'
  observed_at: '2026-11-20'
  source: https://github.com/keras-team/keras-tuner
aliases:
- keras-team/keras-tuner
tags:
- automl
- hyperparameter-tuning
- keras
updated: '2026-11-20'
sources:
- url: https://github.com/keras-team/keras-tuner
  title: GitHub repository
- url: https://keras.io/keras_tuner/
  title: Documentation
---

## Overview

Google's hyperparameter tuning library specifically designed for Keras models. Simple API for defining search spaces within model building functions. Supports random search, Bayesian optimization, and Hyperband.
