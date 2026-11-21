---
id: framework/paddlepaddle
type: framework
slug: paddlepaddle
schema_version: 1.1
title: PaddlePaddle
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: 'PArallel Distributed Deep LEarning: Machine Learning Framework from Industrial Practice.'
description: PaddlePaddle (PArallel Distributed Deep LEarning) is a deep learning framework that supports both training and inference. It unifies dynamic and static graphs with automatic parallelism, and includes a neural network compiler, high-order automatic differentiation for scientific computing and a pluggable adaptation layer for multiple hardware types.
best_for: Deep learning training and inference, Distributed training
key_features:
- Distributed training with automatic parallelism
- Unified dynamic and static graphs
- Neural network compiler
- High-order automatic differentiation
- Inference deployment and model compression
- Custom device and custom kernel interfaces
use_cases:
- Large model training and inference
- Distributed model training
- Scientific computing with automatic differentiation
pros:
- Training and inference in the same framework
- Pluggable support for multiple hardware types
language: C++
languages_supported:
- Python
- C++
maintained_by: Baidu
license_spdx: Apache-2.0
github_url: https://github.com/PaddlePaddle/Paddle
docs_url: https://www.paddlepaddle.org.cn/documentation/docs/en/guides/index_en.html
website_url: https://www.paddlepaddle.org.cn/en
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
maturity: production
backing:
  type: corporate
  orgs:
  - Baidu
alternatives:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 24147
  downloads_monthly: 1152518
  latest_version: 3.3.1
  latest_release_date: '2026-03-24'
  observed_at: '2026-11-20'
  source: https://github.com/PaddlePaddle/Paddle
aliases:
- PaddlePaddle/Paddle
tags:
- deep-learning
- chinese-ecosystem
- nlp
- ocr
- industrial
updated: '2026-11-21'
sources:
- url: https://github.com/PaddlePaddle/Paddle
  title: GitHub repository
- url: https://www.paddlepaddle.org.cn/documentation/docs/en/guides/index_en.html
  title: Documentation
- url: https://www.paddlepaddle.org.cn/documentation/docs/en/install/pip/linux-pip_en.html
  title: Install on Linux via PIP
- url: https://pypi.org/project/paddlepaddle/
  title: paddlepaddle — PyPI
---

## Overview

PaddlePaddle (PArallel Distributed Deep LEarning) is a deep learning framework that supports both training and inference. It unifies dynamic and static graphs with automatic parallelism, and includes a neural network compiler, high-order automatic differentiation for scientific computing and a pluggable adaptation layer for multiple hardware types.
