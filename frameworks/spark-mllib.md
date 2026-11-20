---
id: framework/spark-mllib
type: framework
slug: spark-mllib
schema_version: 1.1
title: Apache Spark MLlib
kind: library
category: framework-category/data
subcategory: distributed-ml
tagline: Distributed ML algorithms on Apache Spark
description: Machine learning library built on Apache Spark for scalable ML on large datasets. Provides classic ML algorithms (classification, regression, clustering) that run distributed across a Spark cluster. Not for deep learning.
best_for: Classic ML on very large datasets already in Spark
not_ideal_for: Deep learning, small datasets, rapid prototyping
key_features:
- Distributed ML algorithms
- Pipeline API for feature engineering
- Feature transformers library
- Model selection and tuning
- DataFrame-based API
- Integration with Spark ecosystem
use_cases:
- ML on very large datasets (TB+)
- Feature engineering at scale
- Classic ML (not deep learning)
pros:
- Scales to massive datasets
- Integrates with Spark data pipelines
- Supports multiple languages
cons:
- No deep learning support
- Algorithm selection limited compared to sklearn
- Spark cluster overhead
language: Scala
languages_supported:
- Python
- Scala
- Java
- R
maintained_by: Apache Foundation / Databricks
first_release: '2014-09-01'
license_spdx: Apache-2.0
github_url: https://github.com/apache/spark
docs_url: https://spark.apache.org/docs/latest/ml-guide.html
website_url: https://spark.apache.org/mllib/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: large
maturity: production
signal_strength: medium
backing:
  type: foundation
  orgs:
  - Apache Software Foundation
  funding_or_parent: Originated at UC Berkeley AMPLab; commercial support via Databricks
registry_signals:
  github_stars: 44590
  downloads_monthly: 5000000
  latest_version: '3.5'
  latest_release_date: '2024-09-01'
  observed_at: '2026-11-20'
  source: https://github.com/apache/spark
aliases:
- apache/spark
tags:
- data-processing
- distributed
- classic-ml
- big-data
updated: '2026-11-20'
sources:
- url: https://github.com/apache/spark
  title: GitHub repository
- url: https://spark.apache.org/docs/latest/ml-guide.html
  title: Documentation
---

## Overview

Machine learning library built on Apache Spark for scalable ML on large datasets. Provides classic ML algorithms (classification, regression, clustering) that run distributed across a Spark cluster. Not for deep learning.
