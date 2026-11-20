---
id: framework/bentoml
type: framework
slug: bentoml
schema_version: 1.1
title: BentoML
kind: framework
category: framework-category/llm-serving
subcategory: model-serving
tagline: Build, ship, and scale AI applications with Python
description: Python-first framework for building production ML serving applications. Packages models and serving logic into 'Bentos' that can be deployed as containers. Developer-friendly with good abstractions for common serving patterns.
best_for: Python teams wanting flexible, developer-friendly model serving
not_ideal_for: Maximum raw throughput on NVIDIA GPUs (use Triton)
key_features:
- Python-native model serving
- Bento packaging format
- Adaptive batching
- Multi-model composition
- Docker and Kubernetes deployment
- Built-in API documentation
use_cases:
- Custom ML API endpoints
- Multi-model serving pipelines
- Containerized ML deployment
pros:
- Python-first, developer-friendly
- Flexible serving logic
- Good packaging and deployment story
cons:
- Less performant than Triton for raw throughput
- Smaller community
- BentoCloud adds vendor lock-in
language: Python
languages_supported:
- Python
maintained_by: BentoML Inc.
first_release: '2019-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/bentoml/BentoML
docs_url: https://docs.bentoml.com/
website_url: https://www.bentoml.com/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - BentoML Inc
  funding_or_parent: Seed funding from DCM Ventures and others
alternatives:
- framework/ray-serve
- framework/triton-inference-server
- framework/seldon-core
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 8943
  downloads_monthly: 190534
  latest_version: 1.4.40
  latest_release_date: '2026-10-23'
  observed_at: '2026-11-20'
  source: https://github.com/bentoml/BentoML
aliases:
- bentoml/BentoML
tags:
- serving
- python
- deployment
- containerization
updated: '2026-11-20'
sources:
- url: https://github.com/bentoml/BentoML
  title: GitHub repository
- url: https://docs.bentoml.com/
  title: Documentation
---

## Overview

Python-first framework for building production ML serving applications. Packages models and serving logic into 'Bentos' that can be deployed as containers. Developer-friendly with good abstractions for common serving patterns.
