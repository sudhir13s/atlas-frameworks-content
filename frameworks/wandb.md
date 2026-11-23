---
id: framework/wandb
type: framework
slug: wandb
schema_version: 3.0
title: Weights & Biases
status: curated
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: Train and fine-tune models, and manage models from experimentation to production.
description: Weights & Biases tracks, visualizes and compares machine learning experiments, and W&B Weave traces and evaluates LLM applications alongside it. The wandb Python library and CLI log runs, metrics and hyperparameters to the platform, which also provides sweeps, artifacts, reports and automations. It is available as a managed cloud service or as a self-managed server on your own infrastructure.
best_for: ML experiment tracking, Tracing and evaluating LLM applications
key_features:
- Experiment tracking and visualization
- Hyperparameter sweeps
- Artifact versioning
- Reports
- Automations
- LLM tracing and evaluation with W&B Weave
- Managed cloud, dedicated cloud and self-managed deployment
use_cases:
- ML experiment tracking and comparison
- Hyperparameter optimization
- Dataset and model versioning
- LLM application evaluation
pros:
- Integrations with ML frameworks such as PyTorch, Keras and Hugging Face Transformers
- Self-managed deployment including air-gapped Kubernetes
cons:
- Some features require an Enterprise license
language: Python
languages_supported:
- Python
maintained_by: Weights & Biases
license_note: 'wandb Python client: MIT'
github_url: https://github.com/wandb/wandb
docs_url: https://docs.coreweave.com/products/wandb
website_url: https://wandb.ai/
maturity: production
backing:
  type: corporate
  orgs:
  - Weights & Biases
alternatives:
- framework/mlflow
- framework/comet-ml
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
- framework/hugging-face-transformers
- framework/keras
registry_signals:
  github_stars: 11332
  downloads_monthly: 20057702
  latest_version: 0.31.1
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/wandb/wandb
aliases:
- wandb/wandb
tags:
- mlops
- experiment-tracking
- visualization
- collaboration
updated: '2026-11-21'
sources:
- url: https://github.com/wandb/wandb
  title: GitHub repository
- url: https://docs.coreweave.com/products/wandb
  title: Documentation
- url: https://docs.coreweave.com/products/wandb/platform/hosting
  title: Deployment options overview
- url: https://docs.coreweave.com/products/wandb/platform/hosting/self-managed/on-premises-deployments/kubernetes-airgapped
  title: Deploy on air-gapped Kubernetes
- url: https://docs.coreweave.com/products/wandb/integrations
  title: Integrations overview
- url: https://docs.coreweave.com/products/wandb/integrations/pytorch
  title: PyTorch integration
- url: https://docs.coreweave.com/products/wandb/integrations/tensorflow
  title: TensorFlow integration
- url: https://pypi.org/project/wandb/
  title: wandb — PyPI
---


