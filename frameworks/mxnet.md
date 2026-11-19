---
id: framework/mxnet
type: framework
slug: mxnet
schema_version: 1.1
title: Apache MXNet
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: Scalable deep learning framework with multi-language support
description: Apache Foundation deep learning framework formerly backed by Amazon. Supports both imperative and symbolic programming. Now in maintenance mode as AWS has shifted focus to PyTorch.
best_for: Legacy systems already built on MXNet
not_ideal_for: Any new project — migrate to PyTorch or TensorFlow
key_features:
- Hybrid imperative/symbolic execution
- Multi-language bindings
- Gluon high-level API
- Distributed training support
- Memory-efficient training
use_cases:
- Legacy ML systems at AWS
- Multi-language ML projects
pros:
- Good memory efficiency
- Multi-language support
cons:
- Effectively abandoned — retired from Apache Incubator
- Tiny community remaining
- No active development
language: Python
languages_supported:
- Python
- C++
- Scala
- Julia
- R
maintained_by: Apache Foundation (retired)
first_release: '2015-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/apache/mxnet
docs_url: https://mxnet.apache.org/
website_url: https://mxnet.apache.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: minimal
maturity: stable
signal_strength: low
backing:
  type: foundation
  orgs:
  - Apache Software Foundation
  funding_or_parent: Retired/archived by Apache in 2023
alternatives:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 20700
  downloads_monthly: 50000
  latest_version: 1.9.1
  latest_release_date: '2022-05-20'
  observed_at: '2026-06-15'
  source: https://github.com/apache/mxnet
aliases:
- apache/mxnet
tags:
- deep-learning
- legacy
- retired
updated: '2026-11-19'
sources:
- url: https://github.com/apache/mxnet
  title: GitHub repository
- url: https://mxnet.apache.org/
  title: Documentation
---

## Overview

Apache Foundation deep learning framework formerly backed by Amazon. Supports both imperative and symbolic programming. Now in maintenance mode as AWS has shifted focus to PyTorch.
