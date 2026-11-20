---
id: framework/chromadb
type: framework
slug: chromadb
schema_version: 1.1
title: ChromaDB
kind: tool
category: framework-category/vector-dbs
subcategory: embedded
tagline: The AI-native open-source embedding database
description: Lightweight, open-source embedding database designed for AI applications. Runs embedded in Python with no server required. Simple API for storing and querying embeddings. The easiest vector database to get started with.
best_for: Local development, prototyping RAG apps, personal projects
not_ideal_for: Large-scale production (millions of vectors), multi-tenant SaaS
key_features:
- Embedded mode (no server needed)
- Client-server mode for production
- Automatic embedding generation
- Metadata filtering
- Multi-modal support
- Simple Python and JS APIs
use_cases:
- Local RAG applications
- Prototype vector search
- Personal AI projects
- Development and testing
pros:
- Simplest setup — pip install and go
- Good for prototyping and local development
- Clean API
- No infrastructure needed
cons:
- Not designed for massive scale
- Performance limitations vs. dedicated solutions
- Limited production features compared to Milvus/Qdrant
language: Python
languages_supported:
- Python
- JavaScript
maintained_by: Chroma Inc.
first_release: '2022-10-01'
license_spdx: Apache-2.0
github_url: https://github.com/chroma-core/chroma
docs_url: https://docs.trychroma.com/
website_url: https://www.trychroma.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: very-low
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Chroma
  funding_or_parent: Seed $18M led by Astasia Myers / Quiet Capital (2023)
alternatives:
- framework/qdrant
- framework/weaviate
- framework/milvus
ecosystem_connections:
- framework/langchain
- framework/llamaindex
- framework/sentence-transformers
registry_signals:
  github_stars: 29716
  downloads_monthly: 8666293
  latest_version: 1.5.9
  latest_release_date: '2026-05-05'
  observed_at: '2026-11-20'
  source: https://github.com/chroma-core/chroma
aliases:
- chroma-core/chroma
tags:
- vector-db
- embedded
- rag
- simple
- local
updated: '2026-11-20'
sources:
- url: https://github.com/chroma-core/chroma
  title: GitHub repository
- url: https://docs.trychroma.com/
  title: Documentation
---

## Overview

Lightweight, open-source embedding database designed for AI applications. Runs embedded in Python with no server required. Simple API for storing and querying embeddings. The easiest vector database to get started with.
