---
id: framework/pdfplumber
type: framework
slug: pdfplumber
schema_version: 3.0
title: pdfplumber
status: curated
kind: library
category: framework-category/document-parsing
subcategory: pdf-parsing
tagline: Plumb a PDF for detailed information about each char, rectangle, line, et cetera — and easily extract text and tables.
description: pdfplumber is a Python library and command-line tool, built on pdfminer.six, that exposes every character, rectangle, line and curve of a PDF page with its position. It extracts text, with an optional layout-preserving mode, words with bounding boxes and tables, reaches form values through its pdfminer.six wrappers, and the CLI writes CSV, JSON or text. Visual debugging draws detected objects and tables on page images; it works best on machine-generated rather than scanned PDFs.
best_for: Table extraction from machine-generated PDFs, Position-aware text extraction, Inspecting PDF structure
not_ideal_for: Scanned PDFs (it works best on machine-generated ones), Creating or modifying PDFs
key_features:
- Access to each character, rectangle, line and curve with coordinates
- Text extraction with an experimental layout mode
- Word extraction with bounding boxes
- Table detection from ruling lines and word alignment
- Visual debugging of objects and the table finder
- Form field values through its pdfminer.six wrappers
- Command-line output as CSV, JSON or text
- Regex search with match positions
use_cases:
- Extracting tables from PDF reports
- Extracting fixed-width text data
- Debugging PDF text extraction
pros:
- Visual debugging integrated with extraction
- Customizable table-extraction settings and strategies
- Crop-box filtering of page objects
cons:
- No OCR
- No PDF generation or modification
- Weak support for tables in OCR'ed documents
- No direct reconstruction of image content
- No dedicated interface for form data
language: Python
languages_supported:
- Python
maintained_by: jsvine
license_spdx: MIT
github_url: https://github.com/jsvine/pdfplumber
alternatives:
- framework/pdfminer-six
- framework/pypdf
- framework/pymupdf
- framework/camelot
ecosystem_connections:
- framework/pdfminer-six
registry_signals:
  github_stars: 10923
  downloads_monthly: 71037403
  latest_version: 0.11.11
  latest_release_date: '2026-11-21'
  observed_at: '2026-11-24'
  source: https://github.com/jsvine/pdfplumber
aliases:
- jsvine/pdfplumber
tags:
- pdf
- pdf-parsing
- table-extraction
updated: '2026-11-24'
sources:
- url: https://github.com/jsvine/pdfplumber
  title: GitHub repository
- url: https://raw.githubusercontent.com/jsvine/pdfplumber/HEAD/README.md
  title: README
- url: https://pypi.org/project/pdfplumber/
  title: pdfplumber — PyPI
- url: https://pypistats.org/api/packages/pdfplumber/recent
  title: pdfplumber — PyPI download statistics
---


