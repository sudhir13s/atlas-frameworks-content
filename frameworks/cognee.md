---
id: framework/cognee
type: framework
slug: cognee
schema_version: 3.0
title: Cognee
status: curated
kind: library
category: framework-category/rag
subcategory: agent-memory
tagline: Cognee is the open-source AI memory platform for agents.
description: Cognee is an open-source memory platform that turns documents, code and conversations into a self-hosted knowledge graph that AI agents search and reuse across sessions. Its remember operation turns text into entities, relationships and searchable chunks, and recall retrieves graph, vector or code context, either as raw passages or as an LLM-generated answer. It runs as a Python library, a CLI, a REST API or an MCP server, and can work with local models and no API key.
best_for: Persistent memory for AI agents, Knowledge-graph retrieval over documents, code and conversations
key_features:
- remember, recall, improve and forget operations
- Knowledge graph extraction from text, with local GLiNER extraction when no LLM key is set
- Code graph of symbols and dependencies
- Automatic routing between search types, including hybrid, graph, temporal and lexical search
- Session memory distilled into permanent memory
- Custom data models and ontologies
- MCP server and plugins for Claude Code, Codex and other agents
- Python, TypeScript, Rust and REST interfaces
use_cases:
- Long-term memory for coding and chat agents
- Company knowledge base built from docs, tickets and code
- Question answering grounded in a knowledge graph
pros:
- Text ingestion and retrieval work without an LLM key
- Whole memory layer can run on a single Postgres instance
- Imports memory from Mem0, Letta, Zep or Graphiti
cons:
- Postgres as a graph store is released as a demo feature; the production-ready version is a licensed product
- The bundled GLiNER extractor is a demo of the small-model pipeline
language: Python
languages_supported:
- Python
- TypeScript
- Rust
maintained_by: topoteretes
license_spdx: Apache-2.0
github_url: https://github.com/topoteretes/cognee
docs_url: https://docs.cognee.ai/
website_url: https://www.cognee.ai
alternatives:
- framework/mem0
- framework/graphiti
registry_signals:
  github_stars: 33536
  downloads_monthly: 183402
  latest_version: 1.6.10
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-24'
  source: https://github.com/topoteretes/cognee
aliases:
- topoteretes/cognee
- cognee
tags:
- agent-memory
- ai-memory
- knowledge-graph
- graph-rag
- context-engineering
- vector-database
updated: '2026-11-24'
sources:
- url: https://github.com/topoteretes/cognee
  title: GitHub repository
- url: https://raw.githubusercontent.com/topoteretes/cognee/HEAD/README.md
  title: README
- url: https://docs.cognee.ai/core-concepts/main-operations/recall
  title: Query memory (recall)
- url: https://pypi.org/project/cognee/
  title: cognee — PyPI
- url: https://pypistats.org/api/packages/cognee/recent
  title: cognee — PyPI download statistics
---


