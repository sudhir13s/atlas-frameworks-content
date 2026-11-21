---
id: framework/tf-serving
type: framework
slug: tf-serving
schema_version: 1.1
title: TensorFlow Serving
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: A flexible serving system for machine learning models.
description: TensorFlow Serving is a serving system for machine learning models, designed for production environments. It manages trained models and gives clients versioned access over gRPC and HTTP endpoints. It integrates with TensorFlow models out of the box and can be extended to serve other types of models and data.
best_for: Serving TensorFlow models in production
key_features:
- Serves multiple models or multiple versions of a model at once
- gRPC and HTTP (REST) inference endpoints
- New model versions deploy without client code changes
- Canary releases and A/B testing of model versions
- Request batching scheduler for GPU execution
- SavedModel warmup
- Extensible with custom servables and sources
use_cases:
- Production TensorFlow model serving
- Model version rollout and rollback
pros:
- Out-of-the-box integration with TensorFlow SavedModel
- Modular architecture that can be extended to new servable types
language: C++
languages_supported:
- C++
- Python
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/tensorflow/serving
docs_url: https://www.tensorflow.org/tfx/guide/serving
website_url: https://www.tensorflow.org/tfx/guide/serving
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
  - Google
alternatives:
- framework/triton-inference-server
ecosystem_connections:
- framework/tensorflow
registry_signals:
  github_stars: 6363
  downloads_monthly: 500000
  latest_version: 2.21.0
  latest_release_date: '2026-09-29'
  observed_at: '2026-11-20'
  source: https://github.com/tensorflow/serving
aliases:
- tensorflow/serving
tags:
- serving
- tensorflow
- production
- high-performance
updated: '2026-11-21'
sources:
- url: https://github.com/tensorflow/serving
  title: GitHub repository
- url: https://www.tensorflow.org/tfx/guide/serving
  title: Documentation
- url: https://www.tensorflow.org/tfx/serving/docker
  title: TensorFlow Serving with Docker
- url: https://pypi.org/project/tensorflow-serving-api/
  title: tensorflow-serving-api — PyPI
---

## Overview

TensorFlow Serving is a serving system for machine learning models, designed for production environments. It manages trained models and gives clients versioned access over gRPC and HTTP endpoints. It integrates with TensorFlow models out of the box and can be extended to serve other types of models and data.
