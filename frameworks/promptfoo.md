---
id: framework/promptfoo
type: framework
slug: promptfoo
schema_version: 1.1
title: Promptfoo
kind: tool
category: framework-category/evaluation
subcategory: prompt-testing
tagline: Test and evaluate LLM outputs — prompt testing framework
description: Open-source tool for testing and evaluating LLM prompts. Define test cases, run them against multiple models, and compare results. Supports custom assertions, red teaming, and CI/CD integration.
best_for: Prompt testing, multi-model comparison, LLM red teaming
not_ideal_for: Deep RAG evaluation (use Ragas), Python-only teams
key_features:
- YAML-based test definitions
- Multi-model comparison
- Custom assertion functions
- Red teaming and adversarial testing
- Web UI for result comparison
- CI/CD integration
use_cases:
- Prompt regression testing
- Multi-model comparison
- LLM red teaming
- Prompt optimization
pros:
- Easy YAML-based test definitions
- Good multi-model comparison
- Red teaming built-in
- Nice web UI
cons:
- TypeScript-native (Python support is secondary)
- Less focused on RAG-specific metrics than Ragas
language: TypeScript
languages_supported:
- TypeScript
- Python
- CLI
maintained_by: Promptfoo
first_release: '2023-04-01'
license_spdx: MIT
github_url: https://github.com/promptfoo/promptfoo
docs_url: https://www.promptfoo.dev/docs/
website_url: https://www.promptfoo.dev/
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
  - Promptfoo Inc
  funding_or_parent: Seed $5M led by Andreessen Horowitz (2024)
alternatives:
- framework/deepeval
- framework/ragas
- framework/langsmith
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 5500
  downloads_monthly: 300000
  latest_version: '0.100'
  latest_release_date: '2025-02-15'
  observed_at: '2026-06-15'
  source: https://github.com/promptfoo/promptfoo
aliases:
- promptfoo/promptfoo
tags:
- evaluation
- prompt-testing
- red-teaming
- comparison
updated: '2026-11-19'
sources:
- url: https://github.com/promptfoo/promptfoo
  title: GitHub repository
- url: https://www.promptfoo.dev/docs/
  title: Documentation
---

## Overview

Open-source tool for testing and evaluating LLM prompts. Define test cases, run them against multiple models, and compare results. Supports custom assertions, red teaming, and CI/CD integration.
