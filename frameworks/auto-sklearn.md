---
id: framework/auto-sklearn
type: framework
slug: auto-sklearn
schema_version: 3.0
title: auto-sklearn
status: curated
kind: library
category: framework-category/automl
subcategory: automl-framework
tagline: Automated Machine Learning with scikit-learn.
description: auto-sklearn is an automated machine learning toolkit and a drop-in replacement for a scikit-learn estimator. It takes algorithm selection and hyperparameter tuning off the user, using Bayesian optimization, meta-learning and ensemble construction.
best_for: Automating algorithm selection and hyperparameter tuning for scikit-learn models
not_ideal_for: Windows machines, macOS (support not confirmed by the docs)
key_features:
- Automatic algorithm selection
- Automatic hyperparameter tuning
- Bayesian optimization
- Meta-learning
- Ensemble construction
- Drop-in replacement for a scikit-learn estimator
use_cases:
- Automated classification with scikit-learn estimators
pros:
- Removes manual algorithm selection and hyperparameter tuning
- Same estimator interface as scikit-learn
cons:
- Requires Linux; the docs state it cannot run on Windows
language: Python
languages_supported:
- Python
maintained_by: AutoML-Freiburg-Hannover
license_spdx: BSD-3-Clause
github_url: https://github.com/automl/auto-sklearn
docs_url: https://automl.github.io/auto-sklearn/
website_url: https://automl.github.io/auto-sklearn/
alternatives:
- framework/flaml
registry_signals:
  github_stars: 8147
  downloads_monthly: 100000
  latest_version: '0.15'
  latest_release_date: '2023-06-01'
  observed_at: '2026-11-20'
  source: https://github.com/automl/auto-sklearn
aliases:
- automl/auto-sklearn
- Auto-sklearn
tags:
- automl
- sklearn
- tabular
updated: '2026-11-21'
sources:
- url: https://github.com/automl/auto-sklearn
  title: GitHub repository
- url: https://automl.github.io/auto-sklearn/
  title: Documentation
- url: https://automl.github.io/auto-sklearn/master/installation.html
  title: Installation
- url: https://github.com/automl
  title: AutoML-Freiburg-Hannover on GitHub
- url: https://pypi.org/project/auto-sklearn/
  title: auto-sklearn — PyPI
---


