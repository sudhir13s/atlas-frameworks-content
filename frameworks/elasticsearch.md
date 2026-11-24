---
id: framework/elasticsearch
type: framework
slug: elasticsearch
schema_version: 3.0
title: Elasticsearch
status: curated
kind: tool
category: framework-category/search-engines
subcategory: search-engine
tagline: Free and Open Source, Distributed, RESTful Search Engine.
description: Elasticsearch is a distributed search and analytics engine, scalable data store and vector database, and the foundation of Elastic's Stack platform. It analyzes and indexes documents for full-text (lexical) search, stores dense and sparse vectors for semantic search, and returns one ranked list from hybrid queries that it recommends combining with reciprocal rank fusion. In a document-to-answer path it is the retrieval store, with filtered kNN search and semantic re-rankers that reorder a small top-k result set before generation.
best_for: Full-text, vector and hybrid search at production scale, Retrieval for RAG, Log and metrics analytics
key_features:
- Full-text (lexical) search on analyzed text fields with BM25
- Approximate and exact kNN vector search
- Filtered approximate kNN search
- Hybrid search combined with reciprocal rank fusion (RRF)
- Sparse vector search with the Elastic Learned Sparse Encoder (ELSER)
- Semantic re-ranking of top-k results
- Distributed RESTful API with language clients
use_cases:
- Retrieval augmented generation (RAG)
- Vector search
- Full-text search
- Logs, metrics and application performance monitoring
- Security logs
pros:
- Managed service on Elastic Cloud or self-managed download
- Full-text search runs on CPUs
- Local Docker setup with the start-local script
cons:
- The start-local setup is for local development and testing only
language: Java
languages_supported:
- Java
maintained_by: Elastic
license_note: The default throughout the repository is a triple license under the "GNU Affero General Public License v3.0 only", "the Server Side Public License, v 1", and the "Elastic License 2.0", unless the header specifies another license. Code that is licensed solely under the "Elastic License 2.0" is found only in the x-pack folder.
github_url: https://github.com/elastic/elasticsearch
website_url: https://www.elastic.co/products/elasticsearch
backing:
  type: corporate
  orgs:
  - Elastic
registry_signals:
  github_stars: 78719
  latest_version: 9.5.7
  latest_release_date: '2026-11-23'
  observed_at: '2026-11-24'
  source: https://github.com/elastic/elasticsearch
aliases:
- elastic/elasticsearch
tags:
- elasticsearch
- search-engine
- java
updated: '2026-11-24'
sources:
- url: https://github.com/elastic/elasticsearch
  title: GitHub repository
- url: https://raw.githubusercontent.com/elastic/elasticsearch/HEAD/README.asciidoc
  title: README
- url: https://raw.githubusercontent.com/elastic/elasticsearch/HEAD/LICENSE.txt
  title: LICENSE
- url: https://github.com/elastic/elasticsearch/releases/latest
  title: Latest release
- url: https://www.elastic.co/docs/solutions/search/hybrid-search
  title: Hybrid search
- url: https://www.elastic.co/docs/solutions/search/full-text
  title: Full-text search
- url: https://www.elastic.co/docs/solutions/search/vector/knn/filtered-knn-search
  title: Filter approximate kNN results
- url: https://www.elastic.co/docs/solutions/search/vector/sparse-vector
  title: Sparse vector search
- url: https://www.elastic.co/docs/solutions/search/ranking/semantic-reranking
  title: Semantic reranking
---


