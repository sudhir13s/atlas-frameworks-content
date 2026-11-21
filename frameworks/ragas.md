---
id: framework/ragas
type: framework
slug: ragas
schema_version: 1.1
title: Ragas
kind: framework
category: framework-category/evaluation
subcategory: rag-evaluation
tagline: Toolkit for evaluating and optimizing Large Language Model (LLM) applications.
description: Ragas is a toolkit for evaluating and optimizing LLM applications. It provides LLM-based and traditional metrics for retrieval augmented generation (RAG), agents and tool use, SQL and general-purpose evaluation, and it generates test datasets for RAG and agent scenarios.
best_for: Evaluating RAG pipelines, Evaluating LLM applications and agents
key_features:
- Faithfulness metric
- Response relevancy metric
- Context precision and recall
- Synthetic test data generation
- Aspect critic and rubric-based LLM metrics
- Agent and tool use metrics
- Integration with LangChain and LlamaIndex
use_cases:
- RAG pipeline quality measurement
- Retrieval quality evaluation
- Agent evaluation
- Text-to-SQL evaluation
- Prompt evaluation
pros:
- LLM-based and traditional metrics in one library
- Test set generation for RAG and agent scenarios
- Integrations with LLM frameworks and observability tools
cons:
- Collects anonymized usage data unless RAGAS_DO_NOT_TRACK is set
language: Python
languages_supported:
- Python
maintained_by: Vibrant Labs
license_spdx: Apache-2.0
github_url: https://github.com/vibrantlabsai/ragas
docs_url: https://docs.ragas.io/
website_url: https://ragas.io/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: corporate
  orgs:
  - Vibrant Labs
alternatives:
- framework/deepeval
- framework/langsmith
ecosystem_connections:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 16388
  downloads_monthly: 1000000
  latest_version: 0.4.4
  latest_release_date: '2026-11-14'
  observed_at: '2026-11-20'
  source: https://github.com/explodinggradients/ragas
aliases:
- explodinggradients/ragas
- vibrantlabsai/ragas
tags:
- evaluation
- rag
- quality
- metrics
updated: '2026-11-21'
sources:
- url: https://github.com/vibrantlabsai/ragas
  title: GitHub repository
- url: https://docs.ragas.io/
  title: Documentation
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
  title: List of available metrics
- url: https://github.com/vibrantlabsai
  title: Vibrant Labs on GitHub
- url: https://pypi.org/project/ragas/
  title: ragas — PyPI
---

## Overview

Ragas is a toolkit for evaluating and optimizing LLM applications. It provides LLM-based and traditional metrics for retrieval augmented generation (RAG), agents and tool use, SQL and general-purpose evaluation, and it generates test datasets for RAG and agent scenarios.
