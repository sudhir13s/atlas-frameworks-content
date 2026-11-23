---
id: framework/mlflow
type: framework
slug: mlflow
schema_version: 3.0
title: MLflow
status: curated
kind: tool
category: framework-category/mlops
subcategory: experiment-tracking
tagline: The open source AI engineering platform for agents, LLMs, and ML models.
description: MLflow is an open source platform for agents, LLMs and ML models that helps teams debug, evaluate, monitor and optimize AI applications. For LLM and agent work it provides tracing, evaluation, prompt management, prompt optimization and an AI Gateway; for model training it provides experiment tracking, model evaluation, a model registry and deployment. It runs locally, on-premises, on cloud platforms or as a managed service.
best_for: Experiment tracking and model management, Tracing and evaluating LLM applications and agents
key_features:
- Experiment tracking (parameters, metrics, evaluation results)
- Model registry for the model lifecycle
- Deployment to Docker, Kubernetes, Azure ML and AWS SageMaker
- Tracing for LLM applications and agents with OpenTelemetry support
- LLM evaluation and monitoring
- Prompt registry and prompt optimization
- AI Gateway for managing model access and costs
- Native integrations with scikit-learn, XGBoost, TensorFlow, PyTorch, Keras and Spark MLlib
use_cases:
- ML experiment tracking
- Model versioning and registry
- Model deployment
- Debugging and evaluating LLM applications
pros:
- Vendor-neutral and self-hostable
- Covers both classic ML and LLM workflows
- Tracing for Python, TypeScript/JavaScript and Java applications
language: Python
languages_supported:
- Python
- TypeScript/JavaScript
- Java
maintained_by: MLflow Project (a Series of LF Projects, LLC)
license_spdx: Apache-2.0
github_url: https://github.com/mlflow/mlflow
docs_url: https://mlflow.org/docs/latest/
website_url: https://mlflow.org/
maturity: production
backing:
  type: foundation
  orgs:
  - Linux Foundation
alternatives:
- framework/wandb
- framework/clearml
ecosystem_connections:
- framework/pytorch
- framework/tensorflow
registry_signals:
  github_stars: 28908
  downloads_monthly: 22613805
  latest_version: 3.18.0
  latest_release_date: '2026-11-03'
  observed_at: '2026-11-20'
  source: https://github.com/mlflow/mlflow
aliases:
- mlflow/mlflow
tags:
- mlops
- experiment-tracking
- model-registry
- deployment
updated: '2026-11-21'
sources:
- url: https://github.com/mlflow/mlflow
  title: GitHub repository
- url: https://mlflow.org/docs/latest/
  title: Documentation
- url: https://mlflow.org/docs/latest/ml/
  title: MLflow for model training
- url: https://mlflow.org/
  title: MLflow website
- url: https://pypi.org/project/mlflow/
  title: mlflow — PyPI
---


