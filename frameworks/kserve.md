---
id: framework/kserve
type: framework
slug: kserve
schema_version: 1.1
title: KServe
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: Standardized serverless ML inference on Kubernetes
description: Kubernetes-native serverless ML inference platform (formerly KFServing). Part of Kubeflow ecosystem. Provides standardized inference protocol, autoscaling, canary rollouts, and multi-framework support.
best_for: Kubernetes teams wanting serverless ML inference with autoscaling
not_ideal_for: Teams without Kubernetes expertise, latency-sensitive applications
key_features:
- Serverless autoscaling (Knative)
- Standardized V2 inference protocol
- Multi-framework support
- Canary rollouts
- Inference graph for pipelines
- GPU sharing
use_cases:
- Kubernetes ML serving with autoscaling
- Standardized inference APIs
- Serverless ML endpoints
pros:
- Serverless autoscaling including scale-to-zero
- Standardized inference protocol
- CNCF backed
cons:
- Requires Kubernetes + Knative/Istio stack
- Complex infrastructure requirements
- Slower cold starts due to serverless
language: Go
languages_supported:
- Python
- Go
maintained_by: CNCF / Kubeflow
first_release: '2019-06-01'
license_spdx: Apache-2.0
github_url: https://github.com/kserve/kserve
docs_url: https://kserve.github.io/kserve/
website_url: https://kserve.github.io/kserve/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: foundation
  orgs:
  - CNCF
  - Kubeflow
  funding_or_parent: CNCF incubating project (spun out of KFServing)
alternatives:
- framework/seldon-core
- framework/triton-inference-server
- framework/bentoml
registry_signals:
  github_stars: 6252
  downloads_monthly: 86581
  latest_version: 0.21.0
  latest_release_date: '2026-09-25'
  observed_at: '2026-11-20'
  source: https://github.com/kserve/kserve
aliases:
- kserve/kserve
tags:
- serving
- kubernetes
- serverless
- autoscaling
updated: '2026-11-20'
sources:
- url: https://github.com/kserve/kserve
  title: GitHub repository
- url: https://kserve.github.io/kserve/
  title: Documentation
---

## Overview

Kubernetes-native serverless ML inference platform (formerly KFServing). Part of Kubeflow ecosystem. Provides standardized inference protocol, autoscaling, canary rollouts, and multi-framework support.
