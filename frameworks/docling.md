---
id: framework/docling
type: framework
slug: docling
schema_version: 3.0
title: Docling
status: curated
kind: library
category: framework-category/document-parsing
subcategory: document-conversion
tagline: Get your documents ready for gen AI.
description: Docling is a Python library and command-line tool that parses documents in many formats, including PDF, DOCX, PPTX, XLSX, HTML, images and audio, into a unified DoclingDocument representation. Its PDF understanding covers page layout, reading order, table structure, code and formulas, with OCR for scanned PDFs and images. It exports Markdown, HTML, DocTags or lossless JSON, which RAG and agent frameworks then chunk, embed and index.
best_for: Converting PDFs and office files to Markdown or JSON for RAG, Parsing scanned documents with OCR, Local processing of sensitive documents
not_ideal_for: Extracting title, author and reference metadata (listed as coming soon), Python 3.9 environments (support dropped in version 2.70.0)
key_features:
- Parsing of PDF, DOCX, PPTX, XLSX, HTML, EPUB, images, audio and more
- PDF layout, reading order and table structure understanding
- OCR for scanned PDFs and images
- Unified DoclingDocument representation
- Export to Markdown, HTML, DocTags and lossless JSON
- Visual language model support such as GraniteDocling
- MCP server and API server (docling-serve)
- Command-line interface
use_cases:
- Preparing documents for retrieval-augmented generation
- PDF to Markdown conversion
- Table extraction from PDFs
- Document ingestion for agents
pros:
- Runs locally, including in air-gapped environments
- Integrations with LangChain, LlamaIndex, Crew AI and Haystack
- Works on macOS, Linux and Windows for x86_64 and arm64
cons:
- Requires Python 3.10 or higher
- Models carry their own licences, separate from the MIT-licensed codebase
language: Python
languages_supported:
- Python
maintained_by: docling-project
license_spdx: MIT
github_url: https://github.com/docling-project/docling
docs_url: https://docling-project.github.io/docling/
maturity: production
backing:
  type: foundation
  orgs:
  - LF AI & Data Foundation
ecosystem_connections:
- framework/langchain
- framework/llamaindex
- framework/crewai
- framework/haystack
registry_signals:
  github_stars: 70945
  downloads_monthly: 4320276
  latest_version: 2.152.0
  latest_release_date: '2026-11-23'
  observed_at: '2026-11-24'
  source: https://github.com/docling-project/docling
aliases:
- docling-project/docling
tags:
- document-parsing
- pdf
- pdf-converter
- markdown
- tables
- docx
- html
- ai
updated: '2026-11-24'
sources:
- url: https://github.com/docling-project/docling
  title: GitHub repository
- url: https://raw.githubusercontent.com/docling-project/docling/HEAD/README.md
  title: README
- url: https://docling-project.github.io/docling/
  title: Documentation
- url: https://docling-project.github.io/docling/usage/supported_formats/
  title: Supported formats
- url: https://pypi.org/project/docling/
  title: docling — PyPI
- url: https://pypistats.org/api/packages/docling/recent
  title: docling — PyPI download statistics
---


