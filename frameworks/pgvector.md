---
id: framework/pgvector
type: framework
slug: pgvector
schema_version: 3.0
title: pgvector
status: curated
kind: tool
category: framework-category/vector-dbs
subcategory: database-extension
tagline: Open-source vector similarity search for Postgres.
description: pgvector is a Postgres extension, written in C, that stores vectors in table columns next to the rest of your data and searches them with SQL. It runs exact nearest neighbour search by default and approximate search with HNSW or IVFFlat indexes, over single-precision, half-precision, binary and sparse vectors. In a RAG system it is the store that holds chunk embeddings and returns the nearest rows to a query vector.
best_for: Vector search inside an existing Postgres database, Combining vector search with SQL filters and joins
key_features:
- Exact and approximate nearest neighbour search
- HNSW and IVFFlat indexes
- Single-precision, half-precision, binary and sparse vectors
- L2, inner product, cosine, L1, Hamming and Jaccard distances
- Filtering with SQL WHERE clauses and iterative index scans
- Hybrid search with Postgres full-text search
- Binary quantization for indexes
use_cases:
- Semantic search over rows in Postgres
- Retrieval for RAG applications
- Hybrid keyword and vector search
- Multitenant vector search with partitioning
pros:
- Usable from any language with a Postgres client
- ACID compliance, point-in-time recovery and JOINs from Postgres
- Preinstalled with Postgres.app and offered by many hosted Postgres providers
cons:
- With approximate indexes, filtering is applied after the index is scanned, so filtered queries can return fewer results unless iterative index scans are enabled
- The HNSW index supports vectors of up to 2,000 dimensions with the vector type
language: C
languages_supported:
- SQL
maintained_by: pgvector
license_spdx: PostgreSQL
github_url: https://github.com/pgvector/pgvector
docs_url: https://github.com/pgvector/pgvector#readme
registry_signals:
  github_stars: 23794
  latest_version: 0.8.7
  observed_at: '2026-11-24'
  source: https://github.com/pgvector/pgvector
aliases:
- pgvector/pgvector
tags:
- approximate-nearest-neighbor-search
- nearest-neighbor-search
updated: '2026-11-24'
sources:
- url: https://github.com/pgvector/pgvector
  title: GitHub repository
- url: https://raw.githubusercontent.com/pgvector/pgvector/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/pgvector/pgvector/HEAD/LICENSE
  title: LICENSE
---


