---
id: framework/keras
type: framework
slug: keras
schema_version: 1.1
title: Keras
kind: framework
category: framework-category/training
subcategory: high-level-api
tagline: Multi-backend deep learning framework, with support for JAX, TensorFlow, PyTorch, and OpenVINO (for inference-only).
description: Multi-backend deep learning framework that runs on JAX, TensorFlow and PyTorch, with OpenVINO as an inference-only backend. It is used to build and train models for computer vision, natural language processing, audio processing, timeseries forecasting and recommender systems. It is intended as a drop-in replacement for tf.keras when using the TensorFlow backend.
best_for: Building and training deep learning models, Writing backend-agnostic model code
not_ideal_for: Native Windows (the project recommends WSL2)
key_features:
- JAX, TensorFlow and PyTorch backends
- OpenVINO backend for inference
- Keras models usable inside native PyTorch modules or JAX functions
- Custom layers, models and metrics usable in low-level workflows of any backend
- Training from tf.data pipelines or PyTorch DataLoaders
- Training on GPUs or TPUs from a laptop to large clusters
use_cases:
- Computer vision
- Natural language processing
- Audio processing
- Timeseries forecasting
- Recommender systems
- Moving tf.keras code to other backends
pros:
- One model codebase runs on several backends
- Drop-in replacement for tf.keras on the TensorFlow backend
- Works with existing tf.data and PyTorch data pipelines
cons:
- The backend must be set before importing Keras and cannot be changed afterwards
- The OpenVINO backend supports inference only
- Supported on Linux and macOS, with WSL2 recommended on Windows
language: Python
languages_supported:
- Python
maintained_by: Keras team (keras-team)
license_spdx: Apache-2.0
github_url: https://github.com/keras-team/keras
docs_url: https://keras.io/api/
website_url: https://keras.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: true
ecosystem_connections:
- framework/tensorflow
- framework/jax
- framework/pytorch
- framework/keras-tuner
registry_signals:
  github_stars: 64442
  downloads_monthly: 12107636
  latest_version: 3.15.1
  latest_release_date: '2026-07-29'
  observed_at: '2026-11-20'
  source: https://github.com/keras-team/keras
aliases:
- keras-team/keras
tags:
- deep-learning
- high-level
- beginner-friendly
- multi-backend
updated: '2026-11-21'
sources:
- url: https://github.com/keras-team/keras
  title: GitHub repository
- url: https://keras.io/api/
  title: Documentation
- url: https://keras.io/
  title: Keras website
- url: https://keras.io/getting_started/
  title: Getting started
- url: https://pypi.org/project/keras/
  title: keras — PyPI
---

## Overview

Multi-backend deep learning framework that runs on JAX, TensorFlow and PyTorch, with OpenVINO as an inference-only backend. It is used to build and train models for computer vision, natural language processing, audio processing, timeseries forecasting and recommender systems. It is intended as a drop-in replacement for tf.keras when using the TensorFlow backend.
