---
id: framework-category/mlops
type: framework-category
slug: mlops
schema_version: 2.1
title: Experiment Tracking & MLOps
label: Experiment Tracking & MLOps
layer: operate
order: 7
short_description: Tools that track experiments, version models and data, and manage the path from a run to a registered model.
why_it_matters: Without tracking, a result cannot be reproduced and a change cannot be tied to its effect.
defacto:
  framework_id: framework/mlflow
  reason: Open-source platform with experiment tracking, a model registry and model evaluation, plus tracing and evaluation for LLM applications.
rising:
- framework_id: framework/wandb
  reason: Tracks and visualizes machine-learning experiments, from datasets to production models.
alternatives:
- framework_id: framework/clearml
  reason: Open-source suite with experiment tracking, orchestration and pipelines, data management and model serving.
- framework_id: framework/dvc
  reason: Command-line tool that versions data and models alongside Git, with lightweight pipelines and experiment tracking in the local repository.
- framework_id: framework/comet-ml
  reason: Experiment tracking for datasets, code changes, experiment history and production models.
key_concepts:
- experiment tracking
- model registry
- data versioning
- reproducibility
- lineage
canonical_reading:
- title: MLflow — documentation
  url: https://mlflow.org/docs/latest/index.html
- title: Weights & Biases — quickstart
  url: https://docs.coreweave.com/products/wandb/quickstart
- title: Hidden Technical Debt in Machine Learning Systems
  url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
tags:
- mlops
- experiment-tracking
- model-registry
- reproducibility
updated: '2026-11-21'
sources:
- url: https://github.com/mlflow/mlflow
  title: MLflow repository
  trust: 0.9
- url: https://github.com/wandb/wandb
  title: Weights & Biases SDK repository
  trust: 0.9
- url: https://github.com/clearml/clearml
  title: ClearML repository
  trust: 0.9
- url: https://github.com/treeverse/dvc
  title: DVC repository
  trust: 0.9
- url: https://github.com/comet-ml/comet-examples
  title: Comet examples repository
  trust: 0.9
---
