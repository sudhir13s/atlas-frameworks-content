---
id: framework/feast
type: framework
slug: feast
schema_version: 1.1
title: Feast
kind: tool
category: framework-category/data
subcategory: feature-store
tagline: Open-source feature store for machine learning
description: Open-source feature store that manages the lifecycle of ML features. Provides a consistent API for serving features in both training and inference. Supports batch and real-time feature serving.
best_for: ML teams needing consistent feature serving across training and inference
not_ideal_for: Simple projects without feature reuse needs
key_features:
- Feature definitions as code
- Online and offline feature serving
- Point-in-time correct joins
- Feature registry
- Multiple storage backends
use_cases:
- Consistent feature serving for training and inference
- Feature reuse across ML models
- Real-time feature serving
pros:
- Open source and vendor-neutral
- Good for training-serving skew prevention
- Feature definitions as code
cons:
- Setup complexity
- Smaller community than commercial alternatives
- Real-time feature serving needs additional infra
language: Python
languages_supported:
- Python
- Go
maintained_by: Tecton (originally Gojek + Google)
first_release: '2019-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/feast-dev/feast
docs_url: https://docs.feast.dev/
website_url: https://feast.dev/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Tecton
  funding_or_parent: Created at Gojek + Google; stewarded by Tecton (Series C $100M led by Kleiner Perkins 2022)
registry_signals:
  github_stars: 7362
  downloads_monthly: 285750
  latest_version: 0.68.0
  latest_release_date: '2026-11-10'
  observed_at: '2026-11-20'
  source: https://github.com/feast-dev/feast
aliases:
- feast-dev/feast
tags:
- data-processing
- feature-store
- ml-infrastructure
updated: '2026-11-20'
sources:
- url: https://github.com/feast-dev/feast
  title: GitHub repository
- url: https://docs.feast.dev/
  title: Documentation
---

## Overview

Open-source feature store that manages the lifecycle of ML features. Provides a consistent API for serving features in both training and inference. Supports batch and real-time feature serving.
