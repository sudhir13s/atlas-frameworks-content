---
id: framework/seldon-core
type: framework
slug: seldon-core
schema_version: 3.0
title: Seldon Core
status: curated
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: An MLOps framework to package, deploy, monitor and manage production machine learning models.
description: Seldon Core 2 is an MLOps and LLMOps framework for deploying, managing and scaling AI systems in Kubernetes, from single models to modular, data-centric applications. Pipelines connect models, processing steps and custom logic, streaming data between components through Kafka. Experiments route traffic between candidate models or pipelines for A/B tests and shadow deployments.
best_for: Model deployment on Kubernetes, Data-centric ML pipelines
key_features:
- Kubernetes-native deployment
- Kafka-based pipelines
- A/B tests, canary and shadow deployments
- Multi-model serving and overcommit
- Autoscaling of models and servers
- Drift and outlier detection components
- MLServer and Triton Inference Server runtimes
- Open Inference Protocol over REST and gRPC
use_cases:
- ML and LLM deployment on Kubernetes
- Real-time inference pipelines
- Model monitoring and experimentation
pros:
- Kubernetes-native
- Operational and data science monitoring in one framework
- Built-in experiments for A/B tests and shadow deployments
cons:
- Business Source License allows non-production use only without a commercial licence from Seldon
- Business Source License is not an open source licence until each version converts to Apache-2.0
language: Go
maintained_by: Seldon Technologies
license_note: Business Source License 1.1 (Seldon Core v2); each version changes to the Apache License 2.0 four years after its release
github_url: https://github.com/SeldonIO/seldon-core
docs_url: https://docs.seldon.ai/seldon-core-2
website_url: https://docs.seldon.ai/
maturity: production
backing:
  type: corporate
  orgs:
  - Seldon Technologies
alternatives:
- framework/kserve
- framework/bentoml
- framework/ray-serve
registry_signals:
  github_stars: 4781
  downloads_monthly: 100000
  latest_version: '2.9'
  latest_release_date: '2025-01-15'
  observed_at: '2026-11-20'
  source: https://github.com/SeldonIO/seldon-core
aliases:
- SeldonIO/seldon-core
tags:
- serving
- kubernetes
- enterprise
- monitoring
- governance
updated: '2026-11-21'
sources:
- url: https://github.com/SeldonIO/seldon-core
  title: GitHub repository
- url: https://docs.seldon.ai/seldon-core-2
  title: Documentation
- url: https://docs.seldon.ai/seldon-core-2/about/core-features
  title: Seldon Core Features
- url: https://docs.seldon.ai/seldon-core-2/user-guide/servers
  title: Servers
- url: https://docs.seldon.ai/seldon-core-2/user-guide/servers/resource-allocation/example-serving-models-on-dedicated-gpu-nodes
  title: Serving models on dedicated GPU nodes
- url: https://github.com/SeldonIO/seldon-core/blob/v2/LICENSE
  title: Licence
---


