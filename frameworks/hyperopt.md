---
id: framework/hyperopt
type: framework
slug: hyperopt
schema_version: 1.1
title: Hyperopt
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Distributed hyperparameter optimization using TPE and random search
description: One of the earliest Bayesian hyperparameter optimization libraries. Uses Tree-structured Parzen Estimators (TPE). Still widely used but Optuna has largely superseded it for new projects.
best_for: Legacy projects using Hyperopt, Spark-based HPO
not_ideal_for: New projects — use Optuna instead
key_features:
- TPE sampler
- Random search
- MongoDB-based distributed optimization
- Spark integration (SparkTrials)
use_cases:
- Hyperparameter optimization
- Distributed HPO on Spark
pros:
- Established and well-understood
- Spark integration
cons:
- Largely superseded by Optuna
- Less active development
- API is less ergonomic
language: Python
languages_supported:
- Python
maintained_by: James Bergstra + community
first_release: '2013-01-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/hyperopt/hyperopt
docs_url: http://hyperopt.github.io/hyperopt/
website_url: http://hyperopt.github.io/hyperopt/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: low
backing:
  type: community
  funding_or_parent: Created by James Bergstra; community-maintained, limited active development
alternatives:
- framework/optuna
- framework/ray-tune
registry_signals:
  github_stars: 7600
  downloads_monthly: 1720725
  latest_version: 0.3.0
  latest_release_date: '2026-07-24'
  observed_at: '2026-11-20'
  source: https://github.com/hyperopt/hyperopt
aliases:
- hyperopt/hyperopt
tags:
- automl
- hyperparameter-tuning
- bayesian
updated: '2026-11-20'
sources:
- url: https://github.com/hyperopt/hyperopt
  title: GitHub repository
- url: http://hyperopt.github.io/hyperopt/
  title: Documentation
---

## Overview

One of the earliest Bayesian hyperparameter optimization libraries. Uses Tree-structured Parzen Estimators (TPE). Still widely used but Optuna has largely superseded it for new projects.
