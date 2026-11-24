---
id: framework/tantivy
type: framework
slug: tantivy
schema_version: 3.0
title: Tantivy
status: curated
kind: library
category: framework-category/search-engines
subcategory: search-library
tagline: Fast full-text search engine library written in Rust.
description: Tantivy is a full-text search engine library written in Rust and inspired by Apache Lucene. It is not an off-the-shelf search server but a crate for building one; it indexes documents with text, numeric, date, IP, boolean, facet and JSON fields and returns matching documents ranked with BM25 scoring. It provides the keyword retrieval step inside an application, with Python bindings in tantivy-py.
best_for: Embedding full-text search in Rust applications, Building a custom search engine
key_features:
- BM25 scoring, the same as Lucene
- Natural query language with boolean and phrase queries
- Configurable tokenizers with stemming for 17 Latin languages
- Incremental and multithreaded indexing
- Range queries and faceted search
- JSON fields and fast fields
- Aggregations for histograms, range buckets and stats
- Compressed document store
use_cases:
- Full-text search inside an application
- Command-line search tools
- Building a search server
pros:
- Startup time under 10 ms
- Runs on stable Rust on Linux, macOS and Windows
- Python bindings through tantivy-py
cons:
- Distributed search is out of scope
- Data is immutable; editing a document means deleting and reindexing it
language: Rust
languages_supported:
- Rust
- Python
maintained_by: quickwit-oss
license_spdx: MIT
github_url: https://github.com/quickwit-oss/tantivy
docs_url: https://docs.rs/tantivy/
registry_signals:
  github_stars: 16469
  latest_version: 0.27.0
  latest_release_date: '2026-10-17'
  observed_at: '2026-11-24'
  source: https://github.com/quickwit-oss/tantivy
aliases:
- quickwit-oss/tantivy
tags:
- rust
- search-engine
updated: '2026-11-24'
sources:
- url: https://github.com/quickwit-oss/tantivy
  title: GitHub repository
- url: https://raw.githubusercontent.com/quickwit-oss/tantivy/HEAD/README.md
  title: README
- url: https://crates.io/api/v1/crates/tantivy
  title: tantivy — crates.io
---


