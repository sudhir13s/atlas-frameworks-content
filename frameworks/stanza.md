---
id: framework/stanza
type: framework
slug: stanza
schema_version: 1.1
title: Stanza
kind: library
category: framework-category/nlp
subcategory: core-library
tagline: Stanford NLP library for 70+ languages — neural pipeline for text analysis
description: Stanford's official NLP library with neural network models for tokenization, POS, NER, dependency parsing, and sentiment analysis. Supports 70+ languages with state-of-the-art accuracy on Universal Dependencies.
best_for: Multi-lingual NLP, academic linguistic analysis
not_ideal_for: Production speed requirements, LLM-based tasks
key_features:
- 70+ language support
- Neural tokenization and POS tagging
- Dependency parsing
- NER
- Sentiment analysis
- CoreNLP interface
use_cases:
- Multi-lingual NLP
- Linguistic analysis
- Academic NLP research
pros:
- Best multi-lingual coverage
- High accuracy on linguistic tasks
- Stanford-backed research quality
cons:
- Slower than spaCy
- Less production-oriented
language: Python
languages_supported:
- Python
maintained_by: Stanford NLP Group
first_release: '2020-03-01'
license_spdx: Apache-2.0
github_url: https://github.com/stanfordnlp/stanza
docs_url: https://stanfordnlp.github.io/stanza/
website_url: https://stanfordnlp.github.io/stanza/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: foundation
  orgs:
  - Stanford NLP Group
alternatives:
- framework/spacy
- framework/flair
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 7918
  downloads_monthly: 987826
  latest_version: 1.15.1
  latest_release_date: '2026-11-14'
  observed_at: '2026-11-20'
  source: https://github.com/stanfordnlp/stanza
aliases:
- stanfordnlp/stanza
tags:
- nlp
- multilingual
- linguistics
- stanford
updated: '2026-11-20'
sources:
- url: https://github.com/stanfordnlp/stanza
  title: GitHub repository
- url: https://stanfordnlp.github.io/stanza/
  title: Documentation
---

## Overview

Stanford's official NLP library with neural network models for tokenization, POS, NER, dependency parsing, and sentiment analysis. Supports 70+ languages with state-of-the-art accuracy on Universal Dependencies.
