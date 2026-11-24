---
id: framework/lightrag
type: framework
slug: lightrag
schema_version: 3.0
title: LightRAG
status: curated
kind: framework
category: framework-category/rag
subcategory: graph-rag
tagline: Simple and Fast Retrieval-Augmented Generation (EMNLP 2025).
description: LightRAG is a knowledge-graph RAG framework from HKUDS that manages a knowledge graph and vector embeddings side by side. It parses documents with its Native engine, MinerU or Docling, chunks them, extracts entities and relationships with an LLM, and answers queries in local, global, hybrid, naive or mix modes over the graph and text chunks. It runs as a Python SDK or as a server with a web UI and REST API.
best_for: Graph-based RAG over document collections, Cross-document questions, Knowledge bases that need incremental updates
key_features:
- Knowledge graph and vector retrieval in one framework
- Five query modes, with mix as the default
- Optional reranking at query time
- Document parsing with Native, MinerU or Docling engines
- Fixed-length, recursive, vector semantic and paragraph semantic chunking
- Multimodal processing of images, tables and formulas
- Incremental updates and selective deletion
- Server with web UI and REST API
use_cases:
- Question answering over document collections
- Cross-document summarization
- Multimodal document RAG
pros:
- Separate LLM settings for extraction, query, keyword and VLM roles
- PostgreSQL can serve all four storage types
- Vector storage in Milvus or Qdrant and graph storage in Neo4j or Memgraph
cons:
- The default in-memory storages are suitable only for small-scale testing, not for production
- Requires more capable LLMs than traditional RAG for entity-relation extraction
- Enabling rerank typically adds a 1 to 2 second delay
- Changing the embedding model requires re-embedding chunks, entities and relationships
language: Python
languages_supported:
- Python
maintained_by: HKUDS
license_spdx: MIT
github_url: https://github.com/HKUDS/LightRAG
website_url: https://arxiv.org/abs/2410.05779
alternatives:
- framework/graphrag
ecosystem_connections:
- framework/docling
- framework/milvus
- framework/qdrant
registry_signals:
  github_stars: 40841
  downloads_monthly: 164506
  latest_version: 1.5.8
  latest_release_date: '2026-11-23'
  observed_at: '2026-11-24'
  source: https://github.com/HKUDS/LightRAG
aliases:
- HKUDS/LightRAG
tags:
- graphrag
- knowledge-graph
- rag
- retrieval-augmented-generation
- llm
- docling
- mineru
updated: '2026-11-24'
sources:
- url: https://github.com/HKUDS/LightRAG
  title: GitHub repository
- url: https://raw.githubusercontent.com/HKUDS/LightRAG/HEAD/README.md
  title: README
- url: https://pypi.org/project/lightrag-hku/
  title: lightrag-hku — PyPI
- url: https://pypistats.org/api/packages/lightrag-hku/recent
  title: lightrag-hku — PyPI download statistics
---


