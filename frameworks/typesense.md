---
id: framework/typesense
type: framework
slug: typesense
schema_version: 3.0
title: Typesense
status: curated
kind: tool
category: framework-category/search-engines
subcategory: search-engine
tagline: Typesense is a fast, typo-tolerant search engine for building delightful search experiences.
description: Typesense is a typo-tolerant, in-memory search engine written in C++ and run as a single binary or on Typesense Cloud. It indexes JSON documents and answers keyword, vector, semantic and hybrid queries, generating embeddings with built-in or external models and combining keyword and semantic results with rank fusion. In a document-to-answer path it is the retrieval layer, with filtering, faceting and a built-in conversational search (RAG) mode.
best_for: Typo-tolerant instant search, Hybrid keyword and semantic search, Faceted and geo search
key_features:
- Typo tolerance and tunable ranking
- Faceting, filtering, sorting and grouping
- Vector search on stored embeddings
- Semantic and hybrid search with built-in embedding models
- Rank Fusion of keyword and semantic results
- Conversational search (built-in RAG)
- Federated search across collections
- Raft-based clustering
use_cases:
- Site and ecommerce search
- Semantic and similarity search
- Geo search
- Question answering over indexed data
pros:
- Single binary with no runtime dependencies
- Client libraries under the Apache licence
language: C++
languages_supported:
- C++
maintained_by: Typesense
license_spdx: GPL-3.0
github_url: https://github.com/typesense/typesense
docs_url: https://typesense.org/docs/
website_url: https://typesense.org
alternatives:
- framework/elasticsearch
- framework/pinecone
registry_signals:
  github_stars: 27168
  latest_version: '30.2'
  latest_release_date: '2026-04-19'
  observed_at: '2026-11-24'
  source: https://github.com/typesense/typesense
aliases:
- typesense/typesense
tags:
- search-engine
- full-text-search
- typo-tolerance
- vector-search
- semantic-search
- faceting
- geosearch
- in-memory
updated: '2026-11-24'
sources:
- url: https://github.com/typesense/typesense
  title: GitHub repository
- url: https://raw.githubusercontent.com/typesense/typesense/HEAD/README.md
  title: README
- url: https://github.com/typesense/typesense/releases/latest
  title: Latest release
- url: https://typesense.org/docs/latest/api/vector-search.html
  title: Vector search
---


