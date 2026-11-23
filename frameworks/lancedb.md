---
id: framework/lancedb
type: framework
slug: lancedb
schema_version: 3.0
title: LanceDB
status: curated
kind: tool
category: framework-category/vector-dbs
subcategory: embedded
tagline: OSS embedded retrieval library for multimodal AI.
description: LanceDB is an open-source retrieval library built on the Lance columnar format that runs inside your application, with data on local disk or in object storage. It supports vector similarity search, full-text search and SQL over vectors, metadata and multimodal data such as text, images and video.
best_for: Retrieval that runs inside the application process, Multimodal search by keyword or vector or SQL
not_ideal_for: Distributed search and indexing (offered by the separate LanceDB Enterprise product)
key_features:
- Runs in the application process (LanceDB Embedded)
- Built on the Lance columnar format
- Multimodal data support (text, images, videos, point clouds)
- Vector similarity search, full-text search and SQL
- Automatic data versioning
- Object storage backends (S3, Google Cloud Storage, Azure Blob Storage)
- GPU-accelerated vector index building (CUDA, Apple MPS)
use_cases:
- Multimodal search
- Retrieval inside an application
- Pinning and revisiting versions of a dataset
pros:
- No separate server process
- Data versioning built in
- Python, TypeScript and Rust SDKs
cons:
- Automatic GPU indexing is available only in LanceDB Enterprise
language: Rust
languages_supported:
- Python
- JavaScript
- Rust
maintained_by: LanceDB
license_spdx: Apache-2.0
github_url: https://github.com/lancedb/lancedb
docs_url: https://lancedb.github.io/lancedb/
website_url: https://lancedb.com/
maturity: experimental
backing:
  type: corporate
  orgs:
  - LanceDB
alternatives:
- framework/chromadb
- framework/qdrant
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 11952
  downloads_monthly: 7013050
  latest_version: 0.41.0
  latest_release_date: '2026-10-29'
  observed_at: '2026-11-20'
  source: https://github.com/lancedb/lancedb
aliases:
- lancedb/lancedb
tags:
- vector-db
- serverless
- embedded
- multi-modal
updated: '2026-11-21'
sources:
- url: https://github.com/lancedb/lancedb
  title: GitHub repository
- url: https://lancedb.github.io/lancedb/
  title: Documentation
- url: https://docs.lancedb.com/
  title: Documentation home
- url: https://docs.lancedb.com/indexing/gpu-indexing
  title: GPU indexing
- url: https://docs.lancedb.com/storage
  title: Storage
- url: https://pypi.org/project/lancedb/
  title: lancedb — PyPI
---


