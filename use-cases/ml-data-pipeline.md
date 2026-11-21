---
id: use-case/ml-data-pipeline
type: use-case
slug: ml-data-pipeline
schema_version: 2.0
title: Build a Data Pipeline for ML
label: ML data pipeline
order: 7
goal: Turn raw source data into validated, versioned and traceable datasets and features that training jobs and serving models read the same way.
stages:
- id: ingest
  name: Ingest
  note: Runs on a schedule or continuously as source data arrives.
- id: process
  name: Process
  note: Runs after each ingest to clean, join and label the data.
- id: govern
  name: Validate and version
  note: Runs on every new batch before it reaches training.
- id: serve
  name: Serve to training
  note: Runs whenever a training job or an online model reads the data.
blocks:
- id: orchestration
  stage: ingest
  name: Orchestration
  purpose: Schedules, retries and monitors every step of the pipeline from ingest to training export.
  options:
  - name: Apache Airflow
    url: https://airflow.apache.org/
    choice: default
    when: A community-built platform that authors, schedules and monitors workflows as Python code, scales workers through a message queue and ships operators for major clouds and services.
  - name: Dagster
    url: https://github.com/dagster-io/dagster
    choice: alternative
    when: When you think in data assets such as tables, datasets and models; Apache-2.0, with lineage and observability built in.
  - name: Prefect
    url: https://github.com/PrefectHQ/prefect
    choice: alternative
    when: When existing Python scripts should become workflows; Apache-2.0, adding scheduling, caching, retries and event-based automations.
  - record: framework/dvc
    choice: alternative
    when: When the pipeline is a few steps inside one Git repository; DVC pipelines rerun only the steps a change affects.
  how_to_choose:
  - Choose an asset-centric orchestrator (Dagster) when you reason about tables and datasets, and a task-centric one (Airflow, Prefect) when you reason about jobs.
  - Make every step idempotent so a retry or backfill cannot duplicate rows.
- id: ingest
  stage: ingest
  name: Ingestion
  purpose: Moves data from APIs, databases, files and event streams into your storage.
  options:
  - name: dlt
    url: https://github.com/dlt-hub/dlt
    choice: default
    when: Apache-2.0 Python library that loads REST APIs, SQL databases and files into DuckDB, warehouses, Iceberg or Delta, with schema inference and incremental loading.
  - name: Airbyte
    url: https://github.com/airbytehq/airbyte
    choice: alternative
    when: When you want a large connector catalogue and a UI; self-hosted or cloud, with MIT and ELv2 licences in its repository.
  - name: Apache Kafka
    url: https://kafka.apache.org/
    choice: alternative
    when: When data arrives as events; a distributed, durable event streaming platform whose Connect interface links event sources and sinks.
  how_to_choose:
  - Send batch sources and APIs through dlt or Airbyte, and continuous event streams through Kafka.
  - Load incrementally so a rerun fetches only new or changed rows.
- id: storage
  stage: ingest
  name: Storage format
  purpose: The on-disk format every later step reads and writes.
  options:
  - name: Apache Parquet
    url: https://parquet.apache.org/
    choice: default
    when: Open-source column-oriented file format with compression and encoding; Hugging Face Datasets streams selected columns from it and filters on its statistics.
  - name: Apache Iceberg
    url: https://iceberg.apache.org/
    choice: alternative
    when: When several engines share tables; adds schema evolution, snapshot time travel and rollback, and is read by Spark, Trino, Flink and others.
  - name: Delta Lake
    url: https://delta.io/
    choice: alternative
    when: When you need ACID transactions with serializable isolation and time travel; a Linux Foundation project read by Spark, Flink, Trino and others.
  how_to_choose:
  - Plain Parquet files suffice for append-only training snapshots.
  - Move to a table format when rows are updated or several writers share one table.
