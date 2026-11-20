---
id: framework/ray-serve
type: framework
slug: ray-serve
schema_version: 1.1
title: Ray Serve
kind: library
category: framework-category/llm-serving
subcategory: model-serving
tagline: Scalable model serving built on Ray — compose ML models and business logic
description: Scalable model serving framework built on Ray. Excels at composing multiple models and business logic into serving pipelines. Native Python, supports any ML framework, and scales from laptop to cluster.
best_for: Complex multi-model serving with business logic, teams already using Ray
not_ideal_for: Simple single-model serving, teams not using Ray
key_features:
- Python-native model composition
- Multi-model serving graphs
- Dynamic request batching
- Horizontal autoscaling
- Built on Ray distributed runtime
- Framework-agnostic
use_cases:
- Multi-model serving pipelines
- LLM serving with business logic
- Scalable inference APIs
pros:
- Flexible Python-native composition
- Scales from laptop to cluster
- Good for complex serving graphs
- Integration with Ray ecosystem
cons:
- Ray cluster overhead for simple serving
- Less optimized than Triton for raw throughput
- Debugging distributed serving is hard
language: Python
languages_supported:
- Python
maintained_by: Anyscale
first_release: '2020-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/serve/
website_url: https://www.ray.io/ray-serve
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Anyscale
  funding_or_parent: Anyscale Series C $99M led by Andreessen Horowitz (2021); total raised >$250M
alternatives:
- framework/bentoml
- framework/triton-inference-server
ecosystem_connections:
- framework/ray-train
- framework/vllm
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 44348
  downloads_monthly: 15757870
  latest_version: 2.60.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/ray-project/ray
tags:
- serving
- distributed
- scalable
- multi-model
updated: '2026-11-20'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/serve/
  title: Documentation
---

## Overview

Scalable model serving framework built on Ray. Excels at composing multiple models and business logic into serving pipelines. Native Python, supports any ML framework, and scales from laptop to cluster.
