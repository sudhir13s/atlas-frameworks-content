---
id: framework/vespa
type: framework
slug: vespa
schema_version: 3.0
title: Vespa
status: curated
kind: tool
category: framework-category/search-engines
subcategory: search-engine
tagline: The AI search platform.
description: Vespa is a platform to search, make inferences in and organize vectors, tensors, text and structured data at serving time. It selects a subset of a large, continuously changing corpus, evaluates machine-learned ranking models over the selected data and returns organized results, with data distributed over multiple nodes. In a document-to-answer path it is the retrieval and ranking layer, combining BM25 text matching, nearest-neighbor search with filters, reciprocal rank fusion and phased re-ranking such as cross-encoders.
best_for: Search and recommendation with machine-learned ranking, Hybrid lexical and vector retrieval, Large distributed corpora
key_features:
- bm25 rank feature implementing Okapi BM25
- Nearest-neighbor search constrained by query filters
- Hybrid queries combining weakAnd and nearestNeighbor operators
- reciprocal_rank_fusion ranking function
- Phased ranking with first-phase, second-phase and global-phase expressions
- Re-ranking with cross-encoders
- Tensors and machine-learned model evaluation at serving time
- Distribution over multiple nodes
use_cases:
- Search
- Recommendation and personalization
- Retrieval for RAG
pros:
- Runs self-hosted or on the Vespa Cloud service
- Custom Java components in applications
- New releases from the master branch Monday through Thursday
language: Java
languages_supported:
- Java
maintained_by: Vespa.ai
license_spdx: Apache-2.0
github_url: https://github.com/vespa-engine/vespa
docs_url: https://docs.vespa.ai
website_url: https://vespa.ai
registry_signals:
  github_stars: 7198
  latest_version: 8.788.13
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-24'
  source: https://github.com/vespa-engine/vespa
aliases:
- vespa-engine/vespa
tags:
- search-engine
- vector-search
- vector-database
- rag
- tensor
- serving-recommendation
- machine-learning
- java
updated: '2026-11-24'
sources:
- url: https://github.com/vespa-engine/vespa
  title: GitHub repository
- url: https://raw.githubusercontent.com/vespa-engine/vespa/HEAD/README.md
  title: README
- url: https://github.com/vespa-engine/vespa/releases/latest
  title: Latest release
- url: https://docs.vespa.ai/en/learn/tutorials/hybrid-search.html
  title: Hybrid search tutorial
- url: https://docs.vespa.ai/en/ranking/bm25.html
  title: The BM25 rank feature
- url: https://docs.vespa.ai/en/ranking/phased-ranking.html
  title: Phased ranking
- url: https://docs.vespa.ai/en/querying/nearest-neighbor-search-guide.html
  title: Nearest neighbor search guide
---


