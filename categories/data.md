---
id: framework-category/data
type: framework-category
slug: data
schema_version: 3.0
title: Data & ETL Frameworks
label: Data & ETL
layer: data
order: 6
short_description: Tools that move, transform, validate, and serve the data and features models train and infer on.
why_it_matters: Models are trained and served on this data, so its quality, and whether training and serving see the same features, carries into the model.
defacto:
  framework_id: framework/spark-mllib
  reason: Apache Spark is a unified analytics engine for large-scale data processing, with Spark SQL, DataFrames, a pandas API, MLlib and Structured Streaming.
rising:
- framework_id: framework/polars
  reason: Analytical query engine written in Rust, with multi-threaded vectorized execution, the Apache Arrow columnar format and spill-to-disk for data larger than memory.
- framework_id: framework/dask
  reason: Parallelizes pandas and NumPy, with larger-than-memory execution on one machine and distributed computation on a cluster.
alternatives:
- framework_id: framework/feast
  reason: Open-source feature store that makes the same features available for training and online serving, with point-in-time correct joins.
- framework_id: framework/great-expectations
  reason: Expectations are expressive, extensible unit tests for data, with generated documentation of each validation result.
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
tags:
- data
- etl
- feature-store
- data-quality
updated: '2026-11-21'
sources:
- url: https://github.com/apache/spark
  title: Apache Spark repository
  trust: 0.9
- url: https://github.com/pola-rs/polars
  title: Polars repository
  trust: 0.9
- url: https://docs.dask.org/en/stable/
  title: Dask documentation
  trust: 0.9
- url: https://github.com/feast-dev/feast
  title: Feast repository
  trust: 0.9
- url: https://github.com/fivetran/great_expectations
  title: Great Expectations (GX Core) repository
  trust: 0.9
- url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
  title: Hidden Technical Debt in Machine Learning Systems
  trust: 0.9
---


