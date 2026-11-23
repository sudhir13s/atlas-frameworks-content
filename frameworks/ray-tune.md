---
id: framework/ray-tune
type: framework
slug: ray-tune
schema_version: 3.0
title: Ray Tune
status: curated
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Tune is a Python library for experiment execution and hyperparameter tuning at any scale.
description: Ray Tune is a Python library for experiment execution and hyperparameter tuning, part of Ray. It runs algorithms such as Population Based Training and HyperBand/ASHA and integrates with hyperparameter optimization tools including Ax, BayesOpt, BOHB, Nevergrad and Optuna. It parallelizes tuning across multiple GPUs and multiple nodes.
best_for: Hyperparameter tuning, Experiment execution
key_features:
- Population Based Training and HyperBand/ASHA
- Parallel tuning across GPUs and nodes
- Integration with Optuna, HyperOpt, Ax
- Early stopping of trials
- Fault tolerance
- Logging to MLflow and TensorBoard
use_cases:
- Distributed hyperparameter tuning
- Population-based training
- Distributed ML experiments
pros:
- Parallelizes tuning across GPUs and nodes
- Plugs in external search libraries
- Built-in fault tolerance
language: Python
languages_supported:
- Python
maintained_by: The Ray Team
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/tune/
website_url: https://www.ray.io/ray-tune
backing:
  type: foundation
  orgs:
  - LF Projects
  - Anyscale
alternatives:
- framework/optuna
- framework/hyperopt
ecosystem_connections:
- framework/ray-train
- framework/ray-serve
- framework/optuna
- framework/pytorch
registry_signals:
  github_stars: 44348
  downloads_monthly: 15757870
  latest_version: 2.60.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/ray-project/ray
tags:
- automl
- hyperparameter-tuning
- distributed
- ray
updated: '2026-11-21'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/tune/
  title: Documentation
- url: https://docs.ray.io/en/latest/tune/index.html
  title: Ray Tune documentation
- url: https://docs.ray.io/en/latest/train/user-guides/hyperparameter-optimization.html
  title: Ray Train hyperparameter optimization
- url: https://docs.ray.io/en/latest/ray-governance/index.html
  title: Ray governance
- url: https://www.ray.io/
  title: Website
---


