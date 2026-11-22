---
id: framework/clearml
type: framework
slug: clearml
schema_version: 1.1
title: ClearML
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: Experiment management, data management, pipelines, orchestration, scheduling and serving in one MLOps/LLMOps solution.
description: ClearML is an ML/DL development and production suite with modules for experiment management, MLOps and LLMOps orchestration and pipelines, data management and version control on object storage, model serving, and reports. The ClearML Server stores experiment, model and workflow data and is available as a hosted service or as open source to deploy yourself.
best_for: Running experiment tracking and orchestration and data management in one platform
key_features:
- Automatic experiment logging from two lines of code
- Orchestration agent for Kubernetes and cloud and bare-metal jobs
- Automation pipelines built from existing experiments
- Dataset management and versioning on object storage
- Model serving backed by NVIDIA Triton
- Hyperparameter optimization
- Resource monitoring of CPU and GPU utilization
- Reports and orchestration dashboard
use_cases:
- Experiment tracking and comparison
- Self-hosted experiment tracking
- ML pipeline orchestration
- Dataset versioning on S3, Google Cloud Storage, Azure or NAS
pros:
- Open-source server for self-hosting or a hosted service
- Logging added with two lines of code
- Integrations with PyTorch, TensorFlow, Keras, XGBoost, scikit-learn and other frameworks
language: Python
languages_supported:
- Python
maintained_by: ClearML
license_spdx: Apache-2.0
github_url: https://github.com/clearml/clearml
docs_url: https://clear.ml/docs/
website_url: https://clear.ml/
maturity: production
backing:
  type: corporate
  orgs:
  - ClearML
alternatives:
- framework/mlflow
- framework/wandb
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 6943
  downloads_monthly: 500000
  latest_version: 2.2.0
  latest_release_date: '2026-11-03'
  observed_at: '2026-11-20'
  source: https://github.com/allegroai/clearml
aliases:
- allegroai/clearml
- clearml/clearml
tags:
- mlops
- experiment-tracking
- orchestration
- self-hosted
updated: '2026-11-21'
sources:
- url: https://github.com/clearml/clearml
  title: GitHub repository
- url: https://clear.ml/docs/
  title: Documentation
- url: https://github.com/clearml
  title: ClearML on GitHub
- url: https://pypi.org/project/clearml/
  title: clearml — PyPI
---

## Overview

ClearML is an ML/DL development and production suite with modules for experiment management, MLOps and LLMOps orchestration and pipelines, data management and version control on object storage, model serving, and reports. The ClearML Server stores experiment, model and workflow data and is available as a hosted service or as open source to deploy yourself.
