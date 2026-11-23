---
id: framework/ray-serve
type: framework
slug: ray-serve
schema_version: 3.0
title: Ray Serve
status: curated
kind: library
category: framework-category/llm-serving
subcategory: model-serving
tagline: Ray Serve is a scalable model serving library for building online inference APIs.
description: Ray Serve is a framework-agnostic model serving library built on top of Ray. It supports model composition and multi-model serving, combining multiple ML models and business logic in Python code. For large language models it offers response streaming, dynamic request batching and multi-node, multi-GPU serving.
best_for: Model composition, Multi-model serving
not_ideal_for: Model lifecycle management, Model-specific optimizations
key_features:
- Python model composition API
- Multi-model serving
- Dynamic request batching
- Replica autoscaling
- FastAPI integration
- Fractional GPU allocation
- Framework-agnostic
use_cases:
- Multi-model serving pipelines
- LLM serving
- Online inference APIs
pros:
- Models and business logic composed in one Python program
- Same code runs on a laptop or a cluster
- Not tied to a specific ML framework
cons:
- No model-specific optimizations
- No model lifecycle management or performance visualization
language: Python
languages_supported:
- Python
maintained_by: The Ray Team
license_spdx: Apache-2.0
github_url: https://github.com/ray-project/ray
docs_url: https://docs.ray.io/en/latest/serve/
website_url: https://www.ray.io/ray-serve
backing:
  type: foundation
  orgs:
  - LF Projects
  - Anyscale
alternatives:
- framework/bentoml
- framework/triton-inference-server
ecosystem_connections:
- framework/vllm
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 44348
  downloads_monthly: 15757870
  latest_version: 2.60.0
  latest_release_date: '2026-11-04'
  observed_at: '2026-11-20'
  source: https://github.com/ray-project/ray
tags:
- serving
- distributed
- scalable
- multi-model
updated: '2026-11-21'
sources:
- url: https://github.com/ray-project/ray
  title: GitHub repository
- url: https://docs.ray.io/en/latest/serve/
  title: Documentation
- url: https://docs.ray.io/en/latest/serve/index.html
  title: Ray Serve documentation
- url: https://docs.ray.io/en/latest/ray-core/scheduling/accelerators.html
  title: Ray accelerator support
- url: https://docs.ray.io/en/latest/ray-governance/index.html
  title: Ray governance
- url: https://www.ray.io/
  title: Website
---


