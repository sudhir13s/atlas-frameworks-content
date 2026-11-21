---
id: framework/langchain
type: framework
slug: langchain
schema_version: 1.1
title: LangChain
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Framework for building agents and LLM-powered applications.
description: LangChain is a framework for building agents and LLM-powered applications by chaining together interoperable components and third-party integrations. It provides a standard interface for models, embeddings, vector stores and more, and its agents are built on top of LangGraph.
best_for: Building agents and LLM-powered applications, Applications that swap between model providers
key_features:
- Agent harness (create_agent) with tools and middleware
- Standard interface for chat models and embeddings
- Integrations with model providers, tools, vector stores and retrievers
- Retrieval building blocks (document loaders, text splitters, vector stores, retrievers)
- Short-term memory for agents through checkpointers
- Agents built on LangGraph for durable execution and persistence
use_cases:
- AI agents with tool use
- Retrieval-augmented generation (RAG)
- LLM-powered applications that connect to external data sources
pros:
- Model providers can be swapped behind one interface
- Third-party integrations for providers, tools and vector stores
- Python and JavaScript/TypeScript libraries
language: Python
languages_supported:
- Python
- JavaScript/TypeScript
maintained_by: LangChain
license_spdx: MIT
github_url: https://github.com/langchain-ai/langchain
docs_url: https://docs.langchain.com/oss/python/langchain/overview
website_url: https://www.langchain.com/
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
  - LangChain
alternatives:
- framework/llamaindex
- framework/semantic-kernel
- framework/dspy
- framework/haystack
ecosystem_connections:
- framework/langsmith
- framework/chromadb
- framework/pinecone
registry_signals:
  github_stars: 149963
  downloads_monthly: 157281980
  latest_version: 1.5.2
  latest_release_date: '2026-11-18'
  observed_at: '2026-11-20'
  source: https://github.com/langchain-ai/langchain
aliases:
- langchain-ai/langchain
tags:
- llm
- agents
- rag
- orchestration
- integrations
updated: '2026-11-21'
sources:
- url: https://github.com/langchain-ai/langchain
  title: GitHub repository
- url: https://docs.langchain.com/oss/python/langchain/overview
  title: Documentation
- url: https://docs.langchain.com/oss/python/langchain/retrieval
  title: Retrieval
- url: https://docs.langchain.com/oss/python/langchain/short-term-memory
  title: Short-term memory
- url: https://docs.langchain.com/oss/python/integrations/providers/overview
  title: Integration providers
- url: https://pypi.org/project/langchain/
  title: langchain — PyPI
---

## Overview

LangChain is a framework for building agents and LLM-powered applications by chaining together interoperable components and third-party integrations. It provides a standard interface for models, embeddings, vector stores and more, and its agents are built on top of LangGraph.
