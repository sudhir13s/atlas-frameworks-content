---
id: framework/deepeval
type: framework
slug: deepeval
schema_version: 1.1
title: DeepEval
kind: framework
category: framework-category/evaluation
subcategory: llm-evaluation
tagline: Open-source LLM evaluation framework — unit testing for LLM outputs
description: Open-source framework for evaluating LLM applications with a pytest-like interface. Provides 14+ metrics for hallucination, relevancy, bias, toxicity, and more. Treats LLM testing like unit testing.
best_for: Unit testing LLM applications in CI/CD pipelines
not_ideal_for: Large-scale offline evaluation, non-LLM ML testing
key_features:
- pytest-like LLM testing interface
- 14+ evaluation metrics
- Hallucination detection
- Bias and toxicity detection
- Red teaming for adversarial testing
- Synthetic dataset generation
use_cases:
- LLM output quality testing
- CI/CD for LLM applications
- Hallucination and safety testing
- LLM regression testing
pros:
- Familiar pytest-like interface
- Comprehensive metric library
- Good for CI/CD integration
cons:
- LLM-based metrics require API calls
- Confident AI platform adds vendor dependency
- Some metrics are noisy
language: Python
languages_supported:
- Python
maintained_by: Confident AI
first_release: '2023-09-01'
license_spdx: Apache-2.0
github_url: https://github.com/confident-ai/deepeval
docs_url: https://docs.confident-ai.com/
website_url: https://www.confident-ai.com/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Confident AI
  funding_or_parent: YC S23
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
updated: '2026-11-20'
sources:
- url: https://github.com/confident-ai/deepeval
  title: GitHub repository
- url: https://docs.confident-ai.com/
  title: Documentation
---

## Overview

Open-source framework for evaluating LLM applications with a pytest-like interface. Provides 14+ metrics for hallucination, relevancy, bias, toxicity, and more. Treats LLM testing like unit testing.
