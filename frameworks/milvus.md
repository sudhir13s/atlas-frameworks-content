---
id: framework/milvus
type: framework
slug: milvus
schema_version: 1.1
title: Milvus
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: Cloud-native vector database for scalable similarity search
description: Open-source vector database built for billion-scale vector similarity search. Cloud-native architecture with separation of storage and compute. Supports multiple index types (HNSW, IVF, DiskANN) and GPU-accelerated search.
best_for: Billion-scale vector search, enterprise deployments
not_ideal_for: Small projects, simple prototyping, lightweight deployments
key_features:
- Billion-scale vector search
- Multiple index types (HNSW, IVF, DiskANN)
- GPU-accelerated search
- Cloud-native architecture
- Hybrid search (vector + scalar)
- Multi-vector search
- Milvus Lite for embedded use
use_cases:
- Billion-scale similarity search
- Enterprise RAG at scale
- Recommendation systems
- Image/video similarity search
pros:
- Best scale — handles billions of vectors
- Multiple index types for different tradeoffs
- GPU acceleration for search
- Milvus Lite for development
cons:
- Complex deployment (requires etcd, MinIO, Pulsar)
- Heavy infrastructure for small use cases
- Steeper learning curve
language: Go
languages_supported:
- Python
- Go
- Java
- Node.js
maintained_by: Zilliz
first_release: '2019-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/milvus-io/milvus
docs_url: https://milvus.io/docs
website_url: https://milvus.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Zilliz
  - LF AI & Data Foundation
  funding_or_parent: Created by Zilliz (Series B $60M led by Hillhouse 2022); graduated LF AI & Data project
alternatives:
- framework/qdrant
- framework/weaviate
- framework/pinecone
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 46707
  downloads_monthly: 1500000
  latest_version: 3.0.6
  latest_release_date: '2026-11-11'
  observed_at: '2026-11-20'
  source: https://github.com/milvus-io/milvus
aliases:
- milvus-io/milvus
tags:
- vector-db
- open-source
- scalable
- billion-scale
updated: '2026-11-20'
sources:
- url: https://github.com/milvus-io/milvus
  title: GitHub repository
- url: https://milvus.io/docs
  title: Documentation
---

## Overview

Open-source vector database built for billion-scale vector similarity search. Cloud-native architecture with separation of storage and compute. Supports multiple index types (HNSW, IVF, DiskANN) and GPU-accelerated search.
