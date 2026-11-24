---
id: framework/paddleocr
type: framework
slug: paddleocr
schema_version: 3.0
title: PaddleOCR
status: curated
kind: library
category: framework-category/document-parsing
subcategory: ocr
tagline: Turn any PDF or image document into structured data for your AI. A lightweight OCR toolkit that bridges the gap between images/PDFs and LLMs. Supports 100+ languages.
description: PaddleOCR is an OCR and document parsing toolkit that converts PDF documents and images into structured JSON or Markdown for LLM applications. It offers PP-OCR models for text detection and recognition in 100+ languages, PP-StructureV3 for structure-aware conversion with table and text coordinates, and the PaddleOCR-VL vision-language models for parsing text, tables, formulas and charts. It sits at the start of a RAG pipeline, before chunking and indexing.
best_for: Multilingual OCR, Converting PDFs and images to Markdown or JSON, Scene text recognition
not_ideal_for: PDF editing or manipulation, Training models in an environment that already holds Transformers (the docs recommend a clean environment)
key_features:
- PP-OCR text detection and recognition in 100+ languages
- PP-StructureV3 conversion to Markdown or JSON with table cell coordinates
- PaddleOCR-VL document parsing models for text, tables, formulas and charts
- Layout analysis for skewed, warped and scanned pages
- Cross-page table merging
- Office documents to Markdown and DOCX export
- ONNX export and OpenVINO, ONNX Runtime and TensorRT acceleration
- Serving for C++, C# and Java applications
use_cases:
- Document parsing for RAG
- Scene text spotting on IDs, street views and industrial parts
- Table and formula recognition
- Document translation
pros:
- Runs on NVIDIA GPU, Intel CPU, Kunlunxin XPU and other accelerators
- Model tiers from 1.5M to 34.5M parameters for edge, mobile and server
- Integrated with Dify and RAGFlow
- Browser inference through PaddleOCR.js
cons:
- Document parsing, information extraction and translation need optional dependency groups beyond the default install
- An inference engine such as PaddlePaddle or Transformers is installed separately
- Training and model export depend on the PaddlePaddle framework
language: Python
languages_supported:
- Python
- C++
- JavaScript
maintained_by: PaddlePaddle
license_spdx: Apache-2.0
github_url: https://github.com/PaddlePaddle/PaddleOCR
docs_url: https://www.paddleocr.ai/latest/en/index.html
website_url: https://www.paddleocr.com
ecosystem_connections:
- framework/dify
- framework/ragflow
registry_signals:
  github_stars: 93097
  downloads_monthly: 1310159
  latest_version: 3.7.0
  latest_release_date: '2026-06-11'
  observed_at: '2026-11-24'
  source: https://github.com/PaddlePaddle/PaddleOCR
aliases:
- PaddlePaddle/PaddleOCR
tags:
- ocr
- document-parsing
- pdf-parser
- pdf2markdown
- pp-ocr
- pp-structure
- paddleocr-vl
- rag
updated: '2026-11-24'
sources:
- url: https://github.com/PaddlePaddle/PaddleOCR
  title: GitHub repository
- url: https://raw.githubusercontent.com/PaddlePaddle/PaddleOCR/HEAD/README.md
  title: README
- url: https://www.paddleocr.ai/latest/en/index.html
  title: Documentation
- url: https://github.com/PaddlePaddle/PaddleOCR/blob/main/docs/version3.x/installation.en.md
  title: Installation
- url: https://pypi.org/project/paddleocr/
  title: paddleocr — PyPI
- url: https://pypistats.org/api/packages/paddleocr/recent
  title: paddleocr — PyPI download statistics
---


