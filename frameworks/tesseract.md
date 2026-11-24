---
id: framework/tesseract
type: framework
slug: tesseract
schema_version: 3.0
title: Tesseract OCR
status: curated
kind: tool
category: framework-category/document-parsing
subcategory: ocr
tagline: Tesseract Open Source OCR Engine (main repository).
description: Tesseract is an open-source OCR engine, shipped as the libtesseract library and the tesseract command-line program. It reads images such as PNG, JPEG and TIFF and writes plain text, hOCR (HTML), PDF, invisible-text-only PDF, TSV, ALTO or PAGE output. Since version 4 it includes an LSTM-based engine focused on line recognition, alongside the legacy character-pattern engine, and it recognizes more than 100 languages.
best_for: Command-line OCR of images, Embedding OCR in C and C++ applications, Producing searchable PDFs from images
key_features:
- LSTM-based line recognition engine
- Legacy Tesseract 3 engine mode
- More than 100 languages with UTF-8 support
- Output as plain text, hOCR, PDF, TSV, ALTO and PAGE
- C and C++ API (libtesseract)
- Training for new languages
use_cases:
- OCR of scanned images
- Searchable PDF creation
- Text extraction in document pipelines
pros:
- Wrappers exist for other programming languages
- Pre-built binary packages or build from source
- Apache 2.0 licence
cons:
- No GUI application included
- Image quality often has to be improved for better results
language: C++
languages_supported:
- C
- C++
maintained_by: tesseract-ocr
license_spdx: Apache-2.0
github_url: https://github.com/tesseract-ocr/tesseract
docs_url: https://tesseract-ocr.github.io/tessdoc/
website_url: https://tesseract-ocr.github.io/
registry_signals:
  github_stars: 77630
  latest_version: 5.5.4
  latest_release_date: '2026-10-28'
  observed_at: '2026-11-24'
  source: https://github.com/tesseract-ocr/tesseract
aliases:
- tesseract-ocr/tesseract
- tesseract
tags:
- ocr
- ocr-engine
- tesseract
- tesseract-ocr
- lstm
- machine-learning
updated: '2026-11-24'
sources:
- url: https://github.com/tesseract-ocr/tesseract
  title: GitHub repository
- url: https://raw.githubusercontent.com/tesseract-ocr/tesseract/HEAD/README.md
  title: README
- url: https://tesseract-ocr.github.io/tessdoc/
  title: Documentation
- url: https://github.com/tesseract-ocr/tesseract/releases/latest
  title: Latest release
---


