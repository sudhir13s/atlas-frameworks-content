---
id: framework/faiss
type: framework
slug: faiss
schema_version: 1.1
title: Faiss
kind: library
category: framework-category/vector-dbs
subcategory: search-library
tagline: A library for efficient similarity search and clustering of dense vectors.
description: Faiss is a library for efficient similarity search and clustering of dense vectors, including vector sets that may not fit in RAM. It is written in C++ with complete wrappers for Python/numpy, and some of its algorithms are implemented on the GPU. It is developed primarily at Meta's Fundamental AI Research group.
best_for: Similarity search over dense vectors, Clustering dense vectors
key_features:
- Multiple index types (flat, IVF, HNSW, PQ)
- GPU-accelerated search
- Search in vector sets that may not fit in RAM
- Product quantization for compression
- Composable index factory
use_cases:
- Vector similarity search
- Embedding similarity search
- Clustering dense vectors
pros:
- Optional GPU support through CUDA or AMD ROCm
- Index types trade off search time, search quality and memory
language: C++
languages_supported:
- C++
- Python
maintained_by: Meta Fundamental AI Research
license_spdx: MIT
github_url: https://github.com/facebookresearch/faiss
docs_url: https://faiss.ai/
website_url: https://faiss.ai/
backing:
  type: corporate
  orgs:
  - Meta
registry_signals:
  github_stars: 41831
  downloads_monthly: 5000000
  latest_version: '1.9'
  latest_release_date: '2025-01-15'
  observed_at: '2026-11-20'
  source: https://github.com/facebookresearch/faiss
aliases:
- facebookresearch/faiss
- FAISS
tags:
- vector-db
- search-library
- high-performance
- gpu
updated: '2026-11-21'
sources:
- url: https://github.com/facebookresearch/faiss
  title: GitHub repository
- url: https://faiss.ai/
  title: Documentation
- url: https://github.com/facebookresearch/faiss/wiki/The-index-factory
  title: Faiss wiki — The index factory
- url: https://pypi.org/project/faiss-cpu/
  title: faiss-cpu — PyPI
---

## Overview

Faiss is a library for efficient similarity search and clustering of dense vectors, including vector sets that may not fit in RAM. It is written in C++ with complete wrappers for Python/numpy, and some of its algorithms are implemented on the GPU. It is developed primarily at Meta's Fundamental AI Research group.
