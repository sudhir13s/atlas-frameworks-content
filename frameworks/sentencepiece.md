---
id: framework/sentencepiece
type: framework
slug: sentencepiece
schema_version: 3.0
title: SentencePiece
status: curated
kind: library
category: framework-category/nlp
subcategory: tokenization
tagline: Unsupervised text tokenizer and detokenizer that trains byte-pair encoding (BPE) and unigram subword models directly from raw sentences.
description: SentencePiece is an unsupervised text tokenizer and detokenizer for neural network text generation systems, such as large language models, whose vocabulary size is fixed before training. It trains byte-pair encoding (BPE) or unigram language model subword models directly from raw sentences, then encodes text into subword pieces or vocabulary IDs and decodes them back losslessly. It is written in C++ with a Python module, and a trained .model file gives the same tokenization in any environment.
best_for: Training subword tokenizers for language models, Tokenizing languages without explicit word boundaries
key_features:
- Byte-pair encoding (BPE) and unigram language model subword units
- Training directly from raw sentences with no language-specific pre-tokenizer
- Lossless detokenization with whitespace as a meta-symbol
- Subword regularization and BPE-dropout sampling
- Self-contained .model file with normalization rules and vocabulary
- SentencePiece Lite, a zero-dependency C++20 runtime
- Command-line tools, C++ API and Python module
use_cases:
- Tokenizer training for language models
- Text preprocessing for neural machine translation
- On-device tokenization with SentencePiece Lite
pros:
- Language-independent pipeline, including Chinese, Japanese and Thai
- Same tokenization results in C++, Python and other environments with the same model file
- Builds with CMake or Bazel
cons:
- Not an official Google product
language: C++
languages_supported:
- C++
- Python
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/google/sentencepiece
docs_url: https://google.github.io/sentencepiece/
maturity: production
registry_signals:
  github_stars: 12178
  downloads_monthly: 29772400
  latest_version: 0.2.3
  latest_release_date: '2026-11-05'
  observed_at: '2026-11-24'
  source: https://github.com/google/sentencepiece
aliases:
- google/sentencepiece
tags:
- natural-language-processing
- neural-machine-translation
- word-segmentation
- tokenization
updated: '2026-11-24'
sources:
- url: https://github.com/google/sentencepiece
  title: GitHub repository
- url: https://raw.githubusercontent.com/google/sentencepiece/HEAD/README.md
  title: README
- url: https://pypi.org/project/sentencepiece/
  title: sentencepiece — PyPI
- url: https://google.github.io/sentencepiece/
  title: Documentation
- url: https://pypistats.org/api/packages/sentencepiece/recent
  title: sentencepiece — PyPI download statistics
---


