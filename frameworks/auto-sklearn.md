---
id: framework/auto-sklearn
type: framework
slug: auto-sklearn
schema_version: 1.1
title: Auto-sklearn
kind: library
category: framework-category/automl
subcategory: automl-framework
tagline: Automated machine learning for scikit-learn — finds the best pipeline
description: AutoML system built on scikit-learn. Automatically selects the best ML algorithm, preprocessor, and hyperparameters for tabular data. Uses Bayesian optimization and meta-learning.
best_for: Quick automated baselines for tabular ML tasks
not_ideal_for: Deep learning, very large datasets, production systems
key_features:
- Automatic algorithm selection
- Automatic hyperparameter tuning
- Meta-learning for warm-starting
- Ensemble construction
- scikit-learn compatible API
use_cases:
- Quick baseline models for tabular data
- Automated pipeline selection
- ML competition baselines
pros:
- Fully automated ML pipeline selection
- scikit-learn compatible
- Good for baselines
cons:
- Only for tabular/classic ML (no deep learning)
- Can be slow for large datasets
- Development has slowed
language: Python
languages_supported:
- Python
maintained_by: AutoML Freiburg
first_release: '2015-01-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/automl/auto-sklearn
docs_url: https://automl.github.io/auto-sklearn/
website_url: https://automl.github.io/auto-sklearn/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: small-medium
maturity: stable
signal_strength: low
backing:
  type: foundation
  orgs:
  - AutoML Freiburg-Hannover
  funding_or_parent: Academic research group (University of Freiburg)
alternatives:
- framework/flaml
registry_signals:
  github_stars: 7600
  downloads_monthly: 100000
  latest_version: '0.15'
  latest_release_date: '2023-06-01'
  observed_at: '2026-06-15'
  source: https://github.com/automl/auto-sklearn
aliases:
- automl/auto-sklearn
tags:
- automl
- sklearn
- tabular
updated: '2026-11-19'
sources:
- url: https://github.com/automl/auto-sklearn
  title: GitHub repository
- url: https://automl.github.io/auto-sklearn/
  title: Documentation
---

## Overview

AutoML system built on scikit-learn. Automatically selects the best ML algorithm, preprocessor, and hyperparameters for tabular data. Uses Bayesian optimization and meta-learning.
