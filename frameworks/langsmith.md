---
id: framework/langsmith
type: framework
slug: langsmith
schema_version: 1.1
title: LangSmith
kind: tool
category: framework-category/evaluation
subcategory: llm-observability
tagline: LangChain's platform for debugging, testing, evaluating, and monitoring LLM applications
description: LangChain's observability and evaluation platform. Provides tracing, debugging, dataset management, and evaluation for LLM applications. Works with LangChain but also supports any LLM framework via the SDK.
best_for: LangChain teams wanting integrated observability and evaluation
not_ideal_for: Teams not using LangChain, self-hosted requirements
key_features:
- LLM call tracing and debugging
- Evaluation datasets and experiments
- Online evaluation in production
- Annotation queues for human feedback
- Prompt playground
- Integration with LangChain and LangGraph
use_cases:
- LLM application debugging
- Production LLM monitoring
- Evaluation experiment management
- Human feedback collection
pros:
- Tight LangChain integration
- Good tracing UI
- Evaluation experiment management
- Free tier available
cons:
- SaaS dependency
- Best experience requires LangChain
- Can be expensive at scale
language: Python
languages_supported:
- Python
- TypeScript
maintained_by: LangChain Inc.
first_release: '2023-07-01'
license_note: 'Proprietary (client: MIT)'
github_url: https://github.com/langchain-ai/langsmith-sdk
docs_url: https://docs.smith.langchain.com/
website_url: https://smith.langchain.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: large
maturity: production
signal_strength: high
backing:
  type: corporate
  orgs:
  - LangChain Inc
  funding_or_parent: Part of LangChain (Series A $25M Sequoia 2024)
alternatives:
- framework/promptfoo
- framework/deepeval
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 1500
  downloads_monthly: 5000000
  latest_version: '0.2'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/langchain-ai/langsmith-sdk
aliases:
- langchain-ai/langsmith-sdk
tags:
- evaluation
- observability
- debugging
- langchain
updated: '2026-11-19'
sources:
- url: https://github.com/langchain-ai/langsmith-sdk
  title: GitHub repository
- url: https://docs.smith.langchain.com/
  title: Documentation
---

## Overview

LangChain's observability and evaluation platform. Provides tracing, debugging, dataset management, and evaluation for LLM applications. Works with LangChain but also supports any LLM framework via the SDK.
