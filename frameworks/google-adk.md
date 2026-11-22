---
id: framework/google-adk
type: framework
slug: google-adk
schema_version: 1.1
title: Agent Development Kit (ADK)
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: An open-source, code-first Python toolkit for building, evaluating, and deploying AI agents.
description: Open-source, code-first framework from Google for building, evaluating and deploying AI agents. It provides a graph-based workflow runtime, multi-agent hierarchies, agent-to-agent task delegation, and tools from custom functions, OpenAPI specs or MCP. It is optimized for Gemini but is model-agnostic and deployment-agnostic.
best_for: Building AI agents in code, Multi-agent systems, Agents built on Gemini
key_features:
- Graph-based workflow runtime with routing, loops and human-in-the-loop steps
- Multi-agent hierarchies with sub-agent delegation
- Tools from custom functions, OpenAPI specs and MCP
- Bidirectional text and audio streaming for live agents
- Agent evaluation from the CLI or the development UI
- Built-in development web UI
- Deployment to Cloud Run or Agent Runtime
use_cases:
- Gemini-powered agent applications
- Multi-agent orchestration
- Live and voice agents
- Agents deployed on Google Cloud
pros:
- Model adapters for other providers including locally running models
- Built-in evaluation tooling
- Official SDKs for Python, TypeScript, Go, Java and Kotlin
language: Python
languages_supported:
- Python
- TypeScript
- Go
- Java
- Kotlin
maintained_by: Google
license_spdx: Apache-2.0
github_url: https://github.com/google/adk-python
docs_url: https://adk.dev/
website_url: https://adk.dev/
maturity: stable
backing:
  type: corporate
  orgs:
  - Google
alternatives:
- framework/langchain
- framework/crewai
- framework/autogen
registry_signals:
  github_stars: 22279
  downloads_monthly: 11094886
  latest_version: 2.15.0
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/google/adk-python
aliases:
- google/adk-python
- Google ADK
tags:
- llm
- agents
- multi-agent
- google
- gemini
- vertex-ai
updated: '2026-11-21'
sources:
- url: https://github.com/google/adk-python
  title: GitHub repository
- url: https://adk.dev/
  title: Documentation
- url: https://adk.dev/get-started/about/
  title: About ADK
- url: https://pypi.org/project/google-adk/
  title: google-adk — PyPI
---

## Overview

Open-source, code-first framework from Google for building, evaluating and deploying AI agents. It provides a graph-based workflow runtime, multi-agent hierarchies, agent-to-agent task delegation, and tools from custom functions, OpenAPI specs or MCP. It is optimized for Gemini but is model-agnostic and deployment-agnostic.
