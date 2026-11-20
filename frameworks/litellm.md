---
id: framework/litellm
type: framework
slug: litellm
schema_version: 1.1
title: LiteLLM
kind: library
category: framework-category/llm-frameworks
subcategory: llm-gateway
tagline: Call all LLM APIs using the OpenAI format — unified interface for 100+ providers
description: Unified interface for calling 100+ LLM providers (OpenAI, Anthropic, Cohere, local models) using the OpenAI API format. Provides load balancing, fallbacks, spend tracking, and rate limiting. The universal LLM gateway.
best_for: Applications needing to support multiple LLM providers with one API
not_ideal_for: Single-provider applications, provider-specific feature needs
key_features:
- Unified OpenAI-format API for 100+ providers
- Load balancing and fallback routing
- Spend tracking and budgeting
- Rate limiting
- Proxy server mode
- Streaming support
use_cases:
- Multi-provider LLM routing
- Cost optimization across LLM providers
- LLM gateway for applications
- Provider failover and load balancing
pros:
- Simplest way to support multiple LLM providers
- Drop-in OpenAI replacement
- Good cost tracking
- Active development
cons:
- Another abstraction layer
- Provider-specific features may not be fully supported
- Proxy mode adds latency
language: Python
languages_supported:
- Python
maintained_by: BerriAI
first_release: '2023-08-01'
license_spdx: MIT
github_url: https://github.com/BerriAI/litellm
docs_url: https://docs.litellm.ai/
website_url: https://www.litellm.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: very-low
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - BerriAI
  funding_or_parent: Seed $1.6M led by Gravity Fund + YC W23
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 63602
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
updated: '2026-11-20'
sources:
- url: https://github.com/BerriAI/litellm
  title: GitHub repository
- url: https://docs.litellm.ai/
  title: Documentation
---

## Overview

Unified interface for calling 100+ LLM providers (OpenAI, Anthropic, Cohere, local models) using the OpenAI API format. Provides load balancing, fallbacks, spend tracking, and rate limiting. The universal LLM gateway.
