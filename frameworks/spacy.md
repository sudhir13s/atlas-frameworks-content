---
id: framework/spacy
type: framework
slug: spacy
schema_version: 1.1
title: spaCy
kind: library
category: framework-category/nlp
subcategory: core-library
tagline: Industrial-strength Natural Language Processing (NLP) in Python.
description: spaCy is a library for natural language processing in Python and Cython, designed to be used in real products. It provides trained pipelines and components for tokenization, part-of-speech tagging, dependency parsing, named entity recognition, text classification and more. It includes a training system, model packaging and multi-task learning with pretrained transformers such as BERT.
best_for: NLP in real products, Named entity recognition, Text classification
key_features:
- Linguistically-motivated tokenization
- Named entity recognition (NER)
- Part-of-speech tagging and dependency parsing
- Text classification
- Entity linking and lemmatization
- Trained pipelines for many languages
- Training system and model packaging
- LLM components in pipelines
- Visualizers for syntax and NER
use_cases:
- Named entity recognition
- Text classification
- Dependency parsing
- Entity linking
pros:
- Trained pipelines install as Python packages
- Built-in training system
- Extensible with custom components and attributes
- Custom models in PyTorch and TensorFlow
language: Python
languages_supported:
- Python
maintained_by: Explosion AI
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
maturity: production
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
updated: '2026-11-21'
sources:
- url: https://github.com/explosion/spaCy
  title: GitHub repository
- url: https://spacy.io/api
  title: Documentation
- url: https://spacy.io/usage
  title: Install spaCy
- url: https://spacy.io/usage/embeddings-transformers
  title: Embeddings, Transformers and Transfer Learning
- url: https://pypi.org/project/spacy/
  title: spacy — PyPI
---

## Overview

spaCy is a library for natural language processing in Python and Cython, designed to be used in real products. It provides trained pipelines and components for tokenization, part-of-speech tagging, dependency parsing, named entity recognition, text classification and more. It includes a training system, model packaging and multi-task learning with pretrained transformers such as BERT.
