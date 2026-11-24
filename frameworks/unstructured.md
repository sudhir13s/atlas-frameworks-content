---
id: framework/unstructured
type: framework
slug: unstructured
schema_version: 3.0
title: Unstructured
status: curated
kind: library
category: framework-category/document-parsing
subcategory: document-partitioning
tagline: Open-Source Pre-Processing Tools for Unstructured Data.
description: Unstructured is a Python library for ingesting and pre-processing documents such as PDFs, HTML, Word, PowerPoint, Excel, email and images for LLM workflows. Its partition functions detect the file type and break a document into typed elements such as Title, NarrativeText, ListItem and Table, and its chunking functions combine those elements into chunks for RAG. PDFs and images are processed with fast text extraction, a hi_res layout model or Tesseract OCR.
best_for: Turning mixed document types into elements for RAG, Chunking documents by section, Partitioning PDFs and images with OCR
not_ideal_for: Multi-column documents without extractable text under hi_res (the docs recommend ocr_only for them)
key_features:
- Automatic file-type detection and routing with partition
- Partitioning of PDF, DOCX, PPTX, XLSX, HTML, EML, MSG, EPUB, images and more
- PDF strategies fast, hi_res, ocr_only and auto
- Layout detection with detectron2_onnx in hi_res mode
- Table extraction with an HTML representation in element metadata
- OCR through Tesseract with language selection
- Chunking strategies basic and by_title
- Docker images for x86_64 and Apple silicon
use_cases:
- Document pre-processing for RAG
- Chunking documents by section titles
- Extracting tables from PDFs and spreadsheets
- Parsing email archives
pros:
- One partition call covers many document types
- Docker images built for every push to main
- Runs locally, against a self-hosted API or through the hosted API
cons:
- hi_res has difficulty ordering elements in multi-column documents
- PDF, image and Office processing need system packages such as Tesseract, Poppler and LibreOffice
- Sends usage telemetry by default unless DO_NOT_TRACK or SCARF_NO_ANALYTICS is set
language: Python
languages_supported:
- Python
maintained_by: Unstructured
license_spdx: Apache-2.0
github_url: https://github.com/Unstructured-IO/unstructured
docs_url: https://docs.unstructured.io/open-source/introduction/overview
website_url: https://www.unstructured.io/
backing:
  type: corporate
  orgs:
  - Unstructured
ecosystem_connections:
- framework/tesseract
- framework/pdfminer-six
registry_signals:
  github_stars: 15777
  downloads_monthly: 2529234
  latest_version: 0.27.37
  latest_release_date: '2026-11-06'
  observed_at: '2026-11-24'
  source: https://github.com/Unstructured-IO/unstructured
aliases:
- Unstructured-IO/unstructured
tags:
- document-parsing
- document-parser
- pdf
- ocr
- docx
- preprocessing
- data-pipelines
- llm
updated: '2026-11-24'
sources:
- url: https://github.com/Unstructured-IO/unstructured
  title: GitHub repository
- url: https://raw.githubusercontent.com/Unstructured-IO/unstructured/HEAD/README.md
  title: README
- url: https://docs.unstructured.io/open-source/core-functionality/partitioning
  title: Partitioning
- url: https://docs.unstructured.io/open-source/core-functionality/chunking
  title: Chunking
- url: https://pypi.org/project/unstructured/
  title: unstructured — PyPI
- url: https://pypistats.org/api/packages/unstructured/recent
  title: unstructured — PyPI download statistics
---


