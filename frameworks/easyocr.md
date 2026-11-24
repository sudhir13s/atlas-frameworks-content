---
id: framework/easyocr
type: framework
slug: easyocr
schema_version: 3.0
title: EasyOCR
status: curated
kind: library
category: framework-category/document-parsing
subcategory: ocr
tagline: Ready-to-use OCR with 80+ supported languages and all popular writing scripts including Latin, Chinese, Arabic, Devanagari, Cyrillic and etc.
description: EasyOCR is a Python OCR library built on PyTorch that reads text from images in 80+ languages and scripts. It takes a file path, URL, bytes or a NumPy image and returns a list of bounding boxes with the detected text and a confidence score, or plain text. Detection uses the CRAFT algorithm and recognition a CRNN model, and both can be replaced with custom-trained models.
best_for: Text recognition in images, Multilingual OCR from Python
not_ideal_for: Handwritten text (support is listed as coming next), Recovering document layout or table structure (results are text boxes only)
key_features:
- 80+ languages and scripts including Latin, Chinese, Arabic, Devanagari and Cyrillic
- Several languages read in one pass
- Bounding boxes, text and confidence per detection
- CRAFT text detection and CRNN recognition
- Optional DBNet detector
- CPU-only mode
- Command-line interface
- Training of custom detection and recognition models
use_cases:
- Scene text recognition
- Reading text from photos and screenshots
- Multilingual OCR
pros:
- Model weights download automatically per language
- Accepts file paths, URLs, bytes or OpenCV images
- Dockerfile provided
cons:
- Handwritten text is not yet supported
- Not every language combination can be used together
- No release since version 1.7.2 in September 2024
- Issues older than six months are closed automatically
language: Python
languages_supported:
- Python
maintained_by: Jaided AI
license_spdx: Apache-2.0
github_url: https://github.com/JaidedAI/EasyOCR
docs_url: https://www.jaided.ai/easyocr/documentation
website_url: https://www.jaided.ai
maturity: production
backing:
  type: corporate
  orgs:
  - Jaided AI
ecosystem_connections:
- framework/pytorch
registry_signals:
  github_stars: 30163
  downloads_monthly: 2244521
  latest_version: 1.7.2
  latest_release_date: '2024-09-24'
  observed_at: '2026-11-24'
  source: https://github.com/JaidedAI/EasyOCR
aliases:
- JaidedAI/EasyOCR
tags:
- ocr
- optical-character-recognition
- scene-text-recognition
- deep-learning
- pytorch
- crnn
- python
- machine-learning
updated: '2026-11-24'
sources:
- url: https://github.com/JaidedAI/EasyOCR
  title: GitHub repository
- url: https://raw.githubusercontent.com/JaidedAI/EasyOCR/HEAD/README.md
  title: README
- url: https://pypi.org/project/easyocr/
  title: easyocr — PyPI
- url: https://pypistats.org/api/packages/easyocr/recent
  title: easyocr — PyPI download statistics
---


