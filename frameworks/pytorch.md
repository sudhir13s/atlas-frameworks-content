---
id: framework/pytorch
type: framework
slug: pytorch
schema_version: 1.1
title: PyTorch
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: Tensors and Dynamic neural networks in Python with strong GPU acceleration.
description: PyTorch is a Python package that provides tensor computation with GPU acceleration and deep neural networks built on a tape-based autograd system. It executes imperatively, works with Python libraries such as NumPy and SciPy, and includes torch.compile, torch.export and distributed training. The PyTorch Foundation, hosted by the Linux Foundation, supports the project.
best_for: Deep learning research, GPU-accelerated tensor computation
key_features:
- Eager execution with tape-based autograd
- torch.compile compiler
- Distributed training (DDP, FSDP)
- torch.export for model export
- Domain libraries such as torchvision and torchaudio
- CUDA, ROCm, MPS and Intel GPU backends
- C++ extension API
use_cases:
- Deep learning research
- GPU-accelerated scientific computing
- Computer vision
- Distributed model training
pros:
- Imperative execution with stack traces that point to user code
- New layers can be written in Python or C/C++
- Integrates Intel MKL, cuDNN and NCCL acceleration libraries
language: Python
languages_supported:
- Python
- C++
maintained_by: PyTorch Foundation
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/pytorch
docs_url: https://docs.pytorch.org/docs/stable/
website_url: https://pytorch.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: true
  google_tpu: false
maturity: production
backing:
  type: foundation
  orgs:
  - PyTorch Foundation
  - Linux Foundation
alternatives:
- framework/tensorflow
- framework/jax
ecosystem_connections:
- framework/torchvision
registry_signals:
  github_stars: 105748
  downloads_monthly: 15000000
  latest_version: 2.15.0
  latest_release_date: '2026-10-28'
  observed_at: '2026-11-20'
  source: https://github.com/pytorch/pytorch
tags:
- deep-learning
- neural-networks
- gpu
- research
- production
updated: '2026-11-21'
sources:
- url: https://github.com/pytorch/pytorch
  title: GitHub repository
- url: https://docs.pytorch.org/docs/stable/
  title: Documentation
- url: https://docs.pytorch.org/docs/2.15/notes/mps.html
  title: MPS backend
- url: https://pytorch.org/foundation/
  title: PyTorch Foundation
- url: https://pytorch.org/domains/
  title: PyTorch Domains
- url: https://pypi.org/project/torch/
  title: torch — PyPI
---

## Overview

PyTorch is a Python package that provides tensor computation with GPU acceleration and deep neural networks built on a tape-based autograd system. It executes imperatively, works with Python libraries such as NumPy and SciPy, and includes torch.compile, torch.export and distributed training. The PyTorch Foundation, hosted by the Linux Foundation, supports the project.
