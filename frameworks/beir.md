---
id: framework/beir
type: framework
slug: beir
schema_version: 3.0
title: BEIR
status: curated
kind: library
category: framework-category/evaluation
subcategory: retrieval-benchmark
tagline: A Heterogeneous Benchmark for Information Retrieval.
description: BEIR is a benchmark of diverse information retrieval tasks and a Python framework for evaluating retrieval models on it. It loads a corpus, queries and relevance judgements from one of the preprocessed datasets or your own data, runs a lexical, dense, sparse or reranking retriever, and reports NDCG, MAP, recall, precision and MRR at several cut-offs. It tests the retrieval step of a RAG pipeline, before any answer is generated.
best_for: Zero-shot evaluation of retrieval models, Comparing embedding and reranking models across domains
key_features:
- 17 preprocessed benchmark datasets, plus loaders for custom datasets
- Evaluation of lexical, dense, sparse and reranking-based retrievers
- NDCG, MAP, recall, precision and MRR at cut-offs from 1 to 1000
- Sentence-BERT, Hugging Face, vLLM with LoRA and API embedding models such as Cohere
- TREC run files and saved results
- Datasets and models on the Hugging Face Hub
- Official leaderboard
use_cases:
- Benchmarking embedding models for retrieval
- Comparing retrieval architectures across domains
- Evaluating a custom retrieval model
pros:
- Datasets downloadable as ready-made zip files or from Hugging Face
- Reproducible reference models and leaderboard published with the SIGIR 2024 resource paper
cons:
- Users must check that they may use each dataset under its own licence
- The repository describes itself as experimental software published to accompany its paper
- Some datasets, such as BioASQ, Signal-1M, TREC-NEWS and Robust04, are not public and must be reproduced
language: Python
languages_supported:
- Python
maintained_by: beir-cellar
license_spdx: Apache-2.0
github_url: https://github.com/beir-cellar/beir
docs_url: https://github.com/beir-cellar/beir/wiki
website_url: http://beir.ai
ecosystem_connections:
- framework/sentence-transformers
- framework/vllm
registry_signals:
  github_stars: 2336
  downloads_monthly: 50209
  latest_version: 2.2.0
  latest_release_date: '2025-06-04'
  observed_at: '2026-11-24'
  source: https://github.com/beir-cellar/beir
aliases:
- beir-cellar/beir
- benchmarkir/beir
tags:
- benchmark
- information-retrieval
- zero-shot-retrieval
- passage-retrieval
- retrieval-models
- sentence-transformers
- rag
- dataset
updated: '2026-11-24'
sources:
- url: https://github.com/beir-cellar/beir
  title: GitHub repository
- url: https://raw.githubusercontent.com/beir-cellar/beir/HEAD/README.md
  title: README
- url: https://pypi.org/project/beir/
  title: beir — PyPI
- url: https://pypistats.org/api/packages/beir/recent
  title: beir — PyPI download statistics
---


