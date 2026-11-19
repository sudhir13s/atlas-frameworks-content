---
id: framework/pytorch
type: framework
slug: pytorch
schema_version: 1.1
title: PyTorch
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: Tensors and dynamic neural networks with strong GPU acceleration
description: Open-source machine learning framework developed by Meta AI. Known for its dynamic computation graph (eager execution), Pythonic API, and strong research community. The most widely used framework for deep learning research and increasingly for production.
best_for: Research teams and production ML systems needing flexibility and a large ecosystem
not_ideal_for: Simple ML tasks (use scikit-learn), browser deployment (use TF.js), ultra-low-latency mobile (use TF Lite)
key_features:
- Dynamic computation graphs (eager mode)
- torch.compile for production optimization
- Distributed training (DDP, FSDP)
- TorchScript for deployment
- Extensive ecosystem (torchvision, torchaudio, torchtext)
- CUDA integration
- Automatic differentiation
use_cases:
- Deep learning research
- Computer vision
- Natural language processing
- Generative AI model training
- Production ML systems
pros:
- Most popular for research — vast community
- Intuitive Pythonic API
- Dynamic graphs make debugging easy
- Excellent documentation
- Strong ecosystem of extensions
cons:
- Deployment story historically weaker than TF (improving with torch.compile)
- Mobile/edge support less mature than TF Lite
- Memory consumption can be high
language: Python
languages_supported:
- Python
- C++
- CUDA
maintained_by: Meta AI (PyTorch Foundation)
first_release: '2016-09-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/pytorch/pytorch
docs_url: https://pytorch.org/docs/stable/
website_url: https://pytorch.org/
gpu_support:
  nvidia_cuda: true
  amd_rocm: true
  apple_mps: true
  intel_oneapi: true
  google_tpu: true
learning_curve: medium
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Meta
  - PyTorch Foundation (Linux Foundation)
  funding_or_parent: Meta (originated at Facebook AI Research); governance transferred to PyTorch Foundation under Linux Foundation in 2022
alternatives:
- framework/tensorflow
- framework/jax
ecosystem_connections:
- framework/torchvision
- framework/hugging-face-transformers
- framework/lightning
- framework/deepspeed
registry_signals:
  github_stars: 87000
  downloads_monthly: 15000000
  latest_version: '2.6'
  latest_release_date: '2025-01-29'
  observed_at: '2026-06-15'
  source: https://github.com/pytorch/pytorch
tags:
- deep-learning
- neural-networks
- gpu
- research
- production
updated: '2026-11-19'
sources:
- url: https://github.com/pytorch/pytorch
  title: GitHub repository
- url: https://pytorch.org/docs/stable/
  title: Documentation
---

## Overview

Open-source machine learning framework developed by Meta AI. Known for its dynamic computation graph (eager execution), Pythonic API, and strong research community. The most widely used framework for deep learning research and increasingly for production.
