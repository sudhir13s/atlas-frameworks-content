---
id: framework/gensim
type: framework
slug: gensim
schema_version: 1.1
title: Gensim
kind: library
category: framework-category/nlp
subcategory: topic-modeling
tagline: Topic Modelling for Humans.
description: Python library for topic modelling, document indexing and similarity retrieval with large corpora, aimed at the natural language processing and information retrieval community. Its algorithms are memory-independent of corpus size and can stream input larger than RAM. Implementations include Latent Semantic Analysis, Latent Dirichlet Allocation, Random Projections, Hierarchical Dirichlet Process and word2vec.
best_for: Topic modelling on large corpora, Document indexing and similarity retrieval
not_ideal_for: Projects that need new features (Gensim is in stable maintenance mode)
key_features:
- Word2Vec, Doc2Vec and FastText models
- Latent Dirichlet Allocation topic modelling
- Latent Semantic Indexing
- Streamed out-of-core processing of corpora larger than RAM
- Document similarity queries
- Distributed LSA and LDA on a cluster of computers
use_cases:
- Topic modelling on large corpora
- Document similarity
- Training word embeddings
pros:
- Processes corpora larger than RAM by streaming
- Multicore implementations of its core algorithms
cons:
- 'In stable maintenance mode: new features are not accepted, only bug and documentation fixes'
language: Python
languages_supported:
- Python
maintained_by: Gensim open-source community
license_spdx: LGPL-2.1-only
github_url: https://github.com/piskvorky/gensim
docs_url: https://radimrehurek.com/gensim/
website_url: https://radimrehurek.com/gensim/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
maturity: stable
backing:
  type: community
alternatives:
- framework/sentence-transformers
registry_signals:
  github_stars: 16516
  downloads_monthly: 3000000
  latest_version: 4.4.0
  latest_release_date: '2025-10-16'
  observed_at: '2026-11-20'
  source: https://github.com/piskvorky/gensim
aliases:
- piskvorky/gensim
tags:
- nlp
- topic-modeling
- embeddings
- unsupervised
updated: '2026-11-21'
sources:
- url: https://github.com/piskvorky/gensim
  title: GitHub repository
- url: https://radimrehurek.com/gensim/
  title: Documentation
- url: https://radimrehurek.com/gensim/apiref.html
  title: API reference
- url: https://pypi.org/project/gensim/
  title: gensim — PyPI
---

## Overview

Python library for topic modelling, document indexing and similarity retrieval with large corpora, aimed at the natural language processing and information retrieval community. Its algorithms are memory-independent of corpus size and can stream input larger than RAM. Implementations include Latent Semantic Analysis, Latent Dirichlet Allocation, Random Projections, Hierarchical Dirichlet Process and word2vec.
