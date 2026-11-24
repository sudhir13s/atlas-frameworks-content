---
id: framework/ragflow
type: framework
slug: ragflow
schema_version: 3.0
title: RAGFlow
status: curated
kind: tool
category: framework-category/rag
subcategory: rag-engine
tagline: 'RAGFlow is an agent-native database: a Retrieval-Augmented Generation (RAG) engine that grew into context infrastructure.'
description: RAGFlow is an open-source RAG engine with agent capabilities, run as a server with a web UI and APIs. It ingests Word, PowerPoint, Excel, TXT, images, PDFs, scanned copies, structured data and web pages, parses them with its DeepDoc parser (OCR, table structure recognition and layout analysis) or another configured parser, and splits them with template-based chunking. Retrieval combines full-text and vector search with optional reranking and metadata filters, and answers carry traceable citations.
best_for: Self-hosted RAG over complex documents, Teams that want a web UI for datasets, retrieval and agents
key_features:
- DeepDoc parsing with OCR, table structure recognition and layout analysis
- Alternative parsers including Docling, OpenDataLoader, MonkeyOCRv2 and external vision-language models
- Template-based chunking with visualization for human intervention
- Hybrid full-text and vector retrieval with a keyword similarity weight
- Rerank models for candidate results
- Metadata to restrict the retrieval range
- Agentic retrieval with Low, Medium, High and Ultra thinking modes
- Knowledge Compilation into wikis, graphs, trees, mind maps and timelines
- Grounded answers with traceable citations
use_cases:
- Question answering over enterprise documents
- Retrieval over scanned PDFs and tables
- Building agents on top of a document knowledge base
pros:
- Configurable LLMs, embedding models and rerankers
- Ingestion from data sources such as Google BigQuery and website sitemaps
- Docker deployment for evaluation and production
cons:
- Recommended starting configuration is 4 CPU cores, 16 GB RAM and 50 GB of disk
- macOS is not currently supported for the Docker image
- Using a rerank model may increase retrieval latency
- In the open-source 1.0 release, DeepDoc uses CPU inference for layout analysis, OCR and table recognition
language: Go
languages_supported:
- Go
- Python
maintained_by: InfiniFlow
license_spdx: Apache-2.0
github_url: https://github.com/infiniflow/ragflow
docs_url: https://ragflow.io/docs/dev/
website_url: https://ragflow.io
ecosystem_connections:
- framework/docling
- framework/paddleocr
registry_signals:
  github_stars: 94618
  latest_version: 1.0.0
  latest_release_date: '2026-11-06'
  observed_at: '2026-11-24'
  source: https://github.com/infiniflow/ragflow
aliases:
- infiniflow/ragflow
- ragflow
tags:
- rag
- retrieval-augmented-generation
- agentic-retrieval
- context-engine
- knowledge-compilation
- ai-agents
updated: '2026-11-24'
sources:
- url: https://github.com/infiniflow/ragflow
  title: GitHub repository
- url: https://raw.githubusercontent.com/infiniflow/ragflow/HEAD/README.md
  title: README
- url: https://raw.githubusercontent.com/infiniflow/ragflow/HEAD/docs/guides/dataset/configuration.md
  title: Dataset configuration
- url: https://raw.githubusercontent.com/infiniflow/ragflow/HEAD/docs/guides/dataset/retrieval_testing.md
  title: Retrieval testing
- url: https://raw.githubusercontent.com/infiniflow/ragflow/HEAD/docs/guides/dataset/metadata_management.md
  title: Metadata management
- url: https://github.com/infiniflow/ragflow/releases/latest
  title: Latest release
---


