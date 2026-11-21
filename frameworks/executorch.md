---
id: framework/executorch
type: framework
slug: executorch
schema_version: 1.1
title: ExecuTorch
kind: framework
category: framework-category/edge-mobile
subcategory: mobile-runtime
tagline: On-device AI across mobile, embedded and edge for PyTorch.
description: ExecuTorch is PyTorch's end-to-end solution for on-device inference on mobile and edge devices, including wearables, embedded devices and microcontrollers. It is part of the PyTorch Edge ecosystem and uses the same toolchain and SDK from PyTorch model authoring and conversion to debugging and deployment. Backends delegate execution to CPUs, GPUs, NPUs and DSPs.
best_for: Deploying PyTorch models on mobile and edge devices
key_features:
- Native PyTorch model export
- Custom kernel registration
- Hardware delegation (Qualcomm, Apple, Arm)
- Quantization
- Lightweight C++ runtime
use_cases:
- PyTorch model deployment on mobile
- Edge AI with PyTorch
- On-device LLM inference
pros:
- Same toolchain and SDK from PyTorch model authoring to deployment
- Part of the PyTorch Edge ecosystem
cons:
- Some backends such as WebGPU are experimental
language: C++
languages_supported:
- Python
- C++
- Java
maintained_by: PyTorch
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/executorch
docs_url: https://docs.pytorch.org/executorch/
website_url: https://docs.pytorch.org/executorch/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
maturity: stable
backing:
  type: corporate
  orgs:
  - Meta
alternatives:
- framework/tensorflow-lite
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 5183
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
updated: '2026-11-21'
sources:
- url: https://github.com/pytorch/executorch
  title: GitHub repository
- url: https://docs.pytorch.org/executorch/
  title: Documentation
- url: https://docs.pytorch.org/executorch/stable/backends-overview.html
  title: Documentation — Backends overview
- url: https://github.com/pytorch/executorch/blob/main/LICENSE
  title: Licence file
- url: https://pypi.org/project/executorch/
  title: executorch — PyPI
---

## Overview

ExecuTorch is PyTorch's end-to-end solution for on-device inference on mobile and edge devices, including wearables, embedded devices and microcontrollers. It is part of the PyTorch Edge ecosystem and uses the same toolchain and SDK from PyTorch model authoring and conversion to debugging and deployment. Backends delegate execution to CPUs, GPUs, NPUs and DSPs.
