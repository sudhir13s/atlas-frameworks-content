---
id: framework/langchain
type: framework
slug: langchain
schema_version: 1.1
title: LangChain
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Build context-aware reasoning applications with LLMs
description: The most widely adopted framework for building LLM-powered applications. Provides abstractions for chains, agents, RAG pipelines, memory, and tool use. Supports 100+ LLM providers and integrations. LangGraph extends it with stateful multi-agent workflows.
best_for: Rapid prototyping of LLM-powered apps, teams needing many integrations
not_ideal_for: Simple LLM calls (use the provider SDK directly), performance-critical systems
key_features:
- Chain and agent abstractions
- RAG pipeline components
- 100+ LLM provider integrations
- Tool use and function calling
- Memory and conversation management
- LangGraph for stateful multi-agent workflows
- LangSmith for observability
use_cases:
- RAG applications
- Chatbots and conversational AI
- AI agents with tool use
- Document Q&A systems
- Multi-step reasoning workflows
pros:
- Largest ecosystem of integrations
- Fastest way to prototype LLM apps
- Active community and rapid development
- LangGraph adds powerful agent capabilities
cons:
- Abstraction overhead can obscure what LLMs actually do
- Rapid API changes and breaking updates
- Over-abstraction for simple use cases
- Performance overhead from chains of chains
language: Python
languages_supported:
- Python
- JavaScript/TypeScript
maintained_by: LangChain Inc.
first_release: '2022-10-01'
license_spdx: MIT
github_url: https://github.com/langchain-ai/langchain
docs_url: https://python.langchain.com/docs/
website_url: https://www.langchain.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: massive
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - LangChain Inc
  funding_or_parent: Series A $25M led by Sequoia (Feb 2024); earlier $10M seed by Benchmark (Apr 2023)
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
  github_stars: 149964
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
updated: '2026-11-20'
sources:
- url: https://github.com/langchain-ai/langchain
  title: GitHub repository
- url: https://python.langchain.com/docs/
  title: Documentation
---

## Overview

The most widely adopted framework for building LLM-powered applications. Provides abstractions for chains, agents, RAG pipelines, memory, and tool use. Supports 100+ LLM providers and integrations. LangGraph extends it with stateful multi-agent workflows.
