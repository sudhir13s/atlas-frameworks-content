---
id: framework/semantic-chunkers
type: framework
slug: semantic-chunkers
schema_version: 3.0
title: Semantic Chunkers
status: curated
kind: library
category: framework-category/rag
subcategory: chunking
tagline: A multi-modal chunking library for intelligent chunking of text, video, and audio.
description: Semantic Chunkers is a Python library that splits text, video and audio into chunks by meaning rather than by fixed size. Each chunker takes content plus an encoder, such as a Hugging Face, FastEmbed, OpenAI or Cohere encoder from semantic-router, and returns chunks whose boundaries follow changes in embedding similarity. It sits between loading documents and embedding chunks for retrieval.
best_for: Semantic chunking of text for RAG, Splitting video by content
key_features:
- StatisticalChunker with an automatically chosen similarity threshold
- ConsecutiveChunker for text and other modalities
- CumulativeChunker for noise-resistant splits
- RegexChunker
- Open-source and API encoders through semantic-router
- Async chunking methods
- Semantic video chunking
use_cases:
- Context-aware chunks for RAG
- Splitting video into scenes
- Splitting audio
pros:
- StatisticalChunker needs little threshold tuning
- Async methods for faster processing of many documents
cons:
- StatisticalChunker works on text documents only
- CumulativeChunker is very expensive in time and, with API encoders, money
language: Python
languages_supported:
- Python
maintained_by: Aurelio AI
license_spdx: MIT
github_url: https://github.com/aurelio-labs/semantic-chunkers
backing:
  type: corporate
  orgs:
  - Aurelio AI
registry_signals:
  github_stars: 261
  downloads_monthly: 10895
  latest_version: 0.1.1
  latest_release_date: '2025-06-10'
  observed_at: '2026-11-24'
  source: https://github.com/aurelio-labs/semantic-chunkers
aliases:
- aurelio-labs/semantic-chunkers
tags:
- chunking
- semantic-chunking
- rag
updated: '2026-11-24'
sources:
- url: https://github.com/aurelio-labs/semantic-chunkers
  title: GitHub repository
- url: https://raw.githubusercontent.com/aurelio-labs/semantic-chunkers/HEAD/README.md
  title: README
- url: https://github.com/aurelio-labs/semantic-chunkers/blob/main/docs/00-chunkers-intro.ipynb
  title: An Intro to Semantic Chunkers
- url: https://pypi.org/project/semantic-chunkers/
  title: semantic-chunkers — PyPI
- url: https://pypistats.org/api/packages/semantic-chunkers/recent
  title: semantic-chunkers — PyPI download statistics
---


