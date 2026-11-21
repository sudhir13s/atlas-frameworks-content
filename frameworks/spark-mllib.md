---
id: framework/spark-mllib
type: framework
slug: spark-mllib
schema_version: 1.1
title: Apache Spark MLlib
kind: library
category: framework-category/data
subcategory: distributed-ml
tagline: MLlib is Spark's machine learning (ML) library.
description: MLlib is Apache Spark's machine learning library, built to make practical machine learning scalable. It provides common learning algorithms for classification, regression, clustering and collaborative filtering, together with featurization, ML Pipelines, model persistence and utilities. Its primary API is DataFrame-based; the older RDD-based API is in maintenance mode.
best_for: Scalable machine learning on Spark, ML pipelines on Spark DataFrames
key_features:
- Classification, regression, clustering and collaborative filtering
- Feature extraction, transformation and selection
- ML Pipelines for constructing, evaluating and tuning
- Model selection and tuning
- Saving and loading models and Pipelines
- Frequent pattern mining
- DataFrame-based API
use_cases:
- Machine learning on large-scale data in Spark
- Feature engineering
- Recommendation with collaborative filtering
pros:
- Uniform API across algorithms and languages
- Works on Spark DataFrames with Spark data sources and SQL queries
cons:
- RDD-based API is in maintenance mode
- R API is deprecated
language: Scala
languages_supported:
- Python
- Scala
- Java
- R
maintained_by: Apache Software Foundation
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
maturity: production
backing:
  type: foundation
  orgs:
  - Apache Software Foundation
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
updated: '2026-11-21'
sources:
- url: https://github.com/apache/spark
  title: GitHub repository
- url: https://spark.apache.org/docs/latest/ml-guide.html
  title: Documentation
- url: https://pypi.org/project/pyspark/
  title: pyspark — PyPI
---

## Overview

MLlib is Apache Spark's machine learning library, built to make practical machine learning scalable. It provides common learning algorithms for classification, regression, clustering and collaborative filtering, together with featurization, ML Pipelines, model persistence and utilities. Its primary API is DataFrame-based; the older RDD-based API is in maintenance mode.
