---
id: framework/optuna
type: framework
slug: optuna
schema_version: 1.1
title: Optuna
kind: framework
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Automatic hyperparameter optimization framework
description: State-of-the-art hyperparameter optimization framework using Bayesian optimization (Tree-structured Parzen Estimators). Define-by-run API, pruning of unpromising trials, and visualization dashboards. The most popular open-source HPO tool.
best_for: Hyperparameter optimization for any ML framework
not_ideal_for: Neural architecture search, very large search spaces
key_features:
- Define-by-run API (flexible search space)
- TPE and CMA-ES samplers
- Early stopping (pruning) of bad trials
- Visualization dashboard
- Distributed optimization
- Integration with PyTorch, TF, sklearn
use_cases:
- Neural network hyperparameter tuning
- ML pipeline optimization
- Multi-objective optimization
pros:
- Most popular HPO tool
- Clean define-by-run API
- Good pruning algorithms
- Excellent visualizations
cons:
- Limited to hyperparameter optimization (not NAS)
- Bayesian optimization can be slow with many parameters
language: Python
languages_supported:
- Python
maintained_by: Preferred Networks
first_release: '2018-11-01'
license_spdx: MIT
github_url: https://github.com/optuna/optuna
docs_url: https://optuna.readthedocs.io/
website_url: https://optuna.org/
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
  type: corporate
  orgs:
  - Preferred Networks
alternatives:
- framework/ray-tune
- framework/hyperopt
- framework/keras-tuner
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 15070
  downloads_monthly: 14572648
  latest_version: 5.1.0
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-20'
  source: https://github.com/optuna/optuna
aliases:
- optuna/optuna
tags:
- automl
- hyperparameter-tuning
- optimization
- bayesian
updated: '2026-11-20'
sources:
- url: https://github.com/optuna/optuna
  title: GitHub repository
- url: https://optuna.readthedocs.io/
  title: Documentation
---

## Overview

State-of-the-art hyperparameter optimization framework using Bayesian optimization (Tree-structured Parzen Estimators). Define-by-run API, pruning of unpromising trials, and visualization dashboards. The most popular open-source HPO tool.
