---
id: framework/dask
type: framework
slug: dask
schema_version: 1.1
title: Dask
kind: library
category: framework-category/data
subcategory: distributed-computing
tagline: Parallel and distributed computing in Python — scale pandas, numpy, scikit-learn
description: Parallel computing library that scales Python analytics. Provides familiar APIs (DataFrame, Array) that mirror pandas and NumPy but execute in parallel across cores or clusters. Good for data too large for memory.
best_for: Python teams processing data too large for memory
not_ideal_for: Data that fits in memory (use pandas/polars), deep learning
key_features:
- Parallel pandas-like DataFrames
- Parallel NumPy-like arrays
- Task graph scheduling
- Distributed computing on clusters
- Dask-ML for scalable ML
- Dashboard for monitoring
use_cases:
- Processing datasets larger than memory
- Parallelizing pandas workflows
- Distributed data preprocessing for ML
pros:
- Familiar pandas/numpy API
- Scales from laptop to cluster
- Good for data preprocessing pipelines
cons:
- Not a full pandas replacement — some operations differ
- Overhead for small datasets
- Debugging distributed tasks is hard
language: Python
languages_supported:
- Python
maintained_by: Dask community / Coiled
first_release: '2015-01-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/dask/dask
docs_url: https://docs.dask.org/
website_url: https://www.dask.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: large
maturity: production
signal_strength: medium
backing:
  type: community
  orgs:
  - Coiled
  funding_or_parent: Community-driven; commercial support from Coiled (Series A $21M led by Bessemer 2022)
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
updated: '2026-11-20'
sources:
- url: https://github.com/dask/dask
  title: GitHub repository
- url: https://docs.dask.org/
  title: Documentation
---

## Overview

Parallel computing library that scales Python analytics. Provides familiar APIs (DataFrame, Array) that mirror pandas and NumPy but execute in parallel across cores or clusters. Good for data too large for memory.
