---
id: framework/flaml
type: framework
slug: flaml
schema_version: 1.1
title: FLAML
kind: library
category: framework-category/automl
subcategory: automl-framework
tagline: Fast and lightweight AutoML — efficient hyperparameter optimization
description: Microsoft's fast AutoML library for efficient hyperparameter tuning and model selection. Significantly faster than alternatives while achieving competitive results. Also supports LLM application optimization.
best_for: Fast, cost-efficient AutoML for tabular data and LLM optimization
not_ideal_for: Deep learning HPO, very large search spaces
key_features:
- Cost-frugal hyperparameter optimization
- Automatic model selection
- LLM application optimization
- Zero-shot AutoML
- Low computational overhead
use_cases:
- Fast AutoML for tabular data
- LLM application optimization
- Resource-constrained tuning
pros:
- Very fast — much lower compute cost than alternatives
- Good for budget-constrained optimization
- LLM optimization support
cons:
- Smaller community
- Less mature ecosystem
language: Python
languages_supported:
- Python
maintained_by: Microsoft Research
first_release: '2020-12-01'
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
learning_curve: low
community_size: small
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Microsoft
  funding_or_parent: Microsoft Research
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
updated: '2026-11-20'
sources:
- url: https://github.com/microsoft/FLAML
  title: GitHub repository
- url: https://microsoft.github.io/FLAML/
  title: Documentation
---

## Overview

Microsoft's fast AutoML library for efficient hyperparameter tuning and model selection. Significantly faster than alternatives while achieving competitive results. Also supports LLM application optimization.
