---
id: framework/dvc
type: framework
slug: dvc
schema_version: 3.0
title: DVC (Data Version Control)
status: curated
kind: tool
category: framework-category/mlops
subcategory: data-versioning
tagline: Data Versioning and ML Experiments.
description: DVC is a command line tool and VS Code extension for developing reproducible machine learning projects. It stores data and models in cloud or on-premise storage while keeping their version information in a Git repository. DVC pipelines connect code and data, and experiments are tracked in the local Git repo and compared by parameters and metrics.
best_for: Versioning data and models alongside Git, Reproducible ML pipelines
not_ideal_for: Petabyte-scale data lakes (the docs point to lakeFS)
key_features:
- Git-like data versioning
- ML pipeline definition (dvc.yaml)
- Remote storage backends (S3, GCS, Azure, SSH)
- Experiment tracking and comparison
- Data and model registry
use_cases:
- Dataset versioning alongside code
- Reproducible ML pipelines
- Data and model sharing across teams
pros:
- Version information is kept in the Git repository
- Supports cloud and on-premise remote storage
- Experiment tracking without servers
language: Python
languages_supported:
- Python
maintained_by: Treeverse
license_spdx: Apache-2.0
github_url: https://github.com/treeverse/dvc
docs_url: https://doc.dvc.org/
website_url: https://dvc.org/
maturity: experimental
backing:
  type: corporate
  orgs:
  - Treeverse
alternatives:
- framework/mlflow
registry_signals:
  github_stars: 15985
  downloads_monthly: 2000000
  latest_version: 3.67.1
  latest_release_date: '2026-03-31'
  observed_at: '2026-11-20'
  source: https://github.com/iterative/dvc
aliases:
- iterative/dvc
- treeverse/dvc
tags:
- mlops
- data-versioning
- pipelines
- reproducibility
updated: '2026-11-21'
sources:
- url: https://github.com/treeverse/dvc
  title: GitHub repository
- url: https://doc.dvc.org/
  title: Documentation
- url: https://github.com/treeverse
  title: lakeFS by Treeverse — GitHub organisation
- url: https://dvc.org/
  title: DVC website
- url: https://pypi.org/project/dvc/
  title: dvc — PyPI
---


