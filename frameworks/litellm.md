---
id: framework/litellm
type: framework
slug: litellm
schema_version: 1.1
title: LiteLLM
kind: library
category: framework-category/llm-frameworks
subcategory: llm-gateway
tagline: AI Gateway with a Rust core and Python SDK. Call 100+ LLM APIs in OpenAI (or native) format with cost tracking, guardrails, load balancing, and logging.
description: LiteLLM is an open source AI gateway that gives a single, unified interface to call LLM providers such as OpenAI, Anthropic, Gemini, Bedrock and Azure using the OpenAI format. It can be used as a Python SDK inside an application or deployed as an AI Gateway (proxy server) for a team or organization, with virtual keys, spend tracking, guardrails and load balancing.
best_for: Calling multiple LLM providers through one OpenAI-format API, Central LLM gateway for ML platform teams
key_features:
- Unified OpenAI-format API across LLM providers
- Router with retry and fallback logic across deployments
- Load balancing
- Virtual keys with budgets and rate limits
- Spend tracking per project and user
- Proxy server (AI Gateway) with admin dashboard
- Streaming support
- MCP gateway and A2A agent support
use_cases:
- Multi-provider LLM routing
- Cost tracking across LLM providers
- LLM gateway for applications
- Provider failover and load balancing
pros:
- OpenAI-compatible interface across providers
- Usable as a Python library or as a self-hosted gateway
- Per-request cost tracking
cons:
- Features under litellm/enterprise/ require the LiteLLM Commercial License
language: Python
languages_supported:
- Python
maintained_by: Berri AI
github_url: https://github.com/BerriAI/litellm
docs_url: https://docs.litellm.ai/
website_url: https://www.litellm.ai/
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
  - Berri AI
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 63610
  downloads_monthly: 100162170
  latest_version: 1.110.2
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-20'
  source: https://github.com/BerriAI/litellm
aliases:
- BerriAI/litellm
tags:
- llm
- gateway
- multi-provider
- routing
updated: '2026-11-21'
sources:
- url: https://github.com/BerriAI/litellm
  title: GitHub repository
- url: https://docs.litellm.ai/
  title: Documentation
- url: https://pypi.org/project/litellm/
  title: litellm — PyPI
license_note: MIT, except content under litellm/enterprise/, which is under the licence in litellm/enterprise/LICENSE
---

## Overview

LiteLLM is an open source AI gateway that gives a single, unified interface to call LLM providers such as OpenAI, Anthropic, Gemini, Bedrock and Azure using the OpenAI format. It can be used as a Python SDK inside an application or deployed as an AI Gateway (proxy server) for a team or organization, with virtual keys, spend tracking, guardrails and load balancing.
