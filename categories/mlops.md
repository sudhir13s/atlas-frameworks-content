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
why_it_matters: Without tracking you cannot reproduce results or know which change helped; MLOps turns runs into reliable releases.
defacto:
  framework_id: framework/mlflow
  reason: The open standard for experiment tracking, a model registry, and packaging — vendor-neutral and widely integrated.
rising:
- framework_id: framework/wandb
  reason: Best-in-class experiment dashboards and collaboration; ubiquitous in research.
alternatives:
- framework_id: framework/clearml
  reason: End-to-end MLOps with orchestration and data management in one open platform.
- framework_id: framework/dvc
  reason: Git-native data and model versioning; pairs pipelines with your code history.
- framework_id: framework/comet-ml
  reason: Experiment tracking with strong model production monitoring.
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
  url: https://docs.wandb.ai/quickstart/
- title: Hidden Technical Debt in Machine Learning Systems
  url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
did_you_know:
- MLflow was open-sourced by Databricks in 2018.
- The 'Hidden Technical Debt' paper (Sculley et al.) remains the field's founding text.
- W&B's free tier is used by a large fraction of academic ML research.
tags:
- mlops
- experiment-tracking
- model-registry
- reproducibility
updated: '2026-11-19'
sources:
- url: https://mlflow.org/docs/latest/index.html
  title: MLflow documentation
  trust: 0.9
- url: https://docs.wandb.ai/
  title: Weights & Biases documentation
  trust: 0.9
- url: https://clear.ml/docs/latest/
  title: ClearML documentation
  trust: 0.85
---

## Overview

Experiment tracking and MLOps make ML work reproducible and shippable: they record every run's params,
metrics, and artifacts, version data and models, and manage the promotion from an experiment to a
registered, deployable model.

## Landscape

MLflow is the vendor-neutral default, covering tracking, a model registry, and packaging. Weights &
Biases leads on experiment dashboards and is ubiquitous in research. ClearML offers a fuller end-to-end
platform; DVC brings Git-native data/model versioning; Neptune and Comet cover metadata at scale and
production monitoring respectively.

## Notes

Adopt tracking on day one — retrofitting reproducibility after the fact is painful. Many teams pair
W&B (for dashboards) with MLflow (for the registry). Whatever you choose, version data and models, not
just code, or "which run produced this?" becomes unanswerable.
