---
id: framework/tensorflow
type: framework
slug: tensorflow
schema_version: 1.1
title: TensorFlow
kind: framework
category: framework-category/training
subcategory: core-framework
tagline: An Open Source Machine Learning Framework for Everyone.
description: TensorFlow is an end-to-end open source platform for machine learning. It provides stable Python and C++ APIs and the high-level Keras API for building and training models, with TensorFlow Lite for mobile and edge devices, TensorFlow.js for JavaScript environments and TFX for production ML pipelines.
best_for: Building and deploying ML models end to end, Deployment to mobile and edge devices, ML in JavaScript environments
key_features:
- Keras as the high-level API
- Eager execution and tf.function graphs
- Distribution Strategy API for distributed training
- XLA compilation
- SavedModel format for deployment
- TensorBoard visualization
- TensorFlow Lite for mobile and edge devices
- TensorFlow.js for JavaScript environments
- TensorFlow Serving for model serving
use_cases:
- Production ML pipelines with TFX
- Mobile and edge deployment
- Browser-based ML with TensorFlow.js
- Model serving
- Training on TPUs
pros:
- TensorBoard for experiment visualization
- TPU support
- Stable Python and C++ APIs
cons:
- APIs in languages other than Python are not covered by the API stability promises
language: C++
languages_supported:
- Python
- C++
- JavaScript
- Java
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/tensorflow/tensorflow
docs_url: https://www.tensorflow.org/api_docs
website_url: https://www.tensorflow.org/
maturity: production
backing:
  type: corporate
  orgs:
  - Google
alternatives:
- framework/pytorch
- framework/jax
ecosystem_connections:
- framework/keras
- framework/tensorflow-lite
- framework/tf-serving
registry_signals:
  github_stars: 201661
  downloads_monthly: 12374104
  latest_version: 2.21.0
  latest_release_date: '2026-03-06'
  observed_at: '2026-11-20'
  source: https://github.com/tensorflow/tensorflow
tags:
- deep-learning
- neural-networks
- gpu
- production
- mobile
- enterprise
updated: '2026-11-21'
sources:
- url: https://github.com/tensorflow/tensorflow
  title: GitHub repository
- url: https://www.tensorflow.org/api_docs
  title: Documentation
- url: https://www.tensorflow.org/about
  title: Why TensorFlow
- url: https://www.tensorflow.org/install/pip
  title: Install TensorFlow with pip
- url: https://www.tensorflow.org/install/gpu_plugins
  title: GPU device plugins
- url: https://www.tensorflow.org/guide/tpu
  title: Use TPUs
- url: https://openxla.org/xla/tf2xla
  title: Use XLA in TensorFlow
- url: https://www.tensorflow.org/guide/saved_model
  title: SavedModel format
- url: https://www.tensorflow.org/tensorboard
  title: TensorBoard
- url: https://pypi.org/project/tensorflow/
  title: tensorflow — PyPI
---

## Overview

TensorFlow is an end-to-end open source platform for machine learning. It provides stable Python and C++ APIs and the high-level Keras API for building and training models, with TensorFlow Lite for mobile and edge devices, TensorFlow.js for JavaScript environments and TFX for production ML pipelines.
