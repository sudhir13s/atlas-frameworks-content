---
id: framework/chromadb
type: framework
slug: chromadb
schema_version: 3.0
title: Chroma
status: curated
kind: tool
category: framework-category/vector-dbs
subcategory: embedded
tagline: The open-source data infrastructure for AI.
description: Chroma is open-source data infrastructure for AI that stores documents with their embeddings and metadata and queries them by similarity. It handles embedding and indexing automatically or accepts your own embeddings. It runs in-memory, with a persistent client, in client-server mode, or as the hosted Chroma Cloud.
best_for: Prototyping with an in-memory client, Local and self-hosted vector search
key_features:
- In-memory and persistent clients
- Client-server mode
- Automatic embedding and indexing of documents
- Metadata and document-content filters
- Keyword and regex full-text search
- Indexing of images and audio alongside text
- Python, TypeScript and Rust clients
use_cases:
- Prototype vector search
- Similarity search over documents
- Retrieval store for LangChain and LlamaIndex applications
pros:
- Small core API built around collections
- Works with any embedding model or with your own embeddings
- Runs locally, self-hosted or as a managed cloud service
language: Rust
languages_supported:
- Python
- TypeScript
- Rust
maintained_by: Chroma
license_spdx: Apache-2.0
github_url: https://github.com/chroma-core/chroma
docs_url: https://docs.trychroma.com/
website_url: https://www.trychroma.com/
backing:
  type: corporate
  orgs:
  - Chroma
alternatives:
- framework/qdrant
- framework/weaviate
- framework/milvus
ecosystem_connections:
- framework/langchain
- framework/llamaindex
- framework/sentence-transformers
registry_signals:
  github_stars: 29716
  downloads_monthly: 8666293
  latest_version: 1.5.9
  latest_release_date: '2026-05-05'
  observed_at: '2026-11-20'
  source: https://github.com/chroma-core/chroma
aliases:
- chroma-core/chroma
- ChromaDB
tags:
- vector-db
- embedded
- rag
- simple
- local
updated: '2026-11-21'
sources:
- url: https://github.com/chroma-core/chroma
  title: GitHub repository
- url: https://docs.trychroma.com/
  title: Documentation
- url: https://docs.trychroma.com/docs/overview/getting-started
  title: Getting started
- url: https://docs.trychroma.com/integrations/chroma-integrations
  title: Integrations
- url: https://pypi.org/project/chromadb/
  title: chromadb — PyPI
---


