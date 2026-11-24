---
id: framework/flashrank
type: framework
slug: flashrank
schema_version: 3.0
title: FlashRank
status: curated
kind: library
category: framework-category/rag
subcategory: reranking
tagline: Lite & Super-fast re-ranking for your search & retrieval pipelines.
description: FlashRank is a Python library that reranks search results with small cross-encoder models or listwise LLM rerankers, running on CPU without PyTorch or Transformers. It takes a query and a list of passages with optional IDs and metadata, and returns the passages sorted by a relevance score. It sits after keyword, vector or hybrid retrieval and before the passages are passed to an LLM.
best_for: CPU-only reranking, Reranking in serverless functions
key_features:
- Pairwise and pointwise cross-encoder rerankers up to 512 tokens
- Listwise LLM rerankers up to 8192 tokens
- Default model of about 4MB
- Multilingual model for 100+ languages
- Arabic reranker model
- 4-bit quantised rank_zephyr GGUF model
- ONNX Runtime inference
use_cases:
- Reranking lexical search results
- Reranking vector search results for RAG
- Reranking hybrid search results
- Reranking inside AWS Lambda functions
pros:
- No Torch or Transformers dependency
- Small package for short serverless cold starts
- Model cache directory can be set for read-only environments
language: Python
languages_supported:
- Python
maintained_by: Prithivi Da
license_spdx: Apache-2.0
github_url: https://github.com/PrithivirajDamodaran/FlashRank
registry_signals:
  github_stars: 1015
  downloads_monthly: 581614
  latest_version: 0.2.10
  latest_release_date: '2025-01-06'
  observed_at: '2026-11-24'
  source: https://github.com/PrithivirajDamodaran/FlashRank
aliases:
- PrithivirajDamodaran/FlashRank
tags:
- reranking
- cross-encoder
- ranking
- rag
- lexical-search
- hybrid-search
- semantic-search
- retrieval-augmented-generation
updated: '2026-11-24'
sources:
- url: https://github.com/PrithivirajDamodaran/FlashRank
  title: GitHub repository
- url: https://raw.githubusercontent.com/PrithivirajDamodaran/FlashRank/HEAD/README.md
  title: README
- url: https://pypi.org/project/FlashRank/
  title: FlashRank — PyPI
- url: https://pypistats.org/api/packages/flashrank/recent
  title: flashrank — PyPI download statistics
---


