---
id: framework/ray-tune
type: framework
slug: ray-tune
schema_version: 1.1
title: Ray Tune
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Scalable hyperparameter tuning on Ray — any framework, any scale
description: Scalable hyperparameter tuning library in the Ray ecosystem. Supports multiple search algorithms (Bayesian, Population-Based Training, HyperBand) and integrates with all major ML frameworks. Scales from laptop to cluster.
best_for: Large-scale distributed hyperparameter tuning, teams using Ray
not_ideal_for: Simple single-machine tuning (use Optuna)
key_features:
- Multiple search algorithms (BO, PBT, HyperBand)
- Distributed tuning across clusters
- Integration with Optuna, HyperOpt, Ax
- Population-Based Training
- Fault tolerance
- TensorBoard integration
use_cases:
- Large-scale hyperparameter tuning
- Population-based training
- Distributed ML experiments
pros:
- Scales to large clusters
- Multiple search algorithm backends
- Good fault tolerance
cons:
- Ray cluster overhead
- More complex than Optuna for simple tasks
- Configuration can be verbose
language: Python
languages_supported:
- Python
maintained_by: Anyscale
first_release: '2018-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/tune/
website_url: https://www.ray.io/ray-tune
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
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
updated: '2026-11-20'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/tune/
  title: Documentation
---

## Overview

Scalable hyperparameter tuning library in the Ray ecosystem. Supports multiple search algorithms (Bayesian, Population-Based Training, HyperBand) and integrates with all major ML frameworks. Scales from laptop to cluster.
