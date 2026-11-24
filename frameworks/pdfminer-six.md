---
id: framework/pdfminer-six
type: framework
slug: pdfminer-six
schema_version: 3.0
title: pdfminer.six
status: curated
kind: library
category: framework-category/document-parsing
subcategory: pdf-parsing
tagline: Community maintained fork of pdfminer - we fathom PDF.
description: pdfminer.six is a community-maintained fork of PDFMiner, written in Python, for extracting and analyzing text in PDF documents. It reads text directly from the PDF source with its exact location, font and colour, runs automatic layout analysis, and outputs text, images, HTML or hOCR through a Python API or the pdf2txt.py command. Its components are modular, so the interpreter or rendering device can be replaced.
best_for: Text extraction from digital PDFs, Layout analysis of text positions, Building custom PDF parsers
not_ideal_for: Scanned or image-only PDFs (text is read from the PDF source), Python versions below 3.10
key_features:
- Text extraction with location, font and colour
- Automatic layout analysis
- Output as text, images, HTML or hOCR
- CJK languages and vertical writing
- Type1, TrueType, Type3 and CID fonts
- Embedded image extraction
- RC4 and AES encryption
- AcroForm, table of contents and tagged content extraction
use_cases:
- Extracting text from PDFs
- Analyzing text positions on a page
- Command-line PDF to text conversion
pros:
- Written entirely in Python
- Modular components that can be replaced
- Command-line tool pdf2txt.py included
cons:
- Community-maintained with limited maintainer availability
- PDFs with incomplete Unicode mappings yield raw (cid:x) values instead of text
- Image extraction needs the optional image extra
language: Python
languages_supported:
- Python
maintained_by: pdfminer
license_spdx: MIT
github_url: https://github.com/pdfminer/pdfminer.six
docs_url: https://pdfminersix.readthedocs.io
maturity: production
backing:
  type: community
registry_signals:
  github_stars: 7057
  downloads_monthly: 82272448
  latest_version: '20260107'
  latest_release_date: '2026-01-07'
  observed_at: '2026-11-24'
  source: https://github.com/pdfminer/pdfminer.six
aliases:
- pdfminer/pdfminer.six
- pdfminer.six
tags:
- pdf
- parser
- python
updated: '2026-11-24'
sources:
- url: https://github.com/pdfminer/pdfminer.six
  title: GitHub repository
- url: https://raw.githubusercontent.com/pdfminer/pdfminer.six/HEAD/README.md
  title: README
- url: https://github.com/pdfminer/pdfminer.six/blob/master/docs/source/faq.rst
  title: Frequently asked questions
- url: https://pypi.org/project/pdfminer.six/
  title: pdfminer.six — PyPI
- url: https://pypistats.org/api/packages/pdfminer.six/recent
  title: pdfminer.six — PyPI download statistics
---


