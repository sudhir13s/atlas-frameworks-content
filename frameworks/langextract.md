---
id: framework/langextract
type: framework
slug: langextract
schema_version: 3.0
title: LangExtract
status: curated
kind: library
category: framework-category/nlp
subcategory: information-extraction
tagline: A Python library for extracting structured information from unstructured text using LLMs with precise source grounding and interactive visualization.
description: LangExtract is a Python library that uses LLMs to extract structured information from unstructured text documents, such as clinical notes or reports, based on a prompt and a few examples. It returns extractions with attributes, each mapped to its exact character span in the source, and saves them to JSONL with an interactive HTML visualization. Long documents, including text fetched from URLs, are chunked and processed in parallel over multiple passes.
best_for: Structured extraction from long unstructured documents, Extraction that must be traced back to the source text
key_features:
- Source grounding of every extraction to its character span
- Output schema enforced from few-shot examples
- Chunking, parallel processing and multiple passes for long documents
- Interactive HTML visualization of extractions
- Gemini, OpenAI and local models through Ollama
- Custom model provider plugins
- Vertex AI and OpenAI Batch API support
use_cases:
- Clinical note and report structuring
- Entity and relationship extraction from long texts
- Extraction from documents fetched by URL
pros:
- No model fine-tuning needed; tasks are defined with a few examples
- Works with cloud LLMs or local open-source models
- Docker image available
cons:
- Not an officially supported Google product
- Cloud-hosted models such as Gemini require an API key
- Accuracy of inferred information depends on the selected LLM, the task and the prompt examples
language: Python
languages_supported:
- Python
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/google/langextract
website_url: https://pypi.org/project/langextract/
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 39350
  downloads_monthly: 469886
  latest_version: 1.7.2
  latest_release_date: '2026-11-07'
  observed_at: '2026-11-24'
  source: https://github.com/google/langextract
aliases:
- google/langextract
- langextract
tags:
- information-extraction
- structured-data
- large-language-models
- llm
- gemini
- nlp
updated: '2026-11-24'
sources:
- url: https://github.com/google/langextract
  title: GitHub repository
- url: https://raw.githubusercontent.com/google/langextract/HEAD/README.md
  title: README
- url: https://pypi.org/project/langextract/
  title: langextract — PyPI
- url: https://pypistats.org/api/packages/langextract/recent
  title: langextract — PyPI download statistics
---


