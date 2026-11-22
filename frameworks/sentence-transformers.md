---
id: framework/sentence-transformers
type: framework
slug: sentence-transformers
schema_version: 1.1
title: Sentence Transformers
kind: library
category: framework-category/nlp
subcategory: embeddings
tagline: Embeddings, Retrieval, and Reranking.
description: Sentence Transformers (SBERT) is a Python module for using and training embedding and reranker models. It computes embeddings from text, images, audio or video, scores pairs of texts with Cross-Encoder (reranker) models, and produces sparse and multi-vector late-interaction embeddings. Pre-trained models are available on Hugging Face, and custom models can be trained or fine-tuned with the library.
best_for: Embeddings, Semantic search, Reranking, Training embedding models
key_features:
- Pre-trained models on the Hugging Face Hub
- Semantic similarity and search
- Multilingual embeddings
- Cross-Encoder reranking
- Sparse Encoder models
- Multi-Vector Encoder models for ColBERT-style retrieval
- Training and fine-tuning
- ONNX and OpenVINO backends with quantization
use_cases:
- Semantic search
- Retrieve and re-rank
- Clustering
- Paraphrase mining
- Duplicate detection
pros:
- Wide selection of pre-trained models on Hugging Face
- Training and fine-tuning built in
- One API for embedding, reranker and sparse models
language: Python
languages_supported:
- Python
maintained_by: Hugging Face
license_spdx: Apache-2.0
github_url: https://github.com/huggingface/sentence-transformers
docs_url: https://www.sbert.net/
website_url: https://www.sbert.net/
backing:
  type: corporate
  orgs:
  - Hugging Face
ecosystem_connections:
- framework/hugging-face-transformers
- framework/faiss
registry_signals:
  github_stars: 19292
  downloads_monthly: 8000000
  latest_version: 6.3.0
  latest_release_date: '2026-11-11'
  observed_at: '2026-11-20'
  source: https://github.com/UKPLab/sentence-transformers
aliases:
- UKPLab/sentence-transformers
- SentenceTransformers
- huggingface/sentence-transformers
tags:
- nlp
- embeddings
- semantic-search
- rag
updated: '2026-11-21'
sources:
- url: https://github.com/huggingface/sentence-transformers
  title: GitHub repository
- url: https://www.sbert.net/
  title: Documentation
- url: https://www.sbert.net/docs/installation.html
  title: Installation
- url: https://www.sbert.net/examples/sentence_transformer/applications/semantic-search/README.html
  title: Semantic Search
- url: https://pypi.org/project/sentence-transformers/
  title: sentence-transformers — PyPI
---

## Overview

Sentence Transformers (SBERT) is a Python module for using and training embedding and reranker models. It computes embeddings from text, images, audio or video, scores pairs of texts with Cross-Encoder (reranker) models, and produces sparse and multi-vector late-interaction embeddings. Pre-trained models are available on Hugging Face, and custom models can be trained or fine-tuned with the library.
