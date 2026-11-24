---
id: framework/marker
type: framework
slug: marker
schema_version: 3.0
title: Marker
status: curated
kind: tool
category: framework-category/document-parsing
subcategory: document-conversion
tagline: Convert PDF to markdown + JSON quickly with high accuracy.
description: Marker converts PDF, image, PPTX, DOCX, XLSX, HTML and EPUB files to Markdown, JSON, HTML or flat chunks for RAG. It extracts the PDF text layer, detects page layout and reading order, reconstructs tables and sends scanned pages, equations and complex tables to the Surya OCR model, with an optional LLM pass to improve accuracy. It runs as a command-line tool, a Python library or a local API server.
best_for: Converting PDFs to Markdown or JSON, Preparing document chunks for RAG, Table and equation extraction
key_features:
- Input from PDF, image, PPTX, DOCX, XLSX, HTML and EPUB
- Output as Markdown, JSON, HTML or chunks
- Layout detection and reading order
- Table extraction with a dedicated TableConverter
- Equations converted to LaTeX
- OCR of scanned pages through the Surya model
- Optional LLM mode with Gemini, Claude, OpenAI-compatible, Azure, Vertex, OpenRouter or Ollama
- Removal of headers, footers and other artifacts
- Four modes from CPU-only to full-page VLM OCR on GPU
use_cases:
- PDF to Markdown conversion
- Chunking documents for retrieval
- Extracting tables from PDFs
- Batch conversion of document folders
pros:
- Runs on GPU, CPU or Apple MPS
- CPU-only modes need no inference server
- Extensible through processors, renderers and providers
cons:
- Very complex layouts with nested tables and forms may not work
- Forms may not be rendered well
- Model weights use a modified AI Pubs Open Rail-M licence; commercial use beyond research, personal use and startups under $5M funding or revenue needs a paid licence
language: Python
languages_supported:
- Python
maintained_by: Datalab
license_spdx: Apache-2.0
github_url: https://github.com/datalab-to/marker
website_url: https://www.datalab.to
backing:
  type: corporate
  orgs:
  - Datalab
alternatives:
- framework/docling
- framework/paddleocr
ecosystem_connections:
- framework/surya
registry_signals:
  github_stars: 41039
  downloads_monthly: 87687
  latest_version: 2.2.0
  latest_release_date: '2026-11-12'
  observed_at: '2026-11-24'
  source: https://github.com/datalab-to/marker
aliases:
- datalab-to/marker
- marker
- marker-pdf
tags:
- document-parsing
- document-conversion
- pdf-to-markdown
- pdf-parser
- table-extraction
- ocr
- markdown
- llm
updated: '2026-11-24'
sources:
- url: https://github.com/datalab-to/marker
  title: GitHub repository
- url: https://raw.githubusercontent.com/datalab-to/marker/HEAD/README.md
  title: README
- url: https://pypi.org/project/marker-pdf/
  title: marker-pdf — PyPI
- url: https://pypistats.org/api/packages/marker-pdf/recent
  title: marker-pdf — PyPI download statistics
---


