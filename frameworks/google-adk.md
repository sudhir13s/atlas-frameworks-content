---
id: framework/google-adk
type: framework
slug: google-adk
schema_version: 1.1
title: Google ADK
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Google's open-source framework for building multi-agent systems on Gemini and Vertex AI.
description: Agent Development Kit (ADK) is Google's open-source multi-agent framework announced at Cloud Next 2025. Provides primitives for building, orchestrating, and evaluating agents with native Gemini and Vertex AI integration. Supports tool use, sub-agents, streaming, and agent evaluation. Python is primary; Java support is also available.
best_for: Teams building on Gemini/Vertex AI who want a first-party multi-agent framework
not_ideal_for: Non-Google stacks, teams needing a long-stable API
key_features:
- Native Gemini and Vertex AI integration
- Multi-agent orchestration with sub-agents
- Tool use and function calling
- Streaming agent responses
- Built-in agent evaluation framework
- Python and Java implementations
use_cases:
- Gemini-powered agent applications
- Vertex AI production agents
- Multi-agent orchestration on GCP
- Enterprise agent systems on Google Cloud
pros:
- First-party from Google with direct Gemini/Vertex integration
- Clean multi-agent primitives
- Built-in evaluation tooling
- Strong Google Cloud ecosystem fit
cons:
- New release — API still evolving
- Strongest when you're already on Gemini/Vertex
- Smaller community than LangChain/AutoGen
language: Python
languages_supported:
- Python
- Java
maintained_by: Google
first_release: '2025-04-09'
license_spdx: Apache-2.0
github_url: https://github.com/google/adk-python
docs_url: https://google.github.io/adk-docs/
website_url: https://google.github.io/adk-docs/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: experimental
signal_strength: high
backing:
  type: corporate
  orgs:
  - Google
  funding_or_parent: Google — announced at Cloud Next 2025
alternatives:
- framework/langchain
- framework/crewai
- framework/autogen
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 22277
  downloads_monthly: 11094886
  latest_version: 2.15.0
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/google/adk-python
aliases:
- google/adk-python
tags:
- llm
- agents
- multi-agent
- google
- gemini
- vertex-ai
updated: '2026-11-20'
sources:
- url: https://github.com/google/adk-python
  title: GitHub repository
- url: https://google.github.io/adk-docs/
  title: Documentation
---

## Overview

Agent Development Kit (ADK) is Google's open-source multi-agent framework announced at Cloud Next 2025. Provides primitives for building, orchestrating, and evaluating agents with native Gemini and Vertex AI integration. Supports tool use, sub-agents, streaming, and agent evaluation. Python is primary; Java support is also available.
