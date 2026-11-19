---
id: framework/scikit-learn
type: framework
slug: scikit-learn
schema_version: 1.1
title: scikit-learn
kind: library
category: framework-category/training
subcategory: classical-ml
tagline: Machine learning in Python — simple and efficient tools for data analysis
description: The foundational library for classical machine learning in Python. Provides classification, regression, clustering, dimensionality reduction, and model selection algorithms. Not for deep learning — for everything else in ML.
best_for: Classical ML, data preprocessing, education, quick prototyping
not_ideal_for: Deep learning, large-scale data, GPU-accelerated training
key_features:
- Classification, regression, clustering algorithms
- Dimensionality reduction (PCA, t-SNE, UMAP)
- Model selection and evaluation
- Data preprocessing and feature engineering
- Pipeline API for chaining transforms
- Cross-validation and grid search
use_cases:
- Classical ML tasks (tabular data)
- Data preprocessing for deep learning
- ML education
- Quick baselines and prototyping
pros:
- Most comprehensive classical ML library
- Excellent documentation and tutorials
- Consistent API across all algorithms
- Industry standard
cons:
- No deep learning support
- CPU-only (no GPU acceleration)
- Not for large-scale data (use Spark MLlib or Dask)
language: Python
languages_supported:
- Python
maintained_by: scikit-learn community (INRIA funded)
first_release: '2007-06-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/scikit-learn/scikit-learn
docs_url: https://scikit-learn.org/stable/
website_url: https://scikit-learn.org/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: true
  google_tpu: false
learning_curve: low
community_size: massive
maturity: production
signal_strength: high
backing:
  type: foundation
  orgs:
  - INRIA Foundation
  - :probabl.
  funding_or_parent: Originated at INRIA; scikit-learn consortium funded by Microsoft, Nvidia, Hugging Face, Quansight, Dataiku, AXA, BNP Paribas, Chanel, Fujitsu; spin-off :probabl. founded 2024
registry_signals:
  github_stars: 60500
  downloads_monthly: 30000000
  latest_version: '1.6'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/scikit-learn/scikit-learn
aliases:
- scikit-learn/scikit-learn
tags:
- classical-ml
- tabular
- education
- preprocessing
updated: '2026-11-19'
sources:
- url: https://github.com/scikit-learn/scikit-learn
  title: GitHub repository
- url: https://scikit-learn.org/stable/
  title: Documentation
---

## Overview

The foundational library for classical machine learning in Python. Provides classification, regression, clustering, dimensionality reduction, and model selection algorithms. Not for deep learning — for everything else in ML.
