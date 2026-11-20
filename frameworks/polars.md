---
id: framework/polars
type: framework
slug: polars
schema_version: 1.1
title: Polars
kind: library
category: framework-category/data
subcategory: dataframe
tagline: Lightning-fast DataFrame library implemented in Rust
description: High-performance DataFrame library written in Rust with a Python API. Significantly faster than pandas for most operations. Uses Apache Arrow columnar format, lazy evaluation, and automatic query optimization.
best_for: High-performance data processing, teams willing to learn a new API
not_ideal_for: Teams heavily invested in pandas ecosystem, rapid prototyping by pandas experts
key_features:
- Rust-powered performance (10-100x faster than pandas)
- Lazy evaluation with query optimization
- Apache Arrow columnar format
- Streaming for out-of-memory datasets
- SQL interface
- Expression-based API
use_cases:
- High-performance data processing
- ML data preprocessing
- ETL pipelines
- Data analysis replacing pandas
pros:
- Dramatically faster than pandas
- Memory efficient
- Elegant expression API
- Growing rapidly
cons:
- API differs from pandas — learning curve
- Ecosystem still growing (fewer integrations)
- Some edge cases less polished than pandas
language: Rust
languages_supported:
- Python
- Rust
- Node.js
maintained_by: Polars Inc. (Ritchie Vink)
first_release: '2020-05-01'
license_spdx: MIT
github_url: https://github.com/pola-rs/polars
docs_url: https://docs.pola.rs/
website_url: https://www.pola.rs/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Polars Inc
  funding_or_parent: Seed $4M led by Bain Capital Ventures (2023); created by Ritchie Vink
alternatives:
- framework/dask
registry_signals:
  github_stars: 40394
  downloads_monthly: 69107592
  latest_version: 2.1.0
  latest_release_date: '2026-10-25'
  observed_at: '2026-11-20'
  source: https://github.com/pola-rs/polars
aliases:
- pola-rs/polars
tags:
- data-processing
- high-performance
- rust
- dataframe
updated: '2026-11-20'
sources:
- url: https://github.com/pola-rs/polars
  title: GitHub repository
- url: https://docs.pola.rs/
  title: Documentation
---

## Overview

High-performance DataFrame library written in Rust with a Python API. Significantly faster than pandas for most operations. Uses Apache Arrow columnar format, lazy evaluation, and automatic query optimization.
