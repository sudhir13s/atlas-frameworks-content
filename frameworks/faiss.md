---
id: framework/faiss
type: framework
slug: faiss
schema_version: 1.1
title: FAISS
kind: library
category: framework-category/vector-dbs
subcategory: search-library
tagline: Facebook AI Similarity Search — efficient similarity search and clustering of dense vectors
description: Meta AI's library for efficient similarity search and clustering of dense vectors. Not a database but a search library. Provides the fastest vector search algorithms available, often used as the engine inside other vector databases.
best_for: Building custom high-performance vector search systems
not_ideal_for: Applications needing a full database with persistence and filtering
key_features:
- Multiple index types (flat, IVF, HNSW, PQ)
- GPU-accelerated search
- Billion-scale indexing
- Product quantization for compression
- Composable index factory
use_cases:
- High-performance vector search
- Embedding similarity search
- Building custom vector search systems
pros:
- Fastest vector search library
- GPU acceleration
- Battle-tested at Meta scale
- Highly configurable index types
cons:
- Library, not a database — no persistence, CRUD, or filtering
- Complex to tune for optimal performance
- No built-in metadata handling
language: C++
languages_supported:
- C++
- Python
maintained_by: Meta AI Research
first_release: '2017-03-01'
license_spdx: MIT
github_url: https://github.com/facebookresearch/faiss
docs_url: https://faiss.ai/
website_url: https://faiss.ai/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Meta
  funding_or_parent: Meta AI Research (FAIR)
ecosystem_connections:
- framework/pytorch
- framework/langchain
registry_signals:
  github_stars: 32000
  downloads_monthly: 5000000
  latest_version: '1.9'
  latest_release_date: '2025-01-15'
  observed_at: '2026-06-15'
  source: https://github.com/facebookresearch/faiss
aliases:
- facebookresearch/faiss
tags:
- vector-db
- search-library
- high-performance
- gpu
updated: '2026-11-19'
sources:
- url: https://github.com/facebookresearch/faiss
  title: GitHub repository
- url: https://faiss.ai/
  title: Documentation
---

## Overview

Meta AI's library for efficient similarity search and clustering of dense vectors. Not a database but a search library. Provides the fastest vector search algorithms available, often used as the engine inside other vector databases.
