---
id: framework/gensim
type: framework
slug: gensim
schema_version: 1.1
title: Gensim
kind: library
category: framework-category/nlp
subcategory: topic-modeling
tagline: Topic modelling for humans — scalable statistical semantics
description: Library for unsupervised topic modeling, document similarity, and word embeddings. Implements Word2Vec, Doc2Vec, FastText, LDA, and LSI. Memory-efficient streaming implementations for large corpora.
best_for: Topic modeling, document similarity on large corpora
not_ideal_for: Modern text embedding (use SentenceTransformers), any task where transformers excel
key_features:
- Word2Vec, Doc2Vec, FastText
- LDA topic modeling
- LSI/LSA semantic analysis
- Memory-efficient streaming
- Document similarity queries
use_cases:
- Topic modeling on large corpora
- Document similarity
- Word embeddings (pre-transformer era)
pros:
- Memory-efficient for large corpora
- Good topic modeling implementations
- Streaming processing
cons:
- Pre-transformer era — embeddings outdated for many tasks
- Less relevant in the LLM era
language: Python
languages_supported:
- Python
maintained_by: Radim Rehurek
first_release: '2009-01-01'
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
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: low
backing:
  type: community
  funding_or_parent: Created by Radim Rehurek (RARE Technologies); community-maintained
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
updated: '2026-11-20'
sources:
- url: https://github.com/piskvorky/gensim
  title: GitHub repository
- url: https://radimrehurek.com/gensim/
  title: Documentation
---

## Overview

Library for unsupervised topic modeling, document similarity, and word embeddings. Implements Word2Vec, Doc2Vec, FastText, LDA, and LSI. Memory-efficient streaming implementations for large corpora.
