---
id: framework/milvus
type: framework
slug: milvus
schema_version: 1.1
title: Milvus
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: Milvus is a cloud-native vector database built for scalable vector ANN search.
description: Milvus is an open-source vector database written in Go and C++ for organizing and searching unstructured data such as text, images and multi-modal information. It has a distributed, Kubernetes-native architecture that separates compute and storage, and also runs as a single-machine Standalone server or as Milvus Lite, a Python library. The project is hosted by the LF AI & Data Foundation, with Zilliz as its major contributor.
best_for: Vector search at scale on Kubernetes, Hybrid search combining dense vectors and full-text search
key_features:
- Distributed architecture with separate compute and storage
- Deployment modes (Milvus Lite, Standalone, Distributed)
- Index types including HNSW, IVF, FLAT, SCANN and DiskANN
- GPU indexing such as NVIDIA CAGRA
- Metadata filtering and range search
- Full-text search with BM25 and sparse vectors
- Hybrid search with reranking
- Multi-tenancy and hot/cold storage
- Authentication, TLS encryption and role-based access control
use_cases:
- Retrieval-augmented generation (RAG)
- Text and image search
- Recommendation systems
- Hybrid search
pros:
- Same client API from Milvus Lite to a distributed cluster
- Choice of index types for different scenarios
- Official SDKs in several languages
language: Go
languages_supported:
- Python
- Go
- Java
- Node.js
- C++
maintained_by: LF AI & Data Foundation (Zilliz is the major contributor)
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
backing:
  type: foundation
  orgs:
  - LF AI & Data Foundation
  - Zilliz
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
updated: '2026-11-21'
sources:
- url: https://github.com/milvus-io/milvus
  title: GitHub repository
- url: https://milvus.io/docs
  title: Documentation
- url: https://milvus.io/docs/overview.md
  title: What is Milvus
- url: https://pypi.org/project/pymilvus/
  title: pymilvus — PyPI
---

## Overview

Milvus is an open-source vector database written in Go and C++ for organizing and searching unstructured data such as text, images and multi-modal information. It has a distributed, Kubernetes-native architecture that separates compute and storage, and also runs as a single-machine Standalone server or as Milvus Lite, a Python library. The project is hosted by the LF AI & Data Foundation, with Zilliz as its major contributor.
