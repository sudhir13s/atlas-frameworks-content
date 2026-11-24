---
id: framework/surya
type: framework
slug: surya
schema_version: 3.0
title: Surya
status: curated
kind: library
category: framework-category/document-parsing
subcategory: ocr
tagline: OCR, layout analysis, reading order, table recognition in 90+ languages.
description: Surya is a 689M-parameter document OCR and layout vision-language model with a lightweight Python client and command-line tools. It takes images or PDFs and returns JSON blocks with layout labels, reading order, bounding boxes and HTML content, tables as HTML with merged cells, and math as LaTeX. The model runs behind vLLM, llama.cpp or mlx_vlm, and it is the OCR engine Marker uses for full document conversion.
best_for: Multilingual document OCR, Layout analysis and reading order, Table recognition to HTML
not_ideal_for: Photos and natural scenes (the project states performance there is not the goal)
key_features:
- Full-page and block-level OCR
- Layout analysis with labels such as Table, Picture, SectionHeader, Equation and Form
- Reading order
- Table recognition to HTML with colspan and rowspan
- Inline math as KaTeX-compatible LaTeX
- JSON results with bounding boxes and confidence
- Inference through vLLM, llama.cpp or mlx_vlm
- Interactive web viewer
use_cases:
- OCR of scanned pages and images
- Detecting document layout before parsing
- Extracting tables from document images
- Multilingual text recognition
pros:
- One model handles layout, OCR and table recognition
- Client has no heavy local ML dependencies
- Inference server is spawned automatically on first use
cons:
- Model weights use a modified AI Pubs Open Rail-M licence; broader commercial use of the weights needs a paid licence
- Needs a vLLM, llama.cpp or mlx_vlm inference backend
language: Python
languages_supported:
- Python
maintained_by: Datalab
license_spdx: Apache-2.0
github_url: https://github.com/datalab-to/surya
website_url: https://www.datalab.to
backing:
  type: corporate
  orgs:
  - Datalab
ecosystem_connections:
- framework/marker
- framework/vllm
- framework/llama-cpp
registry_signals:
  github_stars: 21616
  downloads_monthly: 132332
  latest_version: 0.24.0
  latest_release_date: '2026-11-13'
  observed_at: '2026-11-24'
  source: https://github.com/datalab-to/surya
aliases:
- datalab-to/surya
- surya
- surya-ocr
tags:
- ocr
- multilingual-ocr
- layout-analysis
- reading-order
- table-recognition
- document-ai
- vision-language-model
- pdf
updated: '2026-11-24'
sources:
- url: https://github.com/datalab-to/surya
  title: GitHub repository
- url: https://raw.githubusercontent.com/datalab-to/surya/HEAD/README.md
  title: README
- url: https://pypi.org/project/surya-ocr/
  title: surya-ocr — PyPI
- url: https://pypistats.org/api/packages/surya-ocr/recent
  title: surya-ocr — PyPI download statistics
---


