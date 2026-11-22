---
id: framework/dask
type: framework
slug: dask
schema_version: 1.1
title: Dask
kind: library
category: framework-category/data
subcategory: distributed-computing
tagline: Parallel computing with task scheduling.
description: Dask is a Python library for parallel and distributed computing. Dask DataFrames and Dask Arrays parallelize pandas and NumPy, Dask Bags process Python objects in parallel, and Dask Futures parallelize arbitrary Python code. It runs on a single machine, including larger-than-memory data, or on distributed clusters.
best_for: Data larger than available RAM, Parallelizing pandas and NumPy code
not_ideal_for: Data that fits in RAM
key_features:
- Parallel pandas-like DataFrames
- Parallel NumPy-like arrays
- Task graph scheduling
- Distributed computing on clusters
- Dashboard for monitoring
use_cases:
- Processing datasets larger than memory
- Parallelizing pandas workflows
- Hyperparameter optimization and batch prediction for ML
pros:
- Uses the pandas and NumPy APIs
- Runs on a single machine or a distributed cluster
cons:
- For data that fits in RAM the docs recommend pandas as faster and easier
language: Python
languages_supported:
- Python
maintained_by: Dask core developers
license_spdx: BSD-3-Clause
github_url: https://github.com/dask/dask
docs_url: https://docs.dask.org/
website_url: https://www.dask.org/
maturity: production
backing:
  type: foundation
  orgs:
  - NumFOCUS
alternatives:
- framework/polars
registry_signals:
  github_stars: 13959
  downloads_monthly: 31722821
  latest_version: 2026.8.0
  latest_release_date: '2026-08-24'
  observed_at: '2026-11-20'
  source: https://github.com/dask/dask
aliases:
- dask/dask
tags:
- data-processing
- distributed
- parallel
- pandas-like
updated: '2026-11-21'
sources:
- url: https://github.com/dask/dask
  title: GitHub repository
- url: https://docs.dask.org/
  title: Documentation
- url: https://docs.dask.org/en/stable/gpu.html
  title: Documentation — GPUs
- url: https://docs.dask.org/en/stable/ml.html
  title: Documentation — Machine Learning
- url: https://docs.dask.org/en/stable/dashboard.html
  title: Documentation — Dashboard
- url: https://docs.dask.org/en/stable/dataframe-best-practices.html
  title: Documentation — DataFrame best practices
- url: https://dask.org/powered-by/
  title: Dask — Powered By
- url: https://pypi.org/project/dask/
  title: dask — PyPI
---

## Overview

Dask is a Python library for parallel and distributed computing. Dask DataFrames and Dask Arrays parallelize pandas and NumPy, Dask Bags process Python objects in parallel, and Dask Futures parallelize arbitrary Python code. It runs on a single machine, including larger-than-memory data, or on distributed clusters.
