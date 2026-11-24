---
id: framework/bm25s
type: framework
slug: bm25s
schema_version: 3.0
title: BM25S
status: curated
kind: library
category: framework-category/search-engines
subcategory: bm25-library
tagline: Fast BM25 search in Python, powered by Numpy and Numba.
description: BM25S (BM25-Sparse) is a Python library that implements BM25 to rank documents against a query, using Numpy sparse matrices that store scores computed eagerly for all document tokens at indexing time. It takes a corpus of strings or dictionaries, tokenizes and indexes it, and returns the top-k document IDs or documents with their scores. It covers the lexical retrieval step, without dependencies on Java or PyTorch, and also runs from a command line or as an MCP server.
best_for: Lexical BM25 retrieval in Python, Keyword search over a local corpus without a search server
key_features:
- BM25 variants Lucene, Robertson, ATIRE, BM25L and BM25+
- Scores precomputed into sparse matrices at indexing time
- Optional Numba backend
- Tokenizer with stopwords and stemming
- Memory-mapped index loading
- Saving and loading indices on the Hugging Face Hub
- Command-line indexing and search of CSV, TXT, JSON and JSONL files
- Built-in MCP server
use_cases:
- Keyword retrieval for RAG
- Searching a local document collection
- Exposing a BM25 index as a tool for LLM agents
pros:
- Needs only Numpy, with optional lightweight dependencies
- Default method reproduces Lucene's BM25 implementation
- Indices can be shared through the Hugging Face Hub
language: Python
languages_supported:
- Python
maintained_by: xhluca
license_spdx: MIT
github_url: https://github.com/xhluca/bm25s
website_url: https://bm25s.github.io
alternatives:
- framework/rank-bm25
- framework/elasticsearch
registry_signals:
  github_stars: 1830
  downloads_monthly: 1666531
  latest_version: 0.3.16
  latest_release_date: '2026-10-28'
  observed_at: '2026-11-24'
  source: https://github.com/xhluca/bm25s
aliases:
- xhluca/bm25s
- BM25-Sparse
tags:
- bm25
- okapi-bm25
- bm25-plus
- lexical-search
- information-retrieval
- retrieval
- rag
- search
updated: '2026-11-24'
sources:
- url: https://github.com/xhluca/bm25s
  title: GitHub repository
- url: https://raw.githubusercontent.com/xhluca/bm25s/HEAD/README.md
  title: README
- url: https://pypi.org/project/bm25s/
  title: bm25s — PyPI
- url: https://pypistats.org/api/packages/bm25s/recent
  title: bm25s — PyPI download statistics
---


