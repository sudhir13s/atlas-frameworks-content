---
id: framework/flair
type: framework
slug: flair
schema_version: 1.1
title: Flair
kind: framework
category: framework-category/nlp
subcategory: sequence-labeling
tagline: State-of-the-art NLP framework built on PyTorch
description: PyTorch-based NLP framework excelling at sequence labeling tasks (NER, POS, chunking). Known for its stacked embeddings approach combining multiple embedding types. Good for text classification and sequence tagging.
best_for: NER and sequence labeling tasks, biomedical NLP
not_ideal_for: General-purpose NLP, generation tasks
key_features:
- Stacked embeddings (Flair + BERT + GloVe)
- NER, POS, text classification
- Biomedical NER models
- Easy training with few lines of code
- Multi-lingual models
use_cases:
- Named entity recognition
- Sequence labeling
- Biomedical text mining
pros:
- Excellent NER performance
- Easy to fine-tune
- Good biomedical models
cons:
- Smaller community than HF Transformers
- Less flexible for non-labeling tasks
language: Python
languages_supported:
- Python
maintained_by: Humboldt University Berlin
first_release: '2018-06-01'
license_spdx: MIT
github_url: https://github.com/flairNLP/flair
docs_url: https://flairnlp.github.io/flair/
website_url: https://flairnlp.github.io/flair/
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
  - Humboldt University of Berlin
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
updated: '2026-11-20'
sources:
- url: https://github.com/flairNLP/flair
  title: GitHub repository
- url: https://flairnlp.github.io/flair/
  title: Documentation
---

## Overview

PyTorch-based NLP framework excelling at sequence labeling tasks (NER, POS, chunking). Known for its stacked embeddings approach combining multiple embedding types. Good for text classification and sequence tagging.
