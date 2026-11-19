---
id: framework/caffe2
type: framework
slug: caffe2
schema_version: 1.1
title: Caffe2
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: Lightweight, modular deep learning framework (now merged into PyTorch)
description: Meta's production-focused deep learning framework, successor to the original Caffe from Berkeley. Has been fully merged into PyTorch since 2018 and is no longer maintained as a separate project.
best_for: Nothing — use PyTorch directly
not_ideal_for: Any new project
key_features:
- Mobile deployment focus
- ONNX model export
- Merged into PyTorch backend
use_cases:
- Legacy mobile deployment at Meta
pros:
- Was lightweight and efficient
cons:
- No longer maintained separately
- Fully absorbed into PyTorch
language: Python
languages_supported:
- Python
- C++
maintained_by: Meta AI (merged into PyTorch)
first_release: '2017-04-01'
license_spdx: Apache-2.0
github_url: https://github.com/pytorch/pytorch
docs_url: https://caffe2.ai/
website_url: https://caffe2.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
community_size: none
maturity: stable
signal_strength: low
backing:
  type: corporate
  orgs:
  - Meta
  funding_or_parent: Meta (merged into PyTorch in 2018)
alternatives:
- framework/pytorch
ecosystem_connections:
- framework/pytorch
registry_signals:
  latest_release_date: '2018-05-01'
  observed_at: '2026-06-15'
  source: https://github.com/pytorch/pytorch
tags:
- deep-learning
- legacy
- deprecated
updated: '2026-11-19'
sources:
- url: https://github.com/pytorch/pytorch
  title: GitHub repository
- url: https://caffe2.ai/
  title: Documentation
---

## Overview

Meta's production-focused deep learning framework, successor to the original Caffe from Berkeley. Has been fully merged into PyTorch since 2018 and is no longer maintained as a separate project.
