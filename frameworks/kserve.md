---
id: framework/kserve
type: framework
slug: kserve
schema_version: 1.1
title: KServe
kind: tool
category: framework-category/llm-serving
subcategory: model-serving
tagline: Standardized Distributed Generative and Predictive AI Inference Platform for Scalable, Multi-Framework Deployment on Kubernetes.
description: Standardized distributed inference platform for generative and predictive AI models on Kubernetes. It serves LLMs through vLLM and llm-d backends with an OpenAI-compatible protocol, and predictive models from TensorFlow, PyTorch, scikit-learn, XGBoost, ONNX and other frameworks. It provides request-based autoscaling, scale-to-zero, canary rollouts and inference pipelines with InferenceGraph, and is a CNCF incubating project.
best_for: Serving generative and predictive models on Kubernetes, Autoscaled inference with scale-to-zero
not_ideal_for: Environments without Kubernetes
key_features:
- vLLM and llm-d backends for LLM serving
- OpenAI-compatible inference protocol
- Request-based autoscaling with scale-to-zero
- Multi-framework serving for predictive models
- Canary rollouts, pipelines and ensembles with InferenceGraph
- Model caching and KV cache offloading
- Model explanations, payload logging, outlier and drift detection
- Optional ModelMesh for high-density model serving
use_cases:
- LLM serving on Kubernetes
- Kubernetes ML serving with autoscaling
- Standardized inference APIs
- Serverless ML endpoints
pros:
- Scale-to-zero frees expensive resources when idle
- One platform for generative and predictive inference
- Available as a Kubeflow add-on component
cons:
- Requires Kubernetes
- The standard Kubernetes installation lacks canary deployment and request-based autoscaling with scale-to-zero (these need the Knative serverless installation)
language: Go
languages_supported:
- Python
- Go
maintained_by: KServe community (CNCF incubating project)
license_spdx: Apache-2.0
github_url: https://github.com/kserve/kserve
docs_url: https://kserve.github.io/website/
website_url: https://kserve.github.io/kserve/
backing:
  type: foundation
  orgs:
  - CNCF
alternatives:
- framework/seldon-core
- framework/triton-inference-server
- framework/bentoml
registry_signals:
  github_stars: 6252
  downloads_monthly: 86581
  latest_version: 0.21.0
  latest_release_date: '2026-09-25'
  observed_at: '2026-11-20'
  source: https://github.com/kserve/kserve
aliases:
- kserve/kserve
tags:
- serving
- kubernetes
- serverless
- autoscaling
updated: '2026-11-21'
sources:
- url: https://github.com/kserve/kserve
  title: GitHub repository
- url: https://kserve.github.io/website/
  title: Documentation
- url: https://kserve.github.io/kserve/
  title: KServe landing page
- url: https://pypi.org/project/kserve/
  title: kserve — PyPI
---

## Overview

Standardized distributed inference platform for generative and predictive AI models on Kubernetes. It serves LLMs through vLLM and llm-d backends with an OpenAI-compatible protocol, and predictive models from TensorFlow, PyTorch, scikit-learn, XGBoost, ONNX and other frameworks. It provides request-based autoscaling, scale-to-zero, canary rollouts and inference pipelines with InferenceGraph, and is a CNCF incubating project.
