---
id: framework/ray-train
type: framework
slug: ray-train
schema_version: 1.1
title: Ray Train
kind: library
category: framework-category/distributed-training
subcategory: training-framework
tagline: Ray Train is a scalable machine learning library for distributed training and fine-tuning.
description: Ray Train is a library for distributed training and fine-tuning built on Ray. It scales model training code from a single machine to a cluster of machines. It supports PyTorch, PyTorch Lightning, Hugging Face Transformers, JAX, TensorFlow, Keras, XGBoost, LightGBM, DeepSpeed and Horovod.
best_for: Distributed training, Fine-tuning
key_features:
- Multi-framework support
- GPU and TPU training
- Checkpoint saving and loading
- Failure and node preemption handling
- Elastic training
- Hyperparameter sweeps with Ray Tune
use_cases:
- Distributed training on Ray clusters
- Fine-tuning
- Fault-tolerant training
pros:
- Scales training code from one machine to a cluster
- Supports many training frameworks
- Built-in checkpointing and failure handling
language: Python
languages_supported:
- Python
maintained_by: The Ray Team
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/train/train.html
website_url: https://www.ray.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
backing:
  type: foundation
  orgs:
  - LF Projects
  - Anyscale
alternatives:
- framework/deepspeed
ecosystem_connections:
- framework/ray-tune
- framework/pytorch
- framework/deepspeed
registry_signals:
  github_stars: 44348
  downloads_monthly: 15757870
  latest_version: 2.60.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/ray-project/ray
tags:
- distributed-training
- ray
- fault-tolerance
- scalable
updated: '2026-11-21'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/train/train.html
  title: Ray Train documentation
- url: https://docs.ray.io/en/latest/train/user-guides/using-gpus.html
  title: Configuring Scale and Accelerators
- url: https://docs.ray.io/en/latest/train/user-guides/hyperparameter-optimization.html
  title: Hyperparameter Optimization
- url: https://docs.ray.io/en/latest/ray-governance/index.html
  title: Ray governance
- url: https://www.ray.io/
  title: Website
---

## Overview

Ray Train is a library for distributed training and fine-tuning built on Ray. It scales model training code from a single machine to a cluster of machines. It supports PyTorch, PyTorch Lightning, Hugging Face Transformers, JAX, TensorFlow, Keras, XGBoost, LightGBM, DeepSpeed and Horovod.
