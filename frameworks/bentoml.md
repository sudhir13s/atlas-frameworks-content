---
id: framework/bentoml
type: framework
slug: bentoml
schema_version: 1.1
title: BentoML
kind: framework
category: framework-category/llm-serving
subcategory: model-serving
tagline: 'Serve AI apps and models: build model inference APIs, job queues, LLM apps, multi-model pipelines, and more.'
description: BentoML is a Python library for building online serving systems for AI apps and model inference. It turns a model inference script into a REST API server, packages code, models and dependency configs into a Bento as the deployable artifact, and generates Docker images for deployment with Docker or Kubernetes.
best_for: Building model inference APIs and multi-model serving systems in Python
key_features:
- REST API servers defined with Python type hints
- Bento packaging of code, models and dependencies
- Automatic Docker image generation
- Adaptive batching
- Workers and model parallelization
- Multi-model composition and task queues
- Deployment with Docker containers or Kubernetes
use_cases:
- Custom model inference API endpoints
- Multi-model serving pipelines
- Containerized model deployment
- Serving LLMs, image generation, embedding and audio models
pros:
- Supports any ML framework, modality and inference runtime
- Develop, run and debug services locally
cons:
- Collects anonymous usage data by default (opt-out documented)
language: Python
languages_supported:
- Python
maintained_by: BentoML
license_spdx: Apache-2.0
github_url: https://github.com/bentoml/BentoML
docs_url: https://docs.bentoml.com/
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
  - BentoML
alternatives:
- framework/ray-serve
- framework/triton-inference-server
- framework/seldon-core
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 8943
  downloads_monthly: 190534
  latest_version: 1.4.40
  latest_release_date: '2026-10-23'
  observed_at: '2026-11-20'
  source: https://github.com/bentoml/BentoML
aliases:
- bentoml/BentoML
tags:
- serving
- python
- deployment
- containerization
updated: '2026-11-21'
sources:
- url: https://github.com/bentoml/BentoML
  title: GitHub repository
- url: https://docs.bentoml.com/
  title: Documentation
- url: https://docs.bentoml.com/en/latest/build-with-bentoml/gpu-inference.html
  title: GPU inference
- url: https://pypi.org/project/bentoml/
  title: bentoml — PyPI
---

## Overview

BentoML is a Python library for building online serving systems for AI apps and model inference. It turns a model inference script into a REST API server, packages code, models and dependency configs into a Bento as the deployable artifact, and generates Docker images for deployment with Docker or Kubernetes.
