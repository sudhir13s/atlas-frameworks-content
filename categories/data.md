---
id: framework-category/data
type: framework-category
slug: data
schema_version: 1.1
title: Data & ETL Frameworks
label: Data & ETL
order: 6
short_description: Tools that move, transform, validate, and serve the data and features models train and infer on.
why_it_matters: Model quality is capped by data quality; this layer decides whether your features are clean, reproducible, and consistent.
defacto:
  framework_id: framework/spark-mllib
  reason: Apache Spark is the incumbent for large-scale distributed ETL and batch feature computation.
rising:
- framework_id: framework/polars
  reason: A multi-threaded, Arrow-backed dataframe that is 5-30x faster than pandas on a single machine.
- framework_id: framework/dask
  reason: Scales familiar dataframe/array APIs across cores and clusters when data outgrows memory.
alternatives:
- framework_id: framework/feast
  reason: Feature store that serves the same definitions to training and online inference, killing skew.
- framework_id: framework/great-expectations
  reason: Declarative data-quality gates that fail a pipeline before bad data reaches the model.
key_concepts:
- columnar / Parquet
- data quality
- feature store
- training/serving skew
- idempotency
canonical_reading:
- title: Polars — user guide
  url: https://docs.pola.rs/user-guide/getting-started/
- title: Feast — documentation
  url: https://docs.feast.dev/
- title: Hidden Technical Debt in Machine Learning Systems
  url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
did_you_know:
- Polars can be 5-30x faster than pandas on the same hardware.
- Parquet's columnar layout is why it dominates ML data storage.
- Feature stores exist because training-serving skew causes silent model failures.
tags:
- data
- etl
- feature-store
- data-quality
updated: '2026-11-19'
sources:
- url: https://docs.pola.rs/
  title: Polars documentation
  trust: 0.9
- url: https://docs.feast.dev/
  title: Feast documentation
  trust: 0.9
- url: https://spark.apache.org/docs/latest/ml-guide.html
  title: Apache Spark MLlib guide
  trust: 0.9
---

## Overview

The data and ETL layer turns raw sources into clean, validated, versioned features. It is the least
glamorous and most consequential part of an ML system — most production failures trace back to data,
not the model.

## Landscape

Spark remains the default for large distributed ETL and batch feature computation. Polars is the fast
rising single-machine dataframe, and Dask scales dataframe APIs when data outgrows RAM. Feast (feature
store) and Great Expectations (data quality) are the pieces teams skip early and regret later — they
are what make features consistent and trustworthy across training and serving.

## Notes

Three habits separate a real pipeline from a toy: validation (fail on bad data), idempotency (re-runs
produce identical output), and versioning (any model's inputs are reproducible). Prefer Parquet, and
define features once in a feature store to avoid training/serving skew.
