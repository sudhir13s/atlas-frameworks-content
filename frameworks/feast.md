---
id: framework/feast
type: framework
slug: feast
schema_version: 1.1
title: Feast
kind: tool
category: framework-category/data
subcategory: feature-store
tagline: The Open Source Feature Store for AI/ML.
description: Feast is an open source feature store for machine learning. It makes features consistently available for training and serving by managing an offline store for historical data, a low-latency online store for real-time prediction and a feature server. It generates point-in-time correct feature sets and provides a single data access layer over existing data infrastructure.
best_for: ML teams needing consistent feature serving across training and inference, ML platform teams productionizing real-time models
not_ideal_for: General ETL or data orchestration, Dataset versioning and experiment management
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
- Works with existing data infrastructure through a single data access layer
- Point-in-time correct feature sets prevent data leakage
- Centralized catalog of feature definitions
cons:
- Not a database; online and offline data live in other systems
- Does not version datasets or manage train and test splits
- Does not pull from streaming sources or manage streaming pipelines
language: Python
languages_supported:
- Python
maintained_by: Feast community
license_spdx: Apache-2.0
github_url: https://github.com/feast-dev/feast
docs_url: https://docs.feast.dev/
website_url: https://feast.dev/
backing:
  type: community
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
updated: '2026-11-21'
sources:
- url: https://github.com/feast-dev/feast
  title: GitHub repository
- url: https://docs.feast.dev/
  title: Documentation
- url: https://pypi.org/project/feast/
  title: feast — PyPI
---

## Overview

Feast is an open source feature store for machine learning. It makes features consistently available for training and serving by managing an offline store for historical data, a low-latency online store for real-time prediction and a feature server. It generates point-in-time correct feature sets and provides a single data access layer over existing data infrastructure.
