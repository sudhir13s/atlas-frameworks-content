---
id: framework/llamaindex
type: framework
slug: llamaindex
schema_version: 1.1
title: LlamaIndex
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Open-source framework of orchestration tools for building RAG and agent applications.
description: LlamaIndex Framework is an open-source Python toolkit for building LLM-powered agents and applications over your own data. It provides data connectors, indexes, query and chat engines, agents and event-driven workflows, built from a core package and separate integration packages for LLM, embedding and vector store providers. The company behind it says its primary focus has shifted to LlamaParse, while the framework remains available as an open toolkit.
best_for: Retrieval-augmented generation over private data, Agents and workflows over documents
key_features:
- Data connectors for APIs, PDFs, documents and SQL
- Indexes and vector store integrations
- Query engines and chat engines
- Agents and tools
- Event-driven workflows with branching, retries and human review
- Evaluation and observability modules
- Core package with separate integration packages
use_cases:
- Question answering over documents (RAG)
- Chatbots
- Structured data extraction
- Text-to-SQL and querying CSVs
- Multi-modal applications over text, images and tables
pros:
- Install only the integrations an application needs
- High-level API for beginners and lower-level APIs for customization
- Python and TypeScript frameworks
cons:
- The company's primary focus has shifted to LlamaParse; the OSS framework remains available as an open toolkit
language: Python
languages_supported:
- Python
- TypeScript
maintained_by: LlamaIndex
license_spdx: MIT
github_url: https://github.com/run-llama/llama_index
docs_url: https://developers.llamaindex.ai/python/framework/
website_url: https://www.llamaindex.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: corporate
  orgs:
  - LlamaIndex
alternatives:
- framework/langchain
- framework/haystack
ecosystem_connections:
- framework/chromadb
- framework/pinecone
- framework/weaviate
registry_signals:
  github_stars: 52967
  downloads_monthly: 1787456
  latest_version: 0.14.26
  latest_release_date: '2026-11-13'
  observed_at: '2026-11-20'
  source: https://github.com/run-llama/llama_index
aliases:
- run-llama/llama_index
tags:
- llm
- rag
- data-framework
- indexing
- retrieval
updated: '2026-11-21'
sources:
- url: https://github.com/run-llama/llama_index
  title: GitHub repository
- url: https://developers.llamaindex.ai/python/framework/
  title: Documentation
- url: https://developers.llamaindex.ai/python/framework/community/integrations
  title: Integrations
- url: https://developers.llamaindex.ai/typescript/framework/
  title: LlamaIndex.TS documentation
- url: https://pypi.org/project/llama-index-core/
  title: llama-index-core — PyPI
---

## Overview

LlamaIndex Framework is an open-source Python toolkit for building LLM-powered agents and applications over your own data. It provides data connectors, indexes, query and chat engines, agents and event-driven workflows, built from a core package and separate integration packages for LLM, embedding and vector store providers. The company behind it says its primary focus has shifted to LlamaParse, while the framework remains available as an open toolkit.
