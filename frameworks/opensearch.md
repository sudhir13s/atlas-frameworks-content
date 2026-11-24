---
id: framework/opensearch
type: framework
slug: opensearch
schema_version: 3.0
title: OpenSearch
status: curated
kind: tool
category: framework-category/search-engines
subcategory: search-engine
tagline: Open source distributed and RESTful search engine.
description: OpenSearch is an open-source search and observability suite, a distributed RESTful search engine built on the Apache Lucene library. It indexes documents and answers full-text queries scored with Okapi BM25 by default, k-NN vector queries, neural sparse queries and hybrid queries that normalize and combine keyword and semantic results into one ranking. In a document-to-answer path it is the retrieval store, with search pipelines that can filter vector results and rerank hits before they reach the application.
best_for: Self-hosted full-text and vector search, Hybrid keyword and semantic retrieval, Search and log analytics
key_features:
- Full-text queries with Okapi BM25 scoring by default
- k-NN vector search with filtering during or after the search
- Hybrid search with score-based normalization or reciprocal rank fusion
- Neural sparse search on an inverted index
- Reranking through a rerank search processor, including cross-encoder models
- Search pipelines that process results at search time
- Distributed RESTful engine built on Apache Lucene
use_cases:
- Keyword and semantic search for applications
- Retrieval for RAG
- Log and observability analytics
pros:
- Apache 2.0 licence
- Score-based or rank-based hybrid combination per request or per pipeline
language: Java
languages_supported:
- Java
maintained_by: OpenSearch Contributors
license_spdx: Apache-2.0
github_url: https://github.com/opensearch-project/OpenSearch
docs_url: https://docs.opensearch.org/
website_url: https://opensearch.org/
registry_signals:
  github_stars: 14064
  latest_version: 3.10.0
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-24'
  source: https://github.com/opensearch-project/OpenSearch
aliases:
- opensearch-project/OpenSearch
tags:
- search
- search-engine
- analytics
- java
- foss
- apache2
updated: '2026-11-24'
sources:
- url: https://github.com/opensearch-project/OpenSearch
  title: GitHub repository
- url: https://raw.githubusercontent.com/opensearch-project/OpenSearch/HEAD/README.md
  title: README
- url: https://github.com/opensearch-project/OpenSearch/releases/latest
  title: Latest release
- url: https://docs.opensearch.org/latest/vector-search/ai-search/hybrid-search/index/
  title: Hybrid search
- url: https://docs.opensearch.org/latest/search-plugins/keyword-search/
  title: Keyword search
- url: https://docs.opensearch.org/latest/query-dsl/full-text/index/
  title: Full-text queries
- url: https://docs.opensearch.org/latest/vector-search/ai-search/neural-sparse-search/
  title: Neural sparse search
- url: https://docs.opensearch.org/latest/search-plugins/search-relevance/reranking-search-results/
  title: Reranking search results
- url: https://docs.opensearch.org/latest/vector-search/filter-search-knn/index/
  title: Filtering data
---


