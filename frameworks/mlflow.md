---
id: framework/mlflow
type: framework
slug: mlflow
schema_version: 1.1
title: MLflow
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: Open-source platform for the ML lifecycle — tracking, packaging, deployment
description: The most widely adopted open-source MLOps platform. Provides experiment tracking, model registry, model packaging (MLmodel format), and deployment. Originally from Databricks, now an Apache project. Supports any ML library.
best_for: Teams wanting open-source experiment tracking and model management
not_ideal_for: Teams wanting polished SaaS experience (use W&B), very small projects
key_features:
- Experiment tracking (metrics, params, artifacts)
- Model registry with versioning and staging
- MLmodel packaging format
- Deployment to multiple targets
- LLM evaluation and tracking
- Integration with 30+ ML frameworks
use_cases:
- ML experiment tracking
- Model versioning and registry
- ML pipeline reproducibility
- Model deployment
pros:
- Most widely adopted open-source MLOps tool
- Framework-agnostic
- Self-hostable
- Strong Databricks integration
- LLM-specific features added
cons:
- UI is functional but basic
- Self-hosted backend can be complex at scale
- Artifact storage requires separate setup
language: Python
languages_supported:
- Python
- R
- Java
- REST API
maintained_by: Databricks / Apache Foundation
first_release: '2018-06-01'
license_spdx: Apache-2.0
github_url: https://github.com/mlflow/mlflow
docs_url: https://mlflow.org/docs/latest/
website_url: https://mlflow.org/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Databricks
  - Linux Foundation
  funding_or_parent: Created at Databricks; donated to Linux Foundation AI & Data in 2020
alternatives:
- framework/wandb
- framework/neptune
- framework/clearml
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 19500
  downloads_monthly: 8000000
  latest_version: '2.20'
  latest_release_date: '2025-02-15'
  observed_at: '2026-06-15'
  source: https://github.com/mlflow/mlflow
aliases:
- mlflow/mlflow
tags:
- mlops
- experiment-tracking
- model-registry
- deployment
updated: '2026-11-19'
sources:
- url: https://github.com/mlflow/mlflow
  title: GitHub repository
- url: https://mlflow.org/docs/latest/
  title: Documentation
---

## Overview

The most widely adopted open-source MLOps platform. Provides experiment tracking, model registry, model packaging (MLmodel format), and deployment. Originally from Databricks, now an Apache project. Supports any ML library.
