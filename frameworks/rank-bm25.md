---
id: framework/rank-bm25
type: framework
slug: rank-bm25
schema_version: 3.0
title: Rank-BM25
status: curated
kind: library
category: framework-category/search-engines
subcategory: bm25-library
tagline: A Collection of BM25 Algorithms in Python.
description: Rank-BM25 is a Python package of BM25 algorithms for querying a set of documents and returning the ones most relevant to the query. It takes a corpus as a list of token lists and a tokenized query, and returns a score per document or the top-n documents. It covers the lexical retrieval step and leaves all text preprocessing, such as lowercasing, stopword removal and stemming, to the caller.
best_for: Small-scale BM25 ranking in Python, Prototyping keyword search
key_features:
- Okapi BM25
- BM25L
- BM25+
- Scores for every document in the corpus
- Top-n document retrieval
use_cases:
- Keyword ranking of a small document set
- Lexical baseline for retrieval experiments
pros:
- Installs with pip and runs in a few lines
- Works on any pre-tokenized corpus
cons:
- Does no text preprocessing; tokenization, stemming and stopword removal are left to the user
- The author points large-scale production users to a more performant retrieval package
language: Python
languages_supported:
- Python
maintained_by: dorianbrown
license_spdx: Apache-2.0
github_url: https://github.com/dorianbrown/rank_bm25
registry_signals:
  github_stars: 1420
  downloads_monthly: 9745415
  latest_version: 0.2.2
  latest_release_date: '2022-02-16'
  observed_at: '2026-11-24'
  source: https://github.com/dorianbrown/rank_bm25
aliases:
- dorianbrown/rank_bm25
- rank_bm25
tags:
- bm25
- information-retrieval
- ranking
- algorithm
updated: '2026-11-24'
sources:
- url: https://github.com/dorianbrown/rank_bm25
  title: GitHub repository
- url: https://raw.githubusercontent.com/dorianbrown/rank_bm25/HEAD/README.md
  title: README
- url: https://pypi.org/project/rank-bm25/
  title: rank-bm25 — PyPI
- url: https://pypistats.org/api/packages/rank-bm25/recent
  title: rank-bm25 — PyPI download statistics
---


