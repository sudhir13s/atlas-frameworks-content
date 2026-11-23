---
id: framework/langsmith
type: framework
slug: langsmith
schema_version: 3.0
title: LangSmith
status: curated
kind: tool
category: framework-category/observability
subcategory: llm-observability
tagline: Instrument your LLM application, investigate traces, and monitor performance in production.
description: LangSmith is a platform from LangChain for observability, evaluation, prompt engineering and deployment of LLM applications and agents. It records traces of what an application did, supports datasets and evaluations built from those traces, and works with many frameworks and providers, with or without LangChain code.
best_for: Tracing and debugging LLM applications and agents, Evaluating LLM applications against datasets
key_features:
- Tracing of LLM calls and application steps
- Evaluation datasets and online evaluation rules
- Annotation queues and inline annotation for human feedback
- Dashboards and alerts for monitoring
- Prompt playground with prompt versioning
- Pytest plugin for datasets and evaluations as test cases
- Cloud, hybrid or self-hosted setup
use_cases:
- LLM application debugging
- Production LLM monitoring
- Evaluation experiment management
- Human feedback collection
pros:
- Works with or without LangChain code
- Integrates with LangChain and LangGraph
- Self-hosted option alongside the cloud service
language: Python
languages_supported:
- Python
- TypeScript
- Java
maintained_by: LangChain
license_note: 'LangSmith Python client: MIT'
github_url: https://github.com/langchain-ai/langsmith-python
docs_url: https://docs.langchain.com/langsmith/observability
website_url: https://smith.langchain.com/
backing:
  type: corporate
  orgs:
  - LangChain
alternatives:
- framework/promptfoo
- framework/deepeval
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 27
  downloads_monthly: 96211380
  latest_version: 0.15.1
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/langchain-ai/langsmith-python
aliases:
- langchain-ai/langsmith-sdk
- langchain-ai/langsmith-python
tags:
- evaluation
- observability
- debugging
- langchain
updated: '2026-11-21'
sources:
- url: https://github.com/langchain-ai/langsmith-python
  title: GitHub repository
- url: https://docs.langchain.com/langsmith/observability
  title: Documentation
- url: https://docs.langchain.com/langsmith/home
  title: LangSmith Observability - Docs by LangChain
- url: https://docs.langchain.com/langsmith/observability-quickstart
  title: Tracing quickstart
- url: https://docs.langchain.com/langsmith/prompt-engineering
  title: Prompt engineering
- url: https://pypi.org/project/langsmith/
  title: langsmith — PyPI
---


