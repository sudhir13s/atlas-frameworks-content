---
id: framework/neptune
type: framework
slug: neptune
schema_version: 1.1
title: Neptune.ai
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: Metadata store for ML experiments — log, compare, share results
description: SaaS experiment tracking and model metadata store. Focuses on flexibility — tracks any metadata type. Good for teams needing structured experiment comparison and model lineage.
best_for: Teams wanting flexible experiment metadata tracking
not_ideal_for: Teams needing self-hosted or air-gapped solutions
key_features:
- Flexible metadata logging
- Experiment comparison dashboards
- Model registry
- Integration with 25+ frameworks
- Team collaboration
use_cases:
- ML experiment tracking
- Model metadata management
- Team ML collaboration
pros:
- Very flexible metadata structure
- Good comparison and filtering tools
- Clean API
cons:
- SaaS only (no self-hosting for free)
- Smaller community than MLflow/W&B
language: Python
languages_supported:
- Python
- R
maintained_by: Neptune Labs
first_release: '2019-01-01'
license_note: 'Proprietary (client: Apache-2.0)'
github_url: https://github.com/neptune-ai/neptune-client
docs_url: https://docs.neptune.ai/
website_url: https://neptune.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: small
maturity: production
signal_strength: low
backing:
  type: corporate
  orgs:
  - Neptune Labs
  funding_or_parent: Seed funding from European VCs
alternatives:
- framework/wandb
- framework/mlflow
- framework/comet-ml
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
- framework/optuna
registry_signals:
  github_stars: 500
  downloads_monthly: 300000
  latest_version: '2.2'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/neptune-ai/neptune-client
aliases:
- neptune-ai/neptune-client
tags:
- mlops
- experiment-tracking
- metadata
updated: '2026-11-19'
sources:
- url: https://github.com/neptune-ai/neptune-client
  title: GitHub repository
- url: https://docs.neptune.ai/
  title: Documentation
---

## Overview

SaaS experiment tracking and model metadata store. Focuses on flexibility — tracks any metadata type. Good for teams needing structured experiment comparison and model lineage.
