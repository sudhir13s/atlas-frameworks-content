---
id: framework/haystack
type: framework
slug: haystack
schema_version: 1.1
title: Haystack
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: LLM framework for building production-ready AI applications
description: deepset's open-source framework for building AI-powered applications. Pipeline-based architecture for composing LLM components. Strong focus on retrieval and RAG with good production patterns.
best_for: Production RAG applications with clean architecture
not_ideal_for: Quick prototyping (LangChain is faster), agent-heavy use cases
key_features:
- Pipeline-based architecture
- Strong RAG capabilities
- Composable components
- Multiple retriever backends
- Document store abstractions
- Evaluation tools
use_cases:
- RAG applications
- Document search and Q&A
- Production LLM pipelines
pros:
- Clean pipeline architecture
- Good production patterns
- Strong retrieval focus
- Well-documented
cons:
- Smaller community than LangChain
- Less flexible for non-pipeline use cases
- Haystack 2.x was a major rewrite
language: Python
languages_supported:
- Python
maintained_by: deepset
first_release: '2020-01-01'
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
learning_curve: medium
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - deepset
  funding_or_parent: Series B $30M led by Balderton Capital (2024)
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
updated: '2026-11-20'
sources:
- url: https://github.com/deepset-ai/haystack
  title: GitHub repository
- url: https://docs.haystack.deepset.ai/
  title: Documentation
---

## Overview

deepset's open-source framework for building AI-powered applications. Pipeline-based architecture for composing LLM components. Strong focus on retrieval and RAG with good production patterns.
