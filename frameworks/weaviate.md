---
id: framework/weaviate
type: framework
slug: weaviate
schema_version: 1.1
title: Weaviate
kind: tool
category: framework-category/vector-dbs
subcategory: self-hosted
tagline: Open-source vector database that stores both objects and vectors, combining vector search with structured filtering.
description: Weaviate is an open-source, cloud-native vector database that stores both objects and vectors. It combines vector similarity search with keyword filtering, retrieval-augmented generation (RAG) and reranking in a single query interface. Vectors can be created at import time by integrated model providers or imported as pre-computed embeddings, and it runs self-hosted with Docker or Kubernetes or as Weaviate Cloud.
best_for: Semantic and hybrid search, Retrieval-augmented generation backends
key_features:
- Automatic vectorization with integrated model providers
- Hybrid search combining vectors and BM25 keyword search
- Generative search (RAG) and reranking
- Multi-tenancy, replication and role-based access control
- Horizontal scaling
- Vector compression
- REST, gRPC and GraphQL APIs
use_cases:
- Semantic and image search
- RAG applications
- Recommendation engines
- Chatbots
pros:
- Vectorization at import or bring-your-own embeddings
- Self-hosted or managed cloud deployment
- Client libraries for several languages
cons:
- The GraphQL API is deprecated
- Code in the wl directory is under a commercial licence and enterprise features need a licence key
language: Go
languages_supported:
- Python
- JavaScript
- Go
- Java
- C#
maintained_by: Weaviate B.V.
github_url: https://github.com/weaviate/weaviate
docs_url: https://docs.weaviate.io/weaviate
website_url: https://weaviate.io/
maturity: production
backing:
  type: corporate
  orgs:
  - Weaviate B.V.
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
updated: '2026-11-21'
sources:
- url: https://github.com/weaviate/weaviate
  title: GitHub repository
- url: https://docs.weaviate.io/weaviate
  title: Documentation
- url: https://docs.weaviate.io/weaviate/model-providers/transformers/embeddings
  title: Locally hosted Transformers embeddings
license_note: BSD-3-Clause outside the wl directory; code in the wl directory is under a separate Weaviate enterprise licence
---

## Overview

Weaviate is an open-source, cloud-native vector database that stores both objects and vectors. It combines vector similarity search with keyword filtering, retrieval-augmented generation (RAG) and reranking in a single query interface. Vectors can be created at import time by integrated model providers or imported as pre-computed embeddings, and it runs self-hosted with Docker or Kubernetes or as Weaviate Cloud.