- id: processing
  stage: process
  name: Processing engine
  purpose: Cleans, joins, deduplicates and transforms data into training-ready tables.
  options:
  - record: framework/polars
    choice: default
    when: MIT-licensed, multi-threaded query engine on Apache Arrow with optimized lazy queries and spill to disk when data exceeds RAM.
  - record: framework/dask
    choice: alternative
    when: When pandas or NumPy code must scale; it parallelizes both from one machine to clusters on Kubernetes, HPC schedulers or cloud services.
  - name: Apache Spark
    url: https://spark.apache.org/
    choice: alternative
    when: When the data already lives in a Spark cluster; a multi-language engine for batch and streaming jobs and distributed SQL.
  - name: Ray Data
    url: https://docs.ray.io/en/latest/data/data.html
    choice: alternative
    when: When preprocessing needs GPUs, such as embedding or batch inference; a streaming engine that keeps CPUs and GPUs busy.
  how_to_choose:
  - Start on one machine with Polars.
  - Move to Dask, Spark or Ray Data only when one machine cannot hold or finish the job.
  browse:
    label: All data tools
    record: framework-category/data
- id: labeling
  stage: process
  name: Labelling
  purpose: Adds human labels to examples that the source data does not already label.
  options:
  - record: framework/label-studio
    choice: default
    when: Apache-2.0 labelling tool for text, images, audio, video, time series and HTML that can show model predictions for pre-labelling.
  how_to_choose:
  - Version labels together with the data they describe.
  - Skip this block when labels come with the source data.
- id: validation
  stage: govern
  name: Data validation
  purpose: Stops a batch that breaks schema or quality rules before it reaches training.
  options:
  - record: framework/great-expectations
    choice: default
    when: Apache-2.0; Expectations act as unit tests for data, and each validation run produces documentation that can be shared.
  - name: Pandera
    url: https://github.com/unionai-oss/pandera
    choice: alternative
    when: When checks should live next to dataframe code; MIT-licensed schemas for pandas, Polars and PySpark written as Python classes with type annotations.
  - name: TensorFlow Data Validation
    url: https://github.com/tensorflow/data-validation
    choice: alternative
    when: When you want schemas inferred from data; it computes summary statistics, infers a schema and flags anomalies such as missing features, scaling through Apache Beam.
  how_to_choose:
  - Fail the pipeline on a broken rule instead of passing bad rows to training.
  - Validate both after ingest and after processing, since each step can introduce errors.
- id: versioning
  stage: govern
  name: Data versioning
  purpose: Gives every dataset an immutable version that a training run can name.
  options:
  - record: framework/dvc
    choice: default
    when: Apache-2.0; keeps data and model version information in Git while the files live in remote storage.
  - name: lakeFS
    url: https://github.com/treeverse/lakeFS
    choice: alternative
    when: When versions must live directly in S3, Azure Blob Storage or Google Cloud Storage; Git-like branches and rollback, licensed BUSL-1.1, which allows free use only for non-production purposes.
  how_to_choose:
  - Record the data version with every training run so a model traces back to its exact inputs.
  - If the storage layer is Iceberg or Delta Lake, their snapshots already give time travel.
- id: lineage
  stage: govern
  name: Lineage
  purpose: Records which job read and wrote which dataset, so a bad model or table can be traced upstream.
  options:
  - name: OpenLineage
    url: https://github.com/OpenLineage/OpenLineage
    choice: default
    when: Apache-2.0 open standard for run, job and dataset metadata with integrations for Spark, Airflow, dbt and Flink, and Marquez as its reference implementation.
  - name: Dagster
    url: https://github.com/dagster-io/dagster
    choice: alternative
    when: When Dagster is already the orchestrator; it tracks lineage between the assets it builds.
  how_to_choose:
  - Emit lineage from the orchestrator and processing engine rather than recording it by hand.
- id: feature-store
  stage: serve
  name: Feature store
  purpose: Serves the same feature values to training jobs and to online models.
  options:
  - record: framework/feast
    choice: default
    when: Apache-2.0 feature store with an offline store for training, an online store for serving and point-in-time correct joins that keep future values out of training data.
  how_to_choose:
  - Use it for timestamped structured features shared by training and online inference.
  - Feast is not a pipeline, orchestrator or warehouse, so it sits downstream of them.
