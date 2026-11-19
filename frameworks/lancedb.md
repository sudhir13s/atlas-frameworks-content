---
id: framework/lancedb
type: framework
slug: lancedb
schema_version: 1.1
title: LanceDB
kind: tool
category: framework-category/vector-dbs
subcategory: embedded
tagline: Serverless vector database for AI applications — embedded, open-source
description: Serverless vector database built on the Lance columnar format. Runs embedded with zero infrastructure. Supports multi-modal data (text, images, video), full-text search, and integrates with data ecosystem tools.
best_for: Serverless vector search, multi-modal applications
not_ideal_for: Enterprise-scale production (use Milvus/Qdrant)
key_features:
- Serverless — no server process needed
- Lance columnar format (fast, versioned)
- Multi-modal support
- Full-text search + vector search
- Automatic versioning
- S3/GCS/Azure storage backends
use_cases:
- Serverless RAG applications
- Multi-modal search
- Data versioning with vector search
pros:
- Zero infrastructure — embedded like SQLite
- Multi-modal native
- Data versioning built-in
- Fast columnar format
cons:
- Newer — less battle-tested
- Smaller community
- Scaling story still developing
language: Rust
languages_supported:
- Python
- JavaScript
- Rust
maintained_by: LanceDB Inc.
first_release: '2023-02-01'
license_spdx: Apache-2.0
github_url: https://github.com/lancedb/lancedb
docs_url: https://lancedb.github.io/lancedb/
website_url: https://lancedb.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: small-medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - LanceDB Inc
  funding_or_parent: Seed $8M led by CRV (2023)
alternatives:
- framework/chromadb
- framework/qdrant
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 5500
  downloads_monthly: 500000
  latest_version: '0.15'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/lancedb/lancedb
aliases:
- lancedb/lancedb
tags:
- vector-db
- serverless
- embedded
- multi-modal
updated: '2026-11-19'
sources:
- url: https://github.com/lancedb/lancedb
  title: GitHub repository
- url: https://lancedb.github.io/lancedb/
  title: Documentation
---

## Overview

Serverless vector database built on the Lance columnar format. Runs embedded with zero infrastructure. Supports multi-modal data (text, images, video), full-text search, and integrates with data ecosystem tools.
