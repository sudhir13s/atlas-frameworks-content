---
id: framework/ragas
type: framework
slug: ragas
schema_version: 1.1
title: Ragas
kind: framework
category: framework-category/evaluation
subcategory: rag-evaluation
tagline: Evaluation framework for RAG pipelines — measure retrieval and generation quality
description: Framework for evaluating Retrieval Augmented Generation (RAG) pipelines. Provides metrics like faithfulness, answer relevancy, context precision, and context recall. Essential for measuring RAG quality without manual evaluation.
best_for: Evaluating and improving RAG pipeline quality
not_ideal_for: Non-RAG LLM evaluation, deterministic testing
key_features:
- Faithfulness scoring (hallucination detection)
- Answer relevancy metric
- Context precision and recall
- Synthetic test data generation
- LLM-as-judge evaluation
- Integration with LangChain and LlamaIndex
use_cases:
- RAG pipeline quality measurement
- Hallucination detection
- Retrieval quality evaluation
- RAG regression testing
pros:
- Purpose-built for RAG evaluation
- Good metric coverage
- Synthetic test data generation
cons:
- LLM-as-judge can be expensive
- Metrics are approximations — not ground truth
- Requires an evaluator LLM
language: Python
languages_supported:
- Python
maintained_by: Ragas team (Explodinggradients)
first_release: '2023-07-01'
license_spdx: Apache-2.0
github_url: https://github.com/explodinggradients/ragas
docs_url: https://docs.ragas.io/
website_url: https://ragas.io/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: medium
maturity: stable
signal_strength: high
backing:
  type: corporate
  orgs:
  - Exploding Gradients
  funding_or_parent: YC W24; seed funding from Y Combinator
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
tags:
- evaluation
- rag
- quality
- metrics
updated: '2026-11-20'
sources:
- url: https://github.com/explodinggradients/ragas
  title: GitHub repository
- url: https://docs.ragas.io/
  title: Documentation
---

## Overview

Framework for evaluating Retrieval Augmented Generation (RAG) pipelines. Provides metrics like faithfulness, answer relevancy, context precision, and context recall. Essential for measuring RAG quality without manual evaluation.
