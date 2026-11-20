---
id: framework/dvc
type: framework
slug: dvc
schema_version: 1.1
title: DVC (Data Version Control)
kind: tool
category: framework-category/mlops
subcategory: data-versioning
tagline: Git for data and ML pipelines — version control for datasets and experiments
description: Version control system for ML projects that extends Git to handle large files, datasets, and ML pipelines. Stores data in remote storage while keeping lightweight pointers in Git. Enables reproducible ML experiments.
best_for: Teams wanting Git-native data versioning and reproducible pipelines
not_ideal_for: Teams needing rich experiment visualization (use W&B), very large-scale data lakes
key_features:
- Git-like data versioning
- ML pipeline definition (dvc.yaml)
- Remote storage backends (S3, GCS, Azure, SSH)
- Experiment tracking and comparison
- Data and model registry
use_cases:
- Dataset versioning alongside code
- Reproducible ML pipelines
- Data and model sharing across teams
pros:
- Git-native workflow — familiar for developers
- Storage-agnostic
- Open source and self-hostable
- Good for data-heavy ML projects
cons:
- Learning curve for non-Git users
- Pipeline definition less flexible than Airflow/Prefect
- Experiment tracking less polished than W&B
language: Python
languages_supported:
- Python
maintained_by: Iterative.ai
first_release: '2017-05-01'
license_spdx: Apache-2.0
github_url: https://github.com/iterative/dvc
docs_url: https://dvc.org/doc
website_url: https://dvc.org/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Iterative.ai
  funding_or_parent: Series A $20M led by 468 Capital (2022)
alternatives:
- framework/mlflow
registry_signals:
  github_stars: 15985
  downloads_monthly: 2000000
  latest_version: 3.67.1
  latest_release_date: '2026-03-31'
  observed_at: '2026-11-20'
  source: https://github.com/iterative/dvc
aliases:
- iterative/dvc
tags:
- mlops
- data-versioning
- pipelines
- reproducibility
updated: '2026-11-20'
sources:
- url: https://github.com/iterative/dvc
  title: GitHub repository
- url: https://dvc.org/doc
  title: Documentation
---

## Overview

Version control system for ML projects that extends Git to handle large files, datasets, and ML pipelines. Stores data in remote storage while keeping lightweight pointers in Git. Enables reproducible ML experiments.
