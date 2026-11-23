---
id: framework/flair
type: framework
slug: flair
schema_version: 3.0
title: Flair
status: curated
kind: framework
category: framework-category/nlp
subcategory: sequence-labeling
tagline: A framework for Natural Language Processing (NLP).
description: Flair is an NLP framework built directly on PyTorch and developed by Humboldt University of Berlin. It applies pre-trained models for named entity recognition, sentiment analysis, part-of-speech tagging, sense disambiguation and classification, with special support for biomedical texts. Its interfaces combine word and document embeddings, including Flair embeddings and transformers.
best_for: NER and sequence labeling tasks, biomedical NLP
key_features:
- Stacked embeddings (Flair, transformer and classic word embeddings)
- NER, POS, text classification
- Biomedical NER models
- Training custom models
- Models for multiple languages
use_cases:
- Named entity recognition
- Sequence labeling
- Biomedical text mining
pros:
- Builds directly on PyTorch for training custom models
- Dedicated support for biomedical text
- Sequence tagging models hosted on the Hugging Face model hub
language: Python
languages_supported:
- Python
maintained_by: Humboldt University of Berlin
license_spdx: MIT
github_url: https://github.com/flairNLP/flair
docs_url: https://flairnlp.github.io/flair/
website_url: https://flairnlp.github.io/flair/
alternatives:
- framework/spacy
- framework/hugging-face-transformers
ecosystem_connections:
- framework/pytorch
- framework/hugging-face-transformers
registry_signals:
  github_stars: 14399
  downloads_monthly: 64424
  latest_version: 0.15.1
  latest_release_date: '2025-02-05'
  observed_at: '2026-11-20'
  source: https://github.com/flairNLP/flair
aliases:
- flairNLP/flair
tags:
- nlp
- ner
- sequence-labeling
- biomedical
updated: '2026-11-21'
sources:
- url: https://github.com/flairNLP/flair
  title: GitHub repository
- url: https://flairnlp.github.io/flair/
  title: Documentation
- url: https://flairnlp.github.io/docs/intro
  title: Documentation — Quick Start
- url: https://flairnlp.github.io/docs/category/tutorial-3-embeddings
  title: Documentation — Embeddings
- url: https://flairnlp.github.io/docs/tutorial-embeddings/transformer-embeddings
  title: Documentation — Transformer embeddings
---


