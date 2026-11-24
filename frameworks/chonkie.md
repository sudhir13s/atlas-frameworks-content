---
id: framework/chonkie
type: framework
slug: chonkie
schema_version: 3.0
title: Chonkie
status: curated
kind: library
category: framework-category/rag
subcategory: chunking
tagline: The lightweight ingestion library for fast, efficient and robust RAG pipelines.
description: Chonkie is a Python chunking library for RAG pipelines. It takes text or files, splits them with token, sentence, recursive, semantic, late, code, neural, LLM-based or table chunkers, and returns chunks with their text and token counts. Its pipeline can then add overlap and embeddings and write the chunks to a vector database, so it sits between document loading and indexing.
best_for: Chunking text for RAG, Building an ingestion pipeline from documents to a vector database
key_features:
- Token, sentence, recursive, semantic, late, code, neural and LLM-based (Slumber) chunkers
- Table chunker for Markdown tables
- Pipeline API chaining chunkers and refineries
- Overlap and embeddings refineries
- Handshakes that write chunks to Chroma, Qdrant, Pinecone, Weaviate, Milvus, LanceDB, pgvector, Elasticsearch, MongoDB and Turbopuffer
- Export to JSON or Hugging Face datasets
- Self-hosted REST API server
- Custom token counting functions
use_cases:
- Splitting documents into chunks for retrieval
- Embedding chunks and loading them into a vector database
- Chunking source code
- Chunking Markdown tables
pros:
- Minimal default install, with optional extras per chunker or integration
- Async pipeline runs
- Out-of-the-box support for 56 languages
language: Python
languages_supported:
- Python
maintained_by: Chonkie
license_spdx: MIT
github_url: https://github.com/feyninc/chonkie
docs_url: https://docs.chonkie.ai
website_url: https://docs.chonkie.ai
backing:
  type: corporate
  orgs:
  - Chonkie
ecosystem_connections:
- framework/chromadb
- framework/qdrant
- framework/pinecone
- framework/weaviate
- framework/milvus
- framework/lancedb
- framework/pgvector
- framework/sentence-transformers
registry_signals:
  github_stars: 4854
  downloads_monthly: 1355595
  latest_version: 1.7.0
  latest_release_date: '2026-07-07'
  observed_at: '2026-11-24'
  source: https://github.com/feyninc/chonkie
aliases:
- feyninc/chonkie
- chonkie-inc/chonkie
tags:
- chunking
- text-splitter
- semantic-chunker
- rag
- retrieval-systems
- llms
updated: '2026-11-24'
sources:
- url: https://github.com/feyninc/chonkie
  title: GitHub repository
- url: https://raw.githubusercontent.com/feyninc/chonkie/HEAD/README.md
  title: README
- url: https://docs.chonkie.ai
  title: Documentation
- url: https://pypi.org/project/chonkie/
  title: chonkie — PyPI
- url: https://pypistats.org/api/packages/chonkie/recent
  title: chonkie — PyPI download statistics
---


