---
id: framework/flaml
type: framework
slug: flaml
schema_version: 1.1
title: FLAML
kind: library
category: framework-category/automl
subcategory: automl-framework
tagline: A fast library for AutoML and tuning.
description: FLAML is a lightweight Python library for efficient automation of machine learning and AI operations. It performs model selection and hyperparameter optimization under resource constraints and finds quality models for tasks like classification and regression with low computational resources. Its tuning tool also handles generic functions, such as inference hyperparameters for foundation models.
best_for: AutoML for classification and regression under resource constraints, Hyperparameter tuning of custom functions
key_features:
- Cost-frugal hyperparameter optimization
- Automatic model selection
- LLM application optimization
- Zero-shot AutoML
- Low computational overhead
use_cases:
- AutoML for classification and regression
- Tuning inference hyperparameters for foundation models
- Resource-constrained tuning
pros:
- Finds quality models with low computational resources
- Scikit-learn style estimator API
- Handles large search spaces with heterogeneous evaluation costs
language: Python
languages_supported:
- Python
maintained_by: Microsoft
license_spdx: MIT
github_url: https://github.com/microsoft/FLAML
docs_url: https://microsoft.github.io/FLAML/
website_url: https://microsoft.github.io/FLAML/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: corporate
  orgs:
  - Microsoft
alternatives:
- framework/optuna
- framework/auto-sklearn
registry_signals:
  github_stars: 4422
  downloads_monthly: 366027
  latest_version: 2.8.0
  latest_release_date: '2026-11-06'
  observed_at: '2026-11-20'
  source: https://github.com/microsoft/FLAML
aliases:
- microsoft/FLAML
tags:
- automl
- efficient
- cost-frugal
- microsoft
updated: '2026-11-21'
sources:
- url: https://github.com/microsoft/FLAML
  title: GitHub repository
- url: https://microsoft.github.io/FLAML/
  title: Documentation
- url: https://pypi.org/project/FLAML/
  title: FLAML — PyPI
---

## Overview

FLAML is a lightweight Python library for efficient automation of machine learning and AI operations. It performs model selection and hyperparameter optimization under resource constraints and finds quality models for tasks like classification and regression with low computational resources. Its tuning tool also handles generic functions, such as inference hyperparameters for foundation models.
