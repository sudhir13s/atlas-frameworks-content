---
id: framework/pypdf
type: framework
slug: pypdf
schema_version: 3.0
title: pypdf
status: curated
kind: library
category: framework-category/document-parsing
subcategory: pdf-manipulation
tagline: A pure-python PDF library capable of splitting, merging, cropping, and transforming the pages of PDF files.
description: pypdf is a pure-Python library for reading and writing PDF files. It splits, merges, crops and transforms pages, adds custom data, viewing options and passwords, and retrieves text and metadata from PDFs, with a layout extraction mode that mimics the page layout. It reads the text layer only; it is not OCR software, so scanned pages return little or no text.
best_for: Splitting, merging and transforming PDFs, Text and metadata extraction from digital PDFs, Pure-Python environments
not_ideal_for: Scanned or image-only PDFs (it is not OCR software), Extracting table structure
key_features:
- Splitting and merging PDFs
- Cropping and transforming pages
- Text extraction with plain and layout modes
- Metadata reading and writing
- Encryption and decryption, including AES
- Reading and creating annotations
- Adding custom data and viewing options
use_cases:
- Merging and splitting PDF files
- Extracting text from digitally created PDFs
- Password-protecting PDFs
pros:
- Pure Python
- Optional extra for AES encryption
- Companion CLI application pdfly
cons:
- Not OCR software; image-only or scanned pages yield minimal text
- Tables come out as positioned text, not table structure
- Extracting a page with a large uncompressed content stream can need a lot of memory
language: Python
languages_supported:
- Python
maintained_by: py-pdf
license_spdx: BSD-3-Clause
github_url: https://github.com/py-pdf/pypdf
docs_url: https://pypdf.readthedocs.io/en/latest/
maturity: production
registry_signals:
  github_stars: 10307
  downloads_monthly: 206880414
  latest_version: 7.1.1
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-24'
  source: https://github.com/py-pdf/pypdf
aliases:
- py-pdf/pypdf
- PyPDF2
tags:
- pdf
- pdf-parsing
- pdf-parser
- pdf-manipulation
- pdf-documents
- python
updated: '2026-11-24'
sources:
- url: https://github.com/py-pdf/pypdf
  title: GitHub repository
- url: https://raw.githubusercontent.com/py-pdf/pypdf/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/py-pdf/pypdf/HEAD/LICENSE
  title: LICENSE
- url: https://raw.githubusercontent.com/py-pdf/pypdf/HEAD/docs/user/extract-text.md
  title: Extract Text from a PDF (documentation source)
- url: https://pypi.org/project/pypdf/
  title: pypdf — PyPI
- url: https://pypistats.org/api/packages/pypdf/recent
  title: pypdf — PyPI download statistics
---


