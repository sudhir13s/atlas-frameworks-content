---
id: framework/graphiti
type: framework
slug: graphiti
schema_version: 3.0
title: Graphiti
status: curated
kind: framework
category: framework-category/rag
subcategory: knowledge-graph
tagline: Build real-time knowledge graphs for AI agents.
description: Graphiti is an open-source Python framework from Zep for building and querying temporal context graphs for AI agents. It ingests episodes of unstructured text or structured JSON, uses an LLM to extract entities and facts with validity windows, and updates the graph incrementally without recomputing it. Queries use hybrid retrieval that combines semantic embeddings, BM25 keyword search and graph traversal, with reranking.
best_for: Agent memory over changing data, Temporal knowledge graphs with provenance, Historical queries about what was true when
key_features:
- Temporal facts with validity windows and automatic invalidation
- Episodes that trace every fact back to its source data
- Prescribed ontology through Pydantic models or learned structure
- Incremental graph construction
- Hybrid retrieval with embeddings, BM25 and graph traversal
- Reciprocal Rank Fusion, MMR, cross-encoder and node distance reranking
- Neo4j, FalkorDB, Amazon Neptune and Relate graph backends
- Reference MCP and REST servers
use_cases:
- Long-term memory for AI agents
- Knowledge graphs from conversations and business data
- Point-in-time queries over evolving facts
pros:
- Retrieval does not rely on LLM summarization
- LLM providers include OpenAI, Anthropic, Gemini, Groq and OpenAI-compatible local servers
- Pluggable graph database backends
cons:
- Works best with LLM services that support Structured Output; other services may cause ingestion failures
- Reference MCP and REST servers have no authentication, authorization or prompt-injection protection and are not production deployments
- Defaults to OpenAI for LLM inference and embedding
- Collects anonymous usage statistics
language: Python
languages_supported:
- Python
maintained_by: Zep
license_spdx: Apache-2.0
github_url: https://github.com/getzep/graphiti
docs_url: https://help.getzep.com/graphiti
website_url: https://help.getzep.com/graphiti
backing:
  type: corporate
  orgs:
  - Zep
alternatives:
- framework/graphrag
ecosystem_connections:
- framework/langgraph
registry_signals:
  github_stars: 33043
  downloads_monthly: 891487
  latest_version: 0.32.0
  latest_release_date: '2026-11-23'
  observed_at: '2026-11-24'
  source: https://github.com/getzep/graphiti
aliases:
- getzep/graphiti
- graphiti
- graphiti-core
tags:
- agents
- graph
- knowledge-graph
- llms
- rag
updated: '2026-11-24'
sources:
- url: https://github.com/getzep/graphiti
  title: GitHub repository
- url: https://raw.githubusercontent.com/getzep/graphiti/HEAD/README.md
  title: README
- url: https://help.getzep.com/graphiti/working-with-data/searching
  title: Searching the Graph
- url: https://pypi.org/project/graphiti-core/
  title: graphiti-core — PyPI
- url: https://pypistats.org/api/packages/graphiti-core/recent
  title: graphiti-core — PyPI download statistics
---


