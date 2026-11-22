---
id: framework/hyperopt
type: framework
slug: hyperopt
schema_version: 1.1
title: Hyperopt
kind: library
category: framework-category/automl
subcategory: hyperparameter-tuning
tagline: Distributed Asynchronous Hyperparameter Optimization in Python.
description: Python library for serial and parallel optimization over awkward search spaces, which may include real-valued, discrete and conditional dimensions. It implements Random Search, Tree of Parzen Estimators (TPE) and Adaptive TPE. All algorithms can be parallelized with Apache Spark or MongoDB.
best_for: Hyperparameter optimization over conditional search spaces, Parallel hyperparameter search on Spark or MongoDB
not_ideal_for: Gaussian-process Bayesian optimization (not implemented)
key_features:
- Random search
- Tree of Parzen Estimators (TPE)
- Adaptive TPE
- Real-valued, discrete and conditional search spaces
- Parallel search on Apache Spark (SparkTrials)
- Parallel search with MongoDB (MongoTrials)
use_cases:
- Hyperparameter optimization
- Distributed hyperparameter search on Spark
pros:
- Supports conditional search spaces
- Parallelization through Spark or MongoDB
cons:
- Bayesian optimization based on Gaussian processes or regression trees is not implemented
- Documentation is partly still hosted on the GitHub wiki
language: Python
languages_supported:
- Python
maintained_by: Hyperopt project (hyperopt GitHub organization)
license_spdx: BSD-3-Clause
github_url: https://github.com/hyperopt/hyperopt
docs_url: http://hyperopt.github.io/hyperopt/
website_url: http://hyperopt.github.io/hyperopt/
maturity: experimental
backing:
  type: community
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
updated: '2026-11-21'
sources:
- url: https://github.com/hyperopt/hyperopt
  title: GitHub repository
- url: http://hyperopt.github.io/hyperopt/
  title: Documentation
- url: https://pypi.org/project/hyperopt/
  title: hyperopt — PyPI
---

## Overview

Python library for serial and parallel optimization over awkward search spaces, which may include real-valued, discrete and conditional dimensions. It implements Random Search, Tree of Parzen Estimators (TPE) and Adaptive TPE. All algorithms can be parallelized with Apache Spark or MongoDB.
