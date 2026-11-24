---
id: framework/mineru
type: framework
slug: mineru
schema_version: 3.0
title: MinerU
status: curated
kind: tool
category: framework-category/document-parsing
subcategory: document-conversion
tagline: Transforms complex documents like PDFs and Office docs into LLM-ready markdown/JSON for your Agentic workflows.
description: MinerU is a document parsing tool that converts PDFs, scanned images, Office, OpenDocument, EPUB, OFD, HTML and CSV files into Markdown and JSON. It handles OCR, tables with cross-page merging, formulas and complex layouts, and renders one document model to Markdown, HTML, LaTeX, DOCX, EPUB, PDF or structured content lists. It runs as a command-line reader for agents with page and block locators for citation, a Python SDK, an HTTP API and a WebUI.
best_for: Converting PDFs and scans to Markdown or JSON, Documents with tables and formulas, Agent reading of long documents with citations
not_ideal_for: Model-based parsing of Office, HTML, EPUB or OFD files (these are parsed at the flash tier only), Standard or advanced tiers on machines without a GPU or MPS with 8 GB+ VRAM
key_features:
- Input from PDF, images, DOC/DOCX, PPT/PPTX, XLS/XLSX, RTF, OpenDocument, EPUB, OFD, HTML and CSV
- Four parsing tiers, flash, basic, standard and advanced
- OCR of scanned PDFs and images
- Table recognition with cross-page merging
- Inline formula recognition
- Output to Markdown, HTML, LaTeX, DOCX, EPUB, PDF and content lists
- Local document library with search and page or block locators
- Python SDK, V1 API, Router and Gradio WebUI
use_cases:
- PDF to Markdown conversion for RAG
- Parsing academic papers with formulas
- Agent reading of long documents
- Batch document conversion
pros:
- Parses locally by default; remote parsing needs an explicit flag
- Automatic GPU acceleration on Intel, AMD and NVIDIA, and MPS on macOS
- VLM served through llama.cpp, vLLM or LMDeploy
cons:
- Flash tier has the lowest quality
- Requires Python 3.11 to 3.14
- Doclib telemetry is enabled by default
- Commercial licence required above 100 million monthly active users or USD 20 million monthly revenue
language: Python
languages_supported:
- Python
maintained_by: OpenDataLab
license_note: MinerU Open Source License - Apache License 2.0 with additional terms (separate commercial licence above 100 million MAU or USD 20 million monthly revenue; attribution for online services)
github_url: https://github.com/opendatalab/MinerU
docs_url: https://opendatalab.github.io/MinerU/
website_url: https://mineru.net/
ecosystem_connections:
- framework/vllm
- framework/llama-cpp
registry_signals:
  github_stars: 84232
  downloads_monthly: 124803
  latest_version: 4.2.3
  latest_release_date: '2026-11-16'
  observed_at: '2026-11-24'
  source: https://github.com/opendatalab/MinerU
aliases:
- opendatalab/MinerU
tags:
- pdf-parser
- pdf-converter
- ocr
- layout-analysis
- document-analysis
- extract-data
- pdf-extractor-rag
- docx
updated: '2026-11-24'
sources:
- url: https://github.com/opendatalab/MinerU
  title: GitHub repository
- url: https://raw.githubusercontent.com/opendatalab/MinerU/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/opendatalab/MinerU/HEAD/LICENSE.md
  title: LICENSE
- url: https://opendatalab.github.io/MinerU/
  title: Documentation
- url: https://pypi.org/project/mineru/
  title: mineru — PyPI
- url: https://pypistats.org/api/packages/mineru/recent
  title: mineru — PyPI download statistics
---


