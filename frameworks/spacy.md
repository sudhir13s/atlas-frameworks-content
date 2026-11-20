---
id: framework/spacy
type: framework
slug: spacy
schema_version: 1.1
title: spaCy
kind: library
category: framework-category/nlp
subcategory: core-library
tagline: Industrial-strength natural language processing in Python
description: Production-ready NLP library designed for real-world applications. Provides tokenization, NER, POS tagging, dependency parsing, and text classification with pre-trained pipelines for 25+ languages. Fast and memory-efficient.
best_for: Production NLP pipelines, NER, text preprocessing
not_ideal_for: State-of-the-art accuracy on NLU benchmarks (use HF Transformers)
key_features:
- Tokenization and linguistic annotations
- Named entity recognition (NER)
- Dependency parsing
- Text classification
- 25+ language pipelines
- Custom training pipelines
- spaCy-LLM integration
use_cases:
- Named entity recognition
- Text preprocessing for ML
- Information extraction
- Production NLP pipelines
pros:
- Fast and memory-efficient
- Production-ready out of the box
- Excellent documentation
- Good training framework
cons:
- Less flexible than Hugging Face for custom models
- Model quality behind transformer-based alternatives for some tasks
language: Python
languages_supported:
- Python
maintained_by: Explosion AI
first_release: '2015-02-01'
license_spdx: MIT
github_url: https://github.com/explosion/spaCy
docs_url: https://spacy.io/api
website_url: https://spacy.io/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - Explosion AI
alternatives:
- framework/hugging-face-transformers
- framework/stanza
- framework/flair
ecosystem_connections:
- framework/hugging-face-transformers
registry_signals:
  github_stars: 34079
  downloads_monthly: 25230885
  latest_version: 3.8.18
  latest_release_date: '2026-10-26'
  observed_at: '2026-11-20'
  source: https://github.com/explosion/spaCy
aliases:
- explosion/spaCy
tags:
- nlp
- ner
- production
- text-processing
updated: '2026-11-20'
sources:
- url: https://github.com/explosion/spaCy
  title: GitHub repository
- url: https://spacy.io/api
  title: Documentation
---

## Overview

Production-ready NLP library designed for real-world applications. Provides tokenization, NER, POS tagging, dependency parsing, and text classification with pre-trained pipelines for 25+ languages. Fast and memory-efficient.
