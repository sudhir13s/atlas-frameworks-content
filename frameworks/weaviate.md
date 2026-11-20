---
id: framework/weaviate
type: framework
slug: weaviate
schema_version: 1.1
title: Weaviate
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: Open-source AI-native vector database with built-in modules
description: Open-source vector database with built-in vectorization modules, hybrid search, and generative modules. Can automatically vectorize data using integrated ML models. Supports both self-hosted and cloud deployment.
best_for: Enterprise vector search with built-in ML integration
not_ideal_for: Simple prototyping (use ChromaDB), extremely cost-sensitive projects
key_features:
- Built-in vectorization modules
- Hybrid search (vector + keyword)
- Generative search (RAG built-in)
- Multi-tenancy
- GraphQL and REST APIs
- Horizontal scaling
use_cases:
- Semantic search with auto-vectorization
- Enterprise RAG applications
- Knowledge management systems
pros:
- Built-in vectorization reduces complexity
- Good hybrid search
- Strong multi-tenancy support
- Both self-hosted and cloud
cons:
- More complex than ChromaDB for simple use cases
- Resource-intensive for small deployments
- Weaviate Cloud can be expensive
language: Go
languages_supported:
- Python
- JavaScript
- Go
- Java
maintained_by: Weaviate B.V.
first_release: '2019-01-01'
license_spdx: BSD-3-Clause
github_url: https://github.com/weaviate/weaviate
docs_url: https://weaviate.io/developers/weaviate
website_url: https://weaviate.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Weaviate B.V.
  funding_or_parent: Series B $50M led by Index Ventures (2023)
alternatives:
- framework/qdrant
- framework/milvus
- framework/pinecone
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 16956
  downloads_monthly: 1000000
  latest_version: 1.40.7
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/weaviate/weaviate
aliases:
- weaviate/weaviate
tags:
- vector-db
- open-source
- enterprise
- hybrid-search
updated: '2026-11-20'
sources:
- url: https://github.com/weaviate/weaviate
  title: GitHub repository
- url: https://weaviate.io/developers/weaviate
  title: Documentation
---

## Overview

Open-source vector database with built-in vectorization modules, hybrid search, and generative modules. Can automatically vectorize data using integrated ML models. Supports both self-hosted and cloud deployment.
