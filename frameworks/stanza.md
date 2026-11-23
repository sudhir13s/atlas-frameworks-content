---
id: framework/stanza
type: framework
slug: stanza
schema_version: 3.0
title: Stanza
status: curated
kind: library
category: framework-category/nlp
subcategory: core-library
tagline: Stanford NLP Python library for tokenization, sentence segmentation, NER, and parsing of many human languages.
description: Stanza is the Stanford NLP Group's official Python library for linguistic analysis of many human languages. Its neural pipeline, built on PyTorch, covers tokenization, multi-word token expansion, lemmatization, part-of-speech and morphological tagging, dependency parsing and named entity recognition using the Universal Dependencies formalism. It also includes the official Python interface to the Java Stanford CoreNLP package.
best_for: Multilingual linguistic analysis, Universal Dependencies parsing
key_features:
- Pretrained neural models for many languages
- Tokenization and part-of-speech tagging
- Dependency and constituency parsing
- Named entity recognition
- Sentiment analysis
- Coreference
- Biomedical and clinical English models
- Python interface to Stanford CoreNLP
use_cases:
- Multilingual NLP
- Linguistic analysis
- Biomedical and clinical text analysis
pros:
- Native Python implementation
- One pipeline design across many languages
- Neural modules trainable on your own annotated data
cons:
- Model training not available through the Pipeline interface and runs from a source checkout
language: Python
languages_supported:
- Python
maintained_by: Stanford NLP Group
license_spdx: Apache-2.0
github_url: https://github.com/stanfordnlp/stanza
docs_url: https://stanfordnlp.github.io/stanza/
website_url: https://stanfordnlp.github.io/stanza/
maturity: experimental
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
updated: '2026-11-21'
sources:
- url: https://github.com/stanfordnlp/stanza
  title: GitHub repository
- url: https://stanfordnlp.github.io/stanza/
  title: Documentation
- url: https://stanfordnlp.github.io/stanza/getting_started.html
  title: Getting Started
- url: https://pypi.org/project/stanza/
  title: stanza — PyPI
---


