---
id: framework/wandb
type: framework
slug: wandb
schema_version: 1.1
title: Weights & Biases
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: The AI developer platform — experiment tracking, model evaluation, dataset management
description: Leading SaaS MLOps platform for experiment tracking, hyperparameter sweeps, artifact management, and collaborative ML. Known for its polished UI, real-time dashboards, and strong integration with PyTorch. Used by most top ML research labs.
best_for: Research teams and companies wanting the best experiment tracking UX
not_ideal_for: Air-gapped environments, teams with strict data residency requirements
key_features:
- Real-time experiment dashboards
- Hyperparameter sweep optimization
- Artifact versioning and lineage
- Model evaluation and comparison
- Team collaboration features
- LLM evaluation (Weave)
- Report sharing and publishing
use_cases:
- ML experiment tracking and comparison
- Hyperparameter optimization
- Team collaboration on ML projects
- Model evaluation and benchmarking
pros:
- Best-in-class UI and UX
- Excellent real-time visualization
- Strong community and research adoption
- Good free tier
cons:
- SaaS — data leaves your infrastructure (self-hosted option exists)
- Can be expensive at scale
- Vendor lock-in risk
language: Python
languages_supported:
- Python
- JavaScript
maintained_by: Weights & Biases Inc.
first_release: '2018-01-01'
license_note: MIT (client), Proprietary (server)
github_url: https://github.com/wandb/wandb
docs_url: https://docs.wandb.ai/
website_url: https://wandb.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Weights & Biases Inc
  funding_or_parent: Series C $135M led by Insight Partners (2021); acquired by CoreWeave announced 2025
alternatives:
- framework/mlflow
- framework/neptune
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
updated: '2026-11-20'
sources:
- url: https://github.com/wandb/wandb
  title: GitHub repository
- url: https://docs.wandb.ai/
  title: Documentation
---

## Overview

Leading SaaS MLOps platform for experiment tracking, hyperparameter sweeps, artifact management, and collaborative ML. Known for its polished UI, real-time dashboards, and strong integration with PyTorch. Used by most top ML research labs.
