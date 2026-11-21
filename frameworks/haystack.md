---
id: framework/haystack
type: framework
slug: haystack
schema_version: 1.1
title: Haystack
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Open-source AI orchestration framework for building context-engineered, production-ready LLM applications.
description: Open-source AI orchestration framework by deepset for building production-ready LLM applications in Python. Applications are built as modular pipelines and agent workflows with explicit control over retrieval, routing, memory and generation. Documented uses include RAG systems, multimodal applications, semantic search, question answering and agents.
best_for: RAG systems, Agent workflows, Semantic search and question answering
key_features:
- Pipelines built from reusable components
- Agents with lifecycle hooks and concurrent tool calls
- Built-in components for retrieval, indexing, tool calling, memory and evaluation
- Document Store abstraction
- Synchronous or asynchronous pipelines with token streaming
- Integrations with model providers and vector databases
- Pipelines served as REST APIs or MCP servers through Hayhooks
use_cases:
- RAG applications
- Semantic search and question answering
- Agent workflows
- Multimodal applications
pros:
- Model- and vendor-agnostic components
- Pipelines are explicit graphs with predictable execution
- Tracing, logging and evaluation tools
language: Python
languages_supported:
- Python
maintained_by: deepset
license_spdx: Apache-2.0
github_url: https://github.com/deepset-ai/haystack
docs_url: https://docs.haystack.deepset.ai/
website_url: https://haystack.deepset.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
maturity: production
backing:
  type: corporate
  orgs:
  - deepset
alternatives:
- framework/langchain
- framework/llamaindex
ecosystem_connections:
- framework/chromadb
- framework/qdrant
- framework/weaviate
registry_signals:
  github_stars: 27062
  downloads_monthly: 1000000
  latest_version: 3.5.0
  latest_release_date: '2026-11-10'
  observed_at: '2026-11-20'
  source: https://github.com/deepset-ai/haystack
aliases:
- deepset-ai/haystack
tags:
- llm
- rag
- pipeline
- production
updated: '2026-11-21'
sources:
- url: https://github.com/deepset-ai/haystack
  title: GitHub repository
- url: https://docs.haystack.deepset.ai/
  title: Documentation
- url: https://haystack.deepset.ai/overview/intro
  title: What is Haystack?
- url: https://haystack.deepset.ai/integrations
  title: Haystack integrations
- url: https://pypi.org/project/haystack-ai/
  title: haystack-ai — PyPI
---

## Overview

Open-source AI orchestration framework by deepset for building production-ready LLM applications in Python. Applications are built as modular pipelines and agent workflows with explicit control over retrieval, routing, memory and generation. Documented uses include RAG systems, multimodal applications, semantic search, question answering and agents.
