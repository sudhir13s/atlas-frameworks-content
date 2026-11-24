---
id: framework/camelot
type: framework
slug: camelot
schema_version: 3.0
title: Camelot
status: curated
kind: library
category: framework-category/document-parsing
subcategory: pdf-tables
tagline: A Python library to extract tabular data from PDFs.
description: Camelot is a Python library and command-line tool that extracts tables from PDFs. It takes a file path, URL or bytes and returns each table as a pandas DataFrame with accuracy and whitespace metrics, exportable to CSV, JSON, Excel, HTML, Markdown or SQLite. Its parsers cover ruled, whitespace-separated and borderless tables, with an optional Table Transformer model and OCR for scanned PDFs.
best_for: Extracting tables from PDFs into DataFrames, Ruled and borderless tables, Table export to CSV, JSON or Excel
key_features:
- Five parsers, lattice, stream, network, hybrid and ml, plus automatic selection
- Optional Table Transformer model for borderless tables
- Optional OCR for scanned and image-only PDFs
- Vector and raster line detection
- pandas DataFrame output
- Export to CSV, JSON, Excel, HTML, Markdown and SQLite
- Per-table accuracy, whitespace and confidence metrics
- Multi-page table stitching
use_cases:
- Extracting tables from PDF reports into ETL workflows
- Converting PDF tables to spreadsheets
- Table extraction from scanned PDFs
pros:
- Default pdfium backend needs no system dependencies
- Metrics to discard poor tables without manual review
- Cell text comes from the PDF text layer or OCR, never from the model
cons:
- Built-in parsers need a text-based PDF; scanned PDFs need the ml and ocr extras
- The ml extra pulls in PyTorch
language: Python
languages_supported:
- Python
maintained_by: camelot-dev
license_spdx: MIT
github_url: https://github.com/camelot-dev/camelot
docs_url: https://camelot-py.readthedocs.io/
maturity: production
registry_signals:
  github_stars: 3859
  downloads_monthly: 2734258
  latest_version: 2.2.0
  latest_release_date: '2026-11-21'
  observed_at: '2026-11-24'
  source: https://github.com/camelot-dev/camelot
aliases:
- camelot-dev/camelot
- camelot-py
tags:
- pdf
- table-extraction
updated: '2026-11-24'
sources:
- url: https://github.com/camelot-dev/camelot
  title: GitHub repository
- url: https://raw.githubusercontent.com/camelot-dev/camelot/HEAD/README.md
  title: README
- url: https://camelot-py.readthedocs.io/
  title: Documentation
- url: https://pypi.org/project/camelot-py/
  title: camelot-py — PyPI
- url: https://pypistats.org/api/packages/camelot-py/recent
  title: camelot-py — PyPI download statistics
---


