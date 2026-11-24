---
id: framework/pymupdf
type: framework
slug: pymupdf
schema_version: 3.0
title: PyMuPDF
status: curated
kind: library
category: framework-category/document-parsing
subcategory: pdf-parsing
tagline: Layout-aware document engine for AI and a feature-rich Python toolkit for extracting, rendering and editing PDFs and other documents.
description: PyMuPDF is a Python library built on the MuPDF C engine for extracting, rendering and editing PDFs and other documents such as XPS, EPUB and images. It returns plain text, text with font and position metadata, tables, images, Markdown or JSON with bounding boxes, and since version 2.0 its layout analysis turns PDFs and Office files into Markdown for RAG and agents. It runs locally without a GPU, with Tesseract or RapidOCR for scanned pages.
best_for: Extracting text and tables from PDFs, Converting PDFs to Markdown or JSON for RAG, Editing, merging and redacting PDFs
key_features:
- Text extraction with font, size, colour and bounding boxes
- Table detection and export to Markdown or pandas
- Markdown, JSON and plain-text output for LLM pipelines
- Layout analysis with multi-column reading order and page chunking
- OCR through Tesseract or RapidOCR
- Page rendering to images
- Annotations, redaction and form filling
- Merging, splitting and encrypting PDFs
use_cases:
- PDF to Markdown conversion for RAG
- Table extraction from PDFs
- OCR of scanned documents
- PDF redaction and editing
pros:
- Runs entirely locally with no telemetry or cloud dependency
- Processes documents without a GPU
- Wheels for Windows, macOS and Linux
cons:
- Not usable from multiple threads; the project recommends multiprocessing
- Office formats need the separately licensed PyMuPDF Office add-on
- Scanned PDFs return no text without OCR
language: Python
languages_supported:
- Python
maintained_by: Artifex Software
license_note: Dual Licensed - GNU AFFERO GPL 3.0 or Artifex Commercial License
github_url: https://github.com/pymupdf/PyMuPDF
docs_url: https://pymupdf.readthedocs.io/
website_url: https://pymupdf.io/
maturity: production
backing:
  type: corporate
  orgs:
  - Artifex Software
ecosystem_connections:
- framework/tesseract
registry_signals:
  github_stars: 11185
  downloads_monthly: 178711219
  latest_version: '2.1'
  latest_release_date: '2026-11-02'
  observed_at: '2026-11-24'
  source: https://github.com/pymupdf/PyMuPDF
aliases:
- pymupdf/PyMuPDF
- fitz
tags:
- pdf
- ocr
- table-extraction
- mupdf
- extract-data
- epub
- text-processing
- python
updated: '2026-11-24'
sources:
- url: https://github.com/pymupdf/PyMuPDF
  title: GitHub repository
- url: https://raw.githubusercontent.com/pymupdf/PyMuPDF/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/pymupdf/PyMuPDF/HEAD/COPYING
  title: COPYING (licence)
- url: https://pymupdf.readthedocs.io/
  title: Documentation
- url: https://pypi.org/project/PyMuPDF/
  title: PyMuPDF — PyPI
- url: https://pypistats.org/api/packages/pymupdf/recent
  title: pymupdf — PyPI download statistics
---


