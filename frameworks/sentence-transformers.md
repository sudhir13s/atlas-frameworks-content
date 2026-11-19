---
id: framework/sentence-transformers
type: framework
slug: sentence-transformers
schema_version: 1.1
title: SentenceTransformers
kind: library
category: framework-category/nlp
subcategory: embeddings
tagline: State-of-the-art text and image embeddings — multilingual, fast, production-ready
description: Library for computing dense vector representations (embeddings) of sentences, paragraphs, and images. Provides 100+ pre-trained models optimized for semantic similarity, search, clustering, and classification.
best_for: Text embeddings for search, RAG, and similarity tasks
not_ideal_for: Text generation, classification without embeddings
key_features:
- 100+ pre-trained embedding models
- Semantic similarity and search
- Multilingual embeddings
- Cross-encoder for reranking
- Custom model training
- ONNX and quantization support
use_cases:
- Semantic search
- RAG embedding generation
- Text clustering
- Duplicate detection
pros:
- Best text embedding library
- Many pre-trained models
- Easy to fine-tune
- Production-ready
cons:
- Embedding quality varies by model
- Fine-tuning requires good training data
language: Python
languages_supported:
- Python
maintained_by: Hugging Face (Nils Reimers)
first_release: '2019-08-01'
license_spdx: Apache-2.0
github_url: https://github.com/UKPLab/sentence-transformers
docs_url: https://www.sbert.net/
website_url: https://www.sbert.net/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: true
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Hugging Face
  funding_or_parent: Created by Nils Reimers at UKP Lab (TU Darmstadt); maintained under Hugging Face
ecosystem_connections:
- framework/hugging-face-transformers
- framework/faiss
- framework/chromadb
registry_signals:
  github_stars: 15800
  downloads_monthly: 8000000
  latest_version: '3.4'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/UKPLab/sentence-transformers
aliases:
- UKPLab/sentence-transformers
tags:
- nlp
- embeddings
- semantic-search
- rag
updated: '2026-11-19'
sources:
- url: https://github.com/UKPLab/sentence-transformers
  title: GitHub repository
- url: https://www.sbert.net/
  title: Documentation
---

## Overview

Library for computing dense vector representations (embeddings) of sentences, paragraphs, and images. Provides 100+ pre-trained models optimized for semantic similarity, search, clustering, and classification.
