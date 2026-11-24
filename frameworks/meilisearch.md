---
id: framework/meilisearch
type: framework
slug: meilisearch
schema_version: 3.0
title: Meilisearch
status: curated
kind: tool
category: framework-category/search-engines
subcategory: search-engine
tagline: A lightning-fast search engine API bringing AI-powered hybrid search to your sites and applications.
description: Meilisearch is a search engine for full-text, semantic and hybrid search, run self-hosted as a single binary or as the managed Meilisearch Cloud. It takes JSON documents over a RESTful API and returns ranked results with typo tolerance, filters, facets and sorting; hybrid search combines keyword matching with semantic matching, balanced by a semanticRatio parameter. In a document-to-answer path it is the retrieval layer, usable as a LangChain vector store or through its MCP server.
best_for: Search-as-you-type for sites and apps, Hybrid keyword and semantic search, Faceted search
key_features:
- Full-text search with typo tolerance
- Hybrid and semantic search with a semanticRatio parameter
- Filtering and faceted search
- Sorting and geosearch
- Synonyms and multi-language support
- Multi-tenancy with tenant tokens
- Conversational search grounded in indexed data
- Native MCP server (experimental) and LangChain vector store
use_cases:
- Site and app search
- Ecommerce search with facets
- Retrieval for AI agents and RAG
pros:
- Self-hosted single binary or managed cloud with the same API
- SDKs for JavaScript, Python, PHP, Ruby, Go and Rust
- Community Edition free for commercial use under the MIT licence
cons:
- Enterprise Edition features such as sharding are not allowed in production without a commercial agreement
- Collects anonymized usage data unless deactivated
language: Rust
languages_supported:
- JavaScript
- Python
- PHP
- Ruby
- Go
- Rust
maintained_by: Meili
license_note: 'SPDX-License-Identifier: MIT AND OpenLDAP AND BUSL-1.1'
github_url: https://github.com/meilisearch/meilisearch
docs_url: https://www.meilisearch.com/docs
website_url: https://www.meilisearch.com
backing:
  type: corporate
  orgs:
  - Meili
alternatives:
- framework/elasticsearch
- framework/typesense
- framework/opensearch
- framework/pinecone
- framework/qdrant
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 59982
  latest_version: 1.58.0
  latest_release_date: '2026-11-23'
  observed_at: '2026-11-24'
  source: https://github.com/meilisearch/meilisearch
aliases:
- meilisearch/meilisearch
tags:
- search-engine
- full-text-search
- hybrid-search
- semantic-search
- vector-search
- typo-tolerance
- faceting
- geosearch
updated: '2026-11-24'
sources:
- url: https://github.com/meilisearch/meilisearch
  title: GitHub repository
- url: https://raw.githubusercontent.com/meilisearch/meilisearch/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/meilisearch/meilisearch/HEAD/LICENSE
  title: LICENSE
- url: https://github.com/meilisearch/meilisearch/releases/latest
  title: Latest release
- url: https://www.meilisearch.com/docs/learn/experimental/vector_search
  title: Hybrid and semantic search
- url: https://www.meilisearch.com/docs/learn/fine_tuning_results/filtering
  title: Filtering
---


