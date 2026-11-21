---
id: framework/keras-tuner
type: framework
slug: keras-tuner
schema_version: 1.1
title: KerasTuner
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: A Hyperparameter Tuning Library for Keras.
description: Hyperparameter optimization framework for Keras models. Search spaces are configured with a define-by-run syntax inside the function that builds the model. It includes Bayesian Optimization, Hyperband and Random Search and is designed to be extended with new search algorithms.
best_for: Hyperparameter tuning of Keras models
key_features:
- Define-by-run search spaces
- Bayesian Optimization, Hyperband and Random Search tuners
- Extensible with new search algorithms
- Distributed tuning with a chief-worker model
- TensorBoard visualization of the tuning process
use_cases:
- Tuning Keras neural networks
- Distributed hyperparameter search across GPUs and machines
pros:
- Scales from a single local process to many parallel workers without code changes
- Tuning runs can be inspected in TensorBoard
cons:
- Requires TensorFlow to be installed
language: Python
languages_supported:
- Python
maintained_by: Keras team (keras-team)
license_spdx: Apache-2.0
github_url: https://github.com/keras-team/keras-tuner
docs_url: https://keras.io/keras_tuner/
website_url: https://keras.io/keras_tuner/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
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
- Keras Tuner
tags:
- automl
- hyperparameter-tuning
- keras
updated: '2026-11-21'
sources:
- url: https://github.com/keras-team/keras-tuner
  title: GitHub repository
- url: https://keras.io/keras_tuner/
  title: Documentation
- url: https://raw.githubusercontent.com/keras-team/keras-io/master/guides/keras_tuner/distributed_tuning.py
  title: Distributed hyperparameter tuning guide
- url: https://raw.githubusercontent.com/keras-team/keras-io/master/guides/keras_tuner/visualize_tuning.py
  title: Visualize the hyperparameter tuning process guide
- url: https://pypi.org/project/keras-tuner/
  title: keras-tuner — PyPI
---

## Overview

Hyperparameter optimization framework for Keras models. Search spaces are configured with a define-by-run syntax inside the function that builds the model. It includes Bayesian Optimization, Hyperband and Random Search and is designed to be extended with new search algorithms.
