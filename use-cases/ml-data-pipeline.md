---
id: use-case/ml-data-pipeline
type: use-case
slug: ml-data-pipeline
schema_version: 1.1
title: Build a Data Pipeline for ML
label: ML data pipeline
order: 7
goal: Turn raw data into clean, validated, versioned features that training and serving can both trust.
languages:
- python
levels:
- intermediate
stack:
- framework_id: framework/polars
  role: Dataframe engine
  why: A multi-threaded, lazy, Arrow-backed dataframe that is 5-30x faster than pandas on the same hardware.
  install: pip install polars
  quickstart_url: https://docs.pola.rs/user-guide/getting-started/
  docs_url: https://docs.pola.rs/
- framework_id: framework/dask
  role: Scale-out compute
  why: Parallelizes dataframe/array work across cores or a cluster when data no longer fits in memory.
  install: pip install 'dask[complete]'
  quickstart_url: https://docs.dask.org/en/stable/10-minutes-to-dask.html
  docs_url: https://docs.dask.org/
- framework_id: framework/great-expectations
  role: Data quality gates
  why: Declarative expectations catch nulls, ranges, and schema drift before bad data reaches the model.
  install: pip install great_expectations
  quickstart_url: https://docs.greatexpectations.io/docs/core/introduction/try_gx
  docs_url: https://docs.greatexpectations.io/
- framework_id: framework/feast
  role: Feature store
  why: Serves the same feature definitions to training and online inference, killing training/serving skew.
  install: pip install feast
  quickstart_url: https://docs.feast.dev/getting-started/quickstart
  docs_url: https://docs.feast.dev/
day1_plan:
- step: 1
  task: Load and clean with Polars
  estimate: 45 min
  details: Read the raw source, apply lazy transforms, and materialize a clean dataframe. Prefer Parquet output.
- step: 2
  task: Add data quality checks
  estimate: 45 min
  details: Write Great Expectations for the columns that matter (nulls, ranges, categories) and fail the run on violation.
- step: 3
  task: Define features in Feast
  estimate: 60 min
  details: Register feature views so the same definitions feed both the training set and online lookups.
- step: 4
  task: Make it idempotent + versioned
  estimate: 45 min
  details: Write partitioned Parquet, version the data/feature definitions, and ensure re-runs produce identical output.
starter_templates:
- name: Feast quickstart
  repo: https://github.com/feast-dev/feast/tree/master/examples
  why: Official end-to-end feature store examples for training + serving.
- name: Great Expectations examples
  repo: https://github.com/great-expectations/great_expectations/tree/develop/examples
  why: Reference expectation suites and validation flows.
learn_next:
- title: Polars — user guide
  url: https://docs.pola.rs/user-guide/getting-started/
  kind: docs
- title: Feast — what is a feature store
  url: https://docs.feast.dev/
  kind: docs
- title: Hidden Technical Debt in Machine Learning Systems
  url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
  kind: paper
pitfalls:
- 'Training/serving skew: computing a feature one way in training and another at serving silently breaks the model.'
- 'No data validation: garbage in, garbage model. Gate the pipeline on explicit expectations.'
- 'Non-idempotent runs: if re-running the pipeline changes the output, you cannot reproduce a model.'
when_to_level_up: When batch is not enough, add streaming ingestion (Kafka/Flink) and online feature serving; when the DAG grows, orchestrate with Airflow/Dagster and add lineage.
community:
- name: MLOps Community
  url: https://mlops.community/
- name: Feast Slack
  url: https://communityinviter.com/apps/feastio/feast-community
- name: Polars Discord
  url: https://discord.gg/4UfP5cfBE7
dont_use:
- what: pandas for large or repeated jobs
  why: Single-threaded and memory-hungry; Polars (or Dask) is faster and scales past RAM.
- what: Ad-hoc feature code copied between train and serve
  why: That is exactly how training/serving skew starts. Define features once in a feature store.
related_use_cases:
- use-case/train-llm
- use-case/fine-tune
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
- url: https://docs.greatexpectations.io/
  title: Great Expectations documentation
  trust: 0.85
---

## Overview

A model is only as good as the data feeding it. An ML data pipeline turns raw sources into clean,
validated, versioned features — and crucially, serves those features identically to training and to
online inference so the two never drift apart.

## Why this stack

Polars is the fast, modern dataframe default; Dask is the escape hatch when data outgrows one machine.
Great Expectations makes data quality a gate, not a hope. Feast is the piece most teams skip and later
regret: it defines features once and serves them to both training and inference, which is the only
real cure for training/serving skew. All open source.

## Notes

The three habits that separate a toy pipeline from a real one are validation (fail on bad data),
idempotency (re-runs produce identical output), and versioning (you can reproduce any model's inputs).
Add streaming and orchestration only once the batch pipeline is solid.
