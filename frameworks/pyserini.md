---
id: framework/pyserini
type: framework
slug: pyserini
schema_version: 3.0
title: Pyserini
status: curated
kind: library
category: framework-category/search-engines
subcategory: ir-toolkit
tagline: Python toolkit for reproducible information retrieval research with sparse and dense representations.
description: Pyserini is a Python toolkit for reproducible information retrieval research with sparse and dense representations. Sparse retrieval such as BM25 runs through the Lucene-based Anserini toolkit and dense retrieval through Faiss; it takes a query and an index and returns ranked top-k document IDs, whose text can then be fetched. It is designed for first-stage retrieval in a multi-stage ranking architecture and ships queries, relevance judgments, prebuilt indexes and evaluation scripts for standard test collections.
best_for: Reproducing information retrieval baselines, BM25, learned sparse and dense retrieval experiments
key_features:
- BM25 retrieval with Lucene
- Learned sparse retrieval such as SPLADE and uniCOIL
- Dense retrieval with Lucene or Faiss
- Hybrid sparse-dense retrieval with HybridSearcher
- Prebuilt indexes for MS MARCO, BEIR and other collections
- Indexing of your own corpus
- Evaluation scripts and two-click reproductions
- REST API and MCP server
use_cases:
- First-stage retrieval research
- Benchmarking retrieval models on standard collections
- Building BM25 baselines for RAG experiments
pros:
- Queries, relevance judgments and indexes ship with the package
- Reproduction matrices for many test collections
- Sparse, dense and hybrid retrieval in one toolkit
cons:
- Requires Java 21 because it depends on Anserini
language: Python
languages_supported:
- Python
maintained_by: castorini
license_spdx: Apache-2.0
github_url: https://github.com/castorini/pyserini
website_url: http://pyserini.io/
ecosystem_connections:
- framework/faiss
registry_signals:
  github_stars: 2233
  downloads_monthly: 92496
  latest_version: 2.4.0
  latest_release_date: '2026-08-27'
  observed_at: '2026-11-24'
  source: https://github.com/castorini/pyserini
aliases:
- castorini/pyserini
tags:
- information-retrieval
updated: '2026-11-24'
sources:
- url: https://github.com/castorini/pyserini
  title: GitHub repository
- url: https://raw.githubusercontent.com/castorini/pyserini/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/castorini/pyserini/HEAD/docs/usage-search.md
  title: How do I search?
- url: https://pypi.org/project/pyserini/
  title: pyserini — PyPI
- url: https://pypistats.org/api/packages/pyserini/recent
  title: pyserini — PyPI download statistics
---


