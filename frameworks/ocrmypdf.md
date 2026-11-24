---
id: framework/ocrmypdf
type: framework
slug: ocrmypdf
schema_version: 3.0
title: OCRmyPDF
status: curated
kind: tool
category: framework-category/document-parsing
subcategory: ocr
tagline: OCRmyPDF adds an OCR text layer to scanned PDF files, allowing them to be searched.
description: OCRmyPDF is a command-line program and Python package that adds an OCR text layer to scanned PDF files so they can be searched or copy-pasted. It takes a PDF or an image and produces a validated, searchable PDF, PDF/A by default, placing the text below the original image without changing its resolution. Recognition uses the Tesseract engine, and plugins can replace it.
best_for: Making scanned PDFs searchable, Producing PDF/A archives, Batch OCR from the command line
not_ideal_for: Getting text, tables or Markdown as the end result (its output is a searchable PDF)
key_features:
- Searchable PDF/A output from scanned PDFs or images
- OCR text placed below the image for copy and paste
- Original image resolution kept
- Deskew, page rotation and image cleaning
- Image optimization that often shrinks files
- Multi-core processing
- Tesseract OCR with more than 100 languages
- Plugin interface to replace the OCR engine
use_cases:
- Making scanned documents searchable
- Preparing scanned PDFs for text extraction
- Long-term archiving as PDF/A
pros:
- Packaged for Debian, Ubuntu, Fedora, Homebrew, FreeBSD and others
- Docker images for x64 and ARM
- Plugins for EasyOCR, PaddleOCR and Apple Vision
cons:
- Requires Ghostscript and Tesseract installed separately
- Languages beyond the defaults need Tesseract language packs
- MPL-2.0 asks you to publish source-level modifications to OCRmyPDF
language: Python
languages_supported:
- Python
maintained_by: ocrmypdf
license_spdx: MPL-2.0
github_url: https://github.com/ocrmypdf/OCRmyPDF
docs_url: https://ocrmypdf.readthedocs.io/
maturity: production
ecosystem_connections:
- framework/tesseract
- framework/easyocr
- framework/paddleocr
registry_signals:
  github_stars: 35382
  downloads_monthly: 1284375
  latest_version: 17.14.2
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-24'
  source: https://github.com/ocrmypdf/OCRmyPDF
aliases:
- ocrmypdf/OCRmyPDF
tags:
- ocr
- pdf
- tesseract
- image-processing
- python
updated: '2026-11-24'
sources:
- url: https://github.com/ocrmypdf/OCRmyPDF
  title: GitHub repository
- url: https://raw.githubusercontent.com/ocrmypdf/OCRmyPDF/HEAD/README.md
  title: README
- url: https://pypi.org/project/ocrmypdf/
  title: ocrmypdf — PyPI
- url: https://pypistats.org/api/packages/ocrmypdf/recent
  title: ocrmypdf — PyPI download statistics
---


