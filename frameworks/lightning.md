---
id: framework/lightning
type: framework
slug: lightning
schema_version: 1.1
title: PyTorch Lightning
kind: framework
category: framework-category/training
subcategory: training-framework
tagline: Organizes PyTorch code to automate training infrastructure such as backpropagation, mixed precision, multi-GPU and distributed training, while keeping full control over model logic.
description: PyTorch Lightning is a deep learning framework to pretrain and finetune AI models that organizes PyTorch code to decouple the science from the engineering. It automates backpropagation, mixed precision, multi-GPU and distributed training while keeping full control over model logic, and scales from CPU to multi-node GPUs without changes to the core code. Lightning Fabric offers expert-level control over the training loop and scaling strategy.
best_for: Pretraining and finetuning PyTorch models, Scaling PyTorch training from CPU to multi-node GPUs
key_features:
- LightningModule for organized training code
- Distributed training strategies (DDP, FSDP, DeepSpeed)
- Mixed precision training
- Callbacks such as early stopping and checkpointing
- Logger integrations (TensorBoard, Weights & Biases, Comet, MLflow)
- Export to TorchScript and ONNX
- Lightning Fabric for custom training loops
use_cases:
- Organized PyTorch training code
- Multi-GPU and TPU training without code changes
- Finetuning models for classification, segmentation and summarization
pros:
- Same code runs on CPU, GPU and TPU
- LightningModules remain PyTorch modules
- Choice of abstraction level between Trainer and Fabric
language: Python
languages_supported:
- Python
maintained_by: Lightning AI
license_spdx: Apache-2.0
github_url: https://github.com/Lightning-AI/pytorch-lightning
docs_url: https://lightning.ai/docs/pytorch/stable/
website_url: https://lightning.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: true
backing:
  type: corporate
  orgs:
  - Lightning AI
alternatives:
- framework/pytorch
- framework/keras
ecosystem_connections:
- framework/pytorch
- framework/wandb
- framework/mlflow
- framework/deepspeed
registry_signals:
  github_stars: 31467
  downloads_monthly: 11733050
  latest_version: 2.6.6
  latest_release_date: '2026-09-10'
  observed_at: '2026-11-20'
  source: https://github.com/Lightning-AI/pytorch-lightning
aliases:
- Lightning-AI/pytorch-lightning
tags:
- deep-learning
- pytorch
- training
- distributed
- organized
updated: '2026-11-21'
sources:
- url: https://github.com/Lightning-AI/pytorch-lightning
  title: GitHub repository
- url: https://lightning.ai/docs/pytorch/stable/
  title: Documentation
- url: https://lightning.ai/docs/pytorch/stable/extensions/accelerator.html
  title: Accelerator
- url: https://lightning.ai/docs/pytorch/stable/accelerators/gpu_basic.html
  title: GPU training (basic)
- url: https://pypi.org/project/pytorch-lightning/
  title: pytorch-lightning — PyPI
---

## Overview

PyTorch Lightning is a deep learning framework to pretrain and finetune AI models that organizes PyTorch code to decouple the science from the engineering. It automates backpropagation, mixed precision, multi-GPU and distributed training while keeping full control over model logic, and scales from CPU to multi-node GPUs without changes to the core code. Lightning Fabric offers expert-level control over the training loop and scaling strategy.
