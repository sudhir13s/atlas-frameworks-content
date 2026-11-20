---
id: framework/executorch
type: framework
slug: executorch
schema_version: 1.1
title: ExecuTorch
kind: framework
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: PyTorch's on-device inference framework for mobile and edge
description: PyTorch's official solution for deploying models on mobile and edge devices. End-to-end from PyTorch model to on-device execution with operator-level customization and hardware delegation. Successor to PyTorch Mobile.
best_for: PyTorch teams wanting native edge deployment
not_ideal_for: Production mobile apps needing mature tooling (use TF Lite for now)
key_features:
- Native PyTorch model export
- Operator-level customization
- Hardware delegation (Qualcomm, Apple, ARM)
- Quantization via PyTorch
- Minimal runtime footprint
use_cases:
- PyTorch model deployment on mobile
- Edge AI with PyTorch
- On-device LLM inference
pros:
- Native PyTorch integration
- Growing hardware delegate ecosystem
- Official PyTorch edge solution
cons:
- Still early — less mature than TF Lite
- Limited hardware delegate coverage
- Documentation is still growing
language: C++
languages_supported:
- Python
- C++
- Java
- Swift
maintained_by: Meta AI (PyTorch Foundation)
first_release: '2023-10-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/executorch
docs_url: https://pytorch.org/executorch/
website_url: https://pytorch.org/executorch/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: small-medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Meta
  - PyTorch Foundation
  funding_or_parent: Meta (PyTorch on-device successor); launched 2023
alternatives:
- framework/tensorflow-lite
ecosystem_connections:
- framework/pytorch
- framework/llama-cpp
registry_signals:
  github_stars: 5182
  downloads_monthly: 69901
  latest_version: 1.6.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/pytorch/executorch
aliases:
- pytorch/executorch
tags:
- edge-mobile
- pytorch
- mobile
- edge
updated: '2026-11-20'
sources:
- url: https://github.com/pytorch/executorch
  title: GitHub repository
- url: https://pytorch.org/executorch/
  title: Documentation
---

## Overview

PyTorch's official solution for deploying models on mobile and edge devices. End-to-end from PyTorch model to on-device execution with operator-level customization and hardware delegation. Successor to PyTorch Mobile.
