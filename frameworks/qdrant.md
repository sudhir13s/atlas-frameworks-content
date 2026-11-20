---
id: framework/qdrant
type: framework
slug: qdrant
schema_version: 1.1
title: Qdrant
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: High-performance vector similarity search engine with filtering
description: Vector similarity search engine written in Rust for maximum performance. Features advanced filtering, payload storage, and distributed deployment. Good balance of performance, features, and operational simplicity.
best_for: Production vector search with strong filtering needs
not_ideal_for: Billion-scale deployments (Milvus may be better)
key_features:
- Rust performance
- Advanced filtering on payload
- Multi-vector support
- Distributed deployment
- Quantization (scalar, product)
- Hybrid search
- Single-binary deployment
use_cases:
- Production vector search
- RAG applications with complex filtering
- Recommendation systems
pros:
- Excellent performance (Rust)
- Simple deployment (single binary)
- Good filtering capabilities
- Active development
cons:
- Newer — less battle-tested than Milvus at extreme scale
- Cloud offering less mature than Pinecone
language: Rust
languages_supported:
- Python
- JavaScript
- Rust
- Go
- Java
maintained_by: Qdrant Solutions
first_release: '2021-05-01'
license_spdx: Apache-2.0
github_url: https://github.com/qdrant/qdrant
docs_url: https://qdrant.tech/documentation/
website_url: https://qdrant.tech/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Qdrant Solutions
  funding_or_parent: Series A $28M led by Spark Capital (2024)
alternatives:
- framework/milvus
- framework/weaviate
- framework/pinecone
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 35642
  downloads_monthly: 1500000
  latest_version: 1.20.2
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-20'
  source: https://github.com/qdrant/qdrant
aliases:
- qdrant/qdrant
tags:
- vector-db
- open-source
- rust
- high-performance
updated: '2026-11-20'
sources:
- url: https://github.com/qdrant/qdrant
  title: GitHub repository
- url: https://qdrant.tech/documentation/
  title: Documentation
---

## Overview

Vector similarity search engine written in Rust for maximum performance. Features advanced filtering, payload storage, and distributed deployment. Good balance of performance, features, and operational simplicity.