- id: training-input
  stage: serve
  name: Training data loader
  purpose: Streams versioned datasets into the training loop.
  options:
  - record: framework/datasets
    choice: default
    when: Streams Parquet, JSON or Hub datasets as iterable datasets with shuffling, sharding across PyTorch DataLoader workers and resumable state.
  - name: Ray Data
    url: https://docs.ray.io/en/latest/data/data.html
    choice: alternative
    when: When preprocessing already runs on a Ray cluster; it handles data loading for ML training with streaming execution.
  how_to_choose:
  - Stream when the dataset exceeds local disk.
  - Use a map-style dataset when training needs random access to examples.
learn_next:
- title: Hidden Technical Debt in Machine Learning Systems
  url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
  kind: paper
- title: Feast documentation
  url: https://docs.feast.dev/
  kind: docs
- title: Hugging Face Datasets, streaming
  url: https://huggingface.co/docs/datasets/stream
  kind: docs
- title: OpenLineage
  url: https://github.com/OpenLineage/OpenLineage
  kind: docs
related_use_cases:
- use-case/train-llm
- use-case/fine-tune
- use-case/serve-in-production
tags:
- data-pipeline
- data-quality
- data-versioning
- lineage
- feature-store
- orchestration
updated: '2026-11-21'
sources:
- url: https://airflow.apache.org/
  title: Apache Airflow
  trust: 0.9
- url: https://github.com/dagster-io/dagster
  title: dagster-io/dagster, GitHub repository
  trust: 0.85
- url: https://github.com/PrefectHQ/prefect
  title: PrefectHQ/prefect, GitHub repository
  trust: 0.85
- url: https://github.com/iterative/dvc
  title: DVC, GitHub repository
  trust: 0.85
- url: https://github.com/dlt-hub/dlt
  title: dlt-hub/dlt, GitHub repository
  trust: 0.85
- url: https://github.com/airbytehq/airbyte
  title: airbytehq/airbyte, GitHub repository
  trust: 0.85
- url: https://kafka.apache.org/
  title: Apache Kafka
  trust: 0.9
- url: https://parquet.apache.org/
  title: Apache Parquet
  trust: 0.9
- url: https://iceberg.apache.org/
  title: Apache Iceberg
  trust: 0.9
- url: https://delta.io/
  title: Delta Lake
  trust: 0.9
- url: https://github.com/pola-rs/polars
  title: pola-rs/polars, GitHub repository
  trust: 0.85
- url: https://docs.dask.org/en/stable/
  title: Dask documentation
  trust: 0.9
- url: https://spark.apache.org/
  title: Apache Spark
  trust: 0.9
- url: https://docs.ray.io/en/latest/data/data.html
  title: Ray Data documentation
  trust: 0.9
- url: https://github.com/HumanSignal/label-studio
  title: HumanSignal/label-studio, GitHub repository
  trust: 0.85
- url: https://github.com/great-expectations/great_expectations
  title: great-expectations/great_expectations, GitHub repository
  trust: 0.85
- url: https://github.com/unionai-oss/pandera
  title: unionai-oss/pandera, GitHub repository
  trust: 0.85
- url: https://github.com/tensorflow/data-validation
  title: tensorflow/data-validation, GitHub repository
  trust: 0.85
- url: https://github.com/treeverse/lakeFS
  title: treeverse/lakeFS, GitHub repository
  trust: 0.85
- url: https://github.com/OpenLineage/OpenLineage
  title: OpenLineage/OpenLineage, GitHub repository
  trust: 0.85
- url: https://github.com/feast-dev/feast
  title: feast-dev/feast, GitHub repository
  trust: 0.85
- url: https://docs.feast.dev/
  title: Feast documentation
  trust: 0.9
- url: https://huggingface.co/docs/datasets/stream
  title: Hugging Face Datasets documentation, streaming
  trust: 0.9
- url: https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html
  title: Hidden Technical Debt in Machine Learning Systems
  trust: 0.95
---

## Overview

An ML data pipeline turns source data into datasets a training run can name and reproduce. An orchestrator drives ingestion into an open storage format, processing, and optional human labelling.

Each batch is validated, versioned and recorded in lineage before release. Training jobs then stream it through a data loader, and features shared with online models come from a feature store.
