---
id: framework/seldon-core
type: framework
slug: seldon-core
schema_version: 1.1
title: Seldon Core
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: Deploy, monitor, and explain ML models on Kubernetes
description: Kubernetes-native ML serving platform with advanced features for model monitoring, A/B testing, canary deployments, and explainability. Enterprise-focused with strong governance features.
best_for: Enterprise Kubernetes environments needing ML governance
not_ideal_for: Small teams, non-Kubernetes environments
key_features:
- Kubernetes-native deployment
- A/B testing and canary rollouts
- Model monitoring and drift detection
- Model explainability
- Multi-framework support
- Inference graph pipelines
use_cases:
- Enterprise ML on Kubernetes
- Regulated ML deployments
- Model monitoring and governance
pros:
- Strong governance and monitoring
- Kubernetes-native
- A/B testing built-in
cons:
- Complex Kubernetes setup required
- License changed to BSL for v2
- Steep learning curve
language: Go
languages_supported:
- Python
- Go
maintained_by: Seldon Technologies
first_release: '2018-01-01'
license_note: 'Apache-2.0 (v2: BSL)'
github_url: https://github.com/SeldonIO/seldon-core
docs_url: https://docs.seldon.io/
website_url: https://www.seldon.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: small-medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Seldon Technologies
  funding_or_parent: Series B $20M led by Bright Pixel (2022)
alternatives:
- framework/kserve
- framework/bentoml
- framework/ray-serve
registry_signals:
  github_stars: 4300
  downloads_monthly: 100000
  latest_version: '2.9'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/SeldonIO/seldon-core
aliases:
- SeldonIO/seldon-core
tags:
- serving
- kubernetes
- enterprise
- monitoring
- governance
updated: '2026-11-19'
sources:
- url: https://github.com/SeldonIO/seldon-core
  title: GitHub repository
- url: https://docs.seldon.io/
  title: Documentation
---

## Overview

Kubernetes-native ML serving platform with advanced features for model monitoring, A/B testing, canary deployments, and explainability. Enterprise-focused with strong governance features.
