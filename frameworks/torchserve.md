---
id: framework/torchserve
type: framework
slug: torchserve
schema_version: 1.1
title: TorchServe
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: Serve PyTorch models at scale in production
description: Official model serving solution for PyTorch. Provides model packaging, multi-model serving, A/B testing, logging, and metrics. Developed jointly by AWS and Meta.
best_for: Production serving of PyTorch models, especially on AWS
not_ideal_for: Multi-framework serving, highly custom serving logic
key_features:
- MAR packaging format for PyTorch models
- Multi-model serving
- A/B testing support
- Metrics and logging
- gRPC and REST APIs
- Dynamic batching
use_cases:
- Production PyTorch model serving
- Multi-model endpoints
- A/B testing ML models
pros:
- Official PyTorch serving solution
- Good for AWS deployment
- Dynamic batching
cons:
- Java-based server adds complexity
- Less flexible than BentoML for custom logic
- Limited compared to Triton for multi-framework
language: Java
languages_supported:
- Python
- Java
maintained_by: PyTorch Foundation (AWS + Meta)
first_release: '2020-04-01'
license_spdx: Apache-2.0
github_url: https://github.com/pytorch/serve
docs_url: https://pytorch.org/serve/
website_url: https://pytorch.org/serve/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Meta
  - AWS
  - PyTorch Foundation
  funding_or_parent: Joint Meta + AWS project under PyTorch Foundation
alternatives:
- framework/triton-inference-server
- framework/bentoml
- framework/ray-serve
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 4300
  downloads_monthly: 300000
  latest_version: '0.12'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/pytorch/serve
aliases:
- pytorch/serve
tags:
- serving
- pytorch
- production
- deployment
updated: '2026-11-19'
sources:
- url: https://github.com/pytorch/serve
  title: GitHub repository
- url: https://pytorch.org/serve/
  title: Documentation
---

## Overview

Official model serving solution for PyTorch. Provides model packaging, multi-model serving, A/B testing, logging, and metrics. Developed jointly by AWS and Meta.
