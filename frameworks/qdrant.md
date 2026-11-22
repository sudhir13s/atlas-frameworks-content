---
id: framework/qdrant
type: framework
slug: qdrant
schema_version: 1.1
title: Qdrant
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: Vector Database and Vector Search Engine.
description: Qdrant is a vector similarity search engine and vector database written in Rust. It stores points, which are vectors with a JSON payload, and searches them through REST and gRPC APIs with payload filtering, dense, sparse and multivector search, hybrid queries, quantization and distributed deployment. It runs self-hosted, in Qdrant Cloud, or inside an application process as Qdrant Edge.
best_for: Vector search with payload filtering, Semantic search and recommendations
key_features:
- Filtering on JSON payload
- Dense, sparse and multivector search
- Hybrid queries with rank fusion
- Vector quantization and on-disk storage
- Sharding and replication
- REST and gRPC APIs
- Qdrant Edge for in-process search
use_cases:
- Semantic text and image search
- Recommendation
- Faceted search
- On-device search with Qdrant Edge
pros:
- Official clients for Python, JavaScript/TypeScript, Rust, Go, Java and .NET
- Self-hosted, managed cloud or embedded deployment
- GPU-accelerated indexing on NVIDIA and AMD GPUs through Vulkan
cons:
- GPU support is not included in the default binary
language: Rust
languages_supported:
- Python
- JavaScript
- Rust
- Go
- Java
- C#
maintained_by: Qdrant Solutions
license_spdx: Apache-2.0
github_url: https://github.com/qdrant/qdrant
docs_url: https://qdrant.tech/documentation/
website_url: https://qdrant.tech/
maturity: production
backing:
  type: corporate
  orgs:
  - Qdrant Solutions
alternatives:
- framework/milvus
- framework/weaviate
- framework/pinecone
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 35644
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
updated: '2026-11-21'
sources:
- url: https://github.com/qdrant/qdrant
  title: GitHub repository
- url: https://qdrant.tech/documentation/
  title: Documentation
- url: https://qdrant.tech/documentation/ops-configuration/running-with-gpu/
  title: Running with GPU
- url: https://qdrant.tech/documentation/ecosystem/
  title: Ecosystem
- url: https://qdrant.tech/
  title: Website
---

## Overview

Qdrant is a vector similarity search engine and vector database written in Rust. It stores points, which are vectors with a JSON payload, and searches them through REST and gRPC APIs with payload filtering, dense, sparse and multivector search, hybrid queries, quantization and distributed deployment. It runs self-hosted, in Qdrant Cloud, or inside an application process as Qdrant Edge.
