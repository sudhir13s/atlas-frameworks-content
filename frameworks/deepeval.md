---
id: framework/deepeval
type: framework
slug: deepeval
schema_version: 1.1
title: DeepEval
kind: framework
category: framework-category/evaluation
subcategory: llm-evaluation
tagline: The LLM Evaluation Framework.
description: DeepEval is an open-source framework for evaluating LLM applications such as AI agents, voice agents, multi-turn chatbots and RAG pipelines. It is similar to Pytest but specialized for unit testing LLM apps, with metrics such as G-Eval, task completion, answer relevancy and hallucination that use LLM-as-a-judge and NLP models. Evals run in CI/CD or as Python scripts.
best_for: Unit testing LLM applications in CI/CD pipelines
key_features:
- pytest-like LLM testing interface
- Ready-to-use evaluation metrics with explanations
- Hallucination detection
- Bias and toxicity detection
- Synthetic dataset generation
use_cases:
- LLM output quality testing
- CI/CD for LLM applications
- Hallucination and toxicity testing
- LLM regression testing
pros:
- Pytest-native test interface
- Each metric score comes with an explanation
- Runs in any CI/CD environment
language: Python
languages_supported:
- Python
- TypeScript
maintained_by: Confident AI
license_spdx: Apache-2.0
github_url: https://github.com/confident-ai/deepeval
docs_url: https://deepeval.com/
website_url: https://www.confident-ai.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
backing:
  type: corporate
  orgs:
  - Confident AI
alternatives:
- framework/ragas
- framework/promptfoo
- framework/langsmith
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 19577
  downloads_monthly: 3405253
  latest_version: 4.3.4
  latest_release_date: '2026-11-11'
  observed_at: '2026-11-20'
  source: https://github.com/confident-ai/deepeval
aliases:
- confident-ai/deepeval
tags:
- evaluation
- llm
- testing
- ci-cd
updated: '2026-11-21'
sources:
- url: https://github.com/confident-ai/deepeval
  title: GitHub repository
- url: https://deepeval.com/
  title: Documentation
- url: https://deepeval.com/docs/getting-started
  title: Documentation — Getting started
- url: https://pypi.org/project/deepeval/
  title: deepeval — PyPI
---

## Overview

DeepEval is an open-source framework for evaluating LLM applications such as AI agents, voice agents, multi-turn chatbots and RAG pipelines. It is similar to Pytest but specialized for unit testing LLM apps, with metrics such as G-Eval, task completion, answer relevancy and hallucination that use LLM-as-a-judge and NLP models. Evals run in CI/CD or as Python scripts.
