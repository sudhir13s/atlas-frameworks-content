---
id: framework/rerankers
type: framework
slug: rerankers
schema_version: 3.0
title: rerankers
status: curated
kind: library
category: framework-category/rag
subcategory: reranking
tagline: A lightweight, low-dependency, unified API to use all common reranking and cross-encoder models.
description: rerankers is a Python library that gives one API to many reranking models, from cross-encoders, T5 and ColBERT to LLM rankers such as RankGPT and hosted APIs from Cohere, Jina, Voyage, MixedBread, Pinecone and Isaacus. It takes a query and a list of documents, with optional IDs and metadata, and returns a RankedResults object with a score and rank per document. It sits after first-stage retrieval and before the documents reach the LLM.
best_for: Reranking retrieved documents, Swapping between reranking models without changing code
key_features:
- Cross-encoder rerankers from Sentence Transformers or Transformers
- T5-based and LLM-based pointwise rankers
- RankGPT and RankLLM listwise rankers
- ColBERT and PyLate late-interaction reranking
- FlashRank ONNX rerankers
- Cohere, Jina, Voyage, MixedBread, Pinecone and Isaacus API rerankers
- MonoVLM multi-modal image reranker
- Metadata stored with documents and results
- Async ranking
use_cases:
- Reranking results from vector or keyword search
- Comparing reranking models on the same data
- Reranking inside a LangChain pipeline
pros:
- Core package ships with no dependencies
- Extras install only the dependencies of the chosen models
- New rerankers are added as a class with one rank() method
cons:
- Described by the project as a beta release that may have issues
- Training rerankers is not supported
language: Python
languages_supported:
- Python
maintained_by: Answer.AI
license_spdx: Apache-2.0
github_url: https://github.com/AnswerDotAI/rerankers
backing:
  type: corporate
  orgs:
  - organization/answerdotai
ecosystem_connections:
- framework/flashrank
- framework/sentence-transformers
- framework/langchain
registry_signals:
  github_stars: 1645
  downloads_monthly: 29637
  latest_version: 0.10.0
  latest_release_date: '2025-05-22'
  observed_at: '2026-11-24'
  source: https://github.com/AnswerDotAI/rerankers
aliases:
- AnswerDotAI/rerankers
tags:
- reranking
- cross-encoder
- retrieval
- rag
updated: '2026-11-24'
sources:
- url: https://github.com/AnswerDotAI/rerankers
  title: GitHub repository
- url: https://raw.githubusercontent.com/AnswerDotAI/rerankers/HEAD/README.md
  title: README
- url: https://pypi.org/project/rerankers/
  title: rerankers — PyPI
- url: https://pypistats.org/api/packages/rerankers/recent
  title: rerankers — PyPI download statistics
---


