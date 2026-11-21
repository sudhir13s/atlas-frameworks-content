---
id: framework/optuna
type: framework
slug: optuna
schema_version: 1.1
title: Optuna
kind: framework
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: A hyperparameter optimization framework.
description: Optuna is an automatic hyperparameter optimization software framework designed for machine learning. Its define-by-run API lets users construct search spaces dynamically with Python conditionals and loops, and it provides sampling algorithms, pruning of unpromising trials, parallel studies and visualization.
best_for: Hyperparameter optimization for machine learning
key_features:
- Define-by-run API with dynamic search spaces
- TPE, CMA-ES, NSGA-II and Gaussian process samplers
- Pruning of unpromising trials
- Visualization functions and Optuna Dashboard
- Distributed optimization
- Integrations with PyTorch, TensorFlow, scikit-learn and other ML frameworks
use_cases:
- Hyperparameter tuning for ML models
- Multi-objective optimization
- Constrained optimization
pros:
- Search spaces written in plain Python
- Simple installation with few requirements
- Scales studies to many workers with little code change
language: Python
languages_supported:
- Python
maintained_by: Preferred Networks
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
maturity: production
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
updated: '2026-11-21'
sources:
- url: https://github.com/optuna/optuna
  title: GitHub repository
- url: https://optuna.readthedocs.io/
  title: Documentation
- url: https://optuna.readthedocs.io/en/stable/reference/samplers/index.html
  title: optuna.samplers
- url: https://optuna.readthedocs.io/en/stable/reference/integration.html
  title: optuna.integration
- url: https://pypi.org/project/optuna/
  title: optuna — PyPI
---

## Overview

Optuna is an automatic hyperparameter optimization software framework designed for machine learning. Its define-by-run API lets users construct search spaces dynamically with Python conditionals and loops, and it provides sampling algorithms, pruning of unpromising trials, parallel studies and visualization.
