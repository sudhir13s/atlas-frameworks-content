---
id: framework/promptfoo
type: framework
slug: promptfoo
schema_version: 1.1
title: Promptfoo
kind: tool
category: framework-category/evaluation
subcategory: prompt-testing
tagline: Test your prompts, agents, and RAGs. Red teaming/pentesting/vulnerability scanning for AI. Declarative configs with command line and CI/CD integration.
description: Promptfoo is an open-source CLI and library for evaluating and red-teaming LLM apps. It runs declarative test cases against prompts, models and RAG pipelines, scores outputs with defined metrics, compares models side by side and scans applications for security vulnerabilities, from the command line, a library or CI/CD.
best_for: Prompt and model evaluation, LLM red teaming
key_features:
- Declarative test case configuration
- Side-by-side model and prompt comparison
- Assertions and custom metrics
- Automated red teaming and vulnerability scanning
- Web viewer for results
- CI/CD integration
- Code scanning for LLM-related security issues
use_cases:
- Prompt regression testing
- Multi-model comparison
- LLM red teaming
- RAG pipeline evaluation
pros:
- Evals run locally and call the configured providers
- Works with any LLM API or programming language
- Caching, concurrency and live reload for evaluations
language: TypeScript
languages_supported:
- TypeScript
- Python
maintained_by: Promptfoo (part of OpenAI)
license_spdx: MIT
github_url: https://github.com/promptfoo/promptfoo
docs_url: https://www.promptfoo.dev/docs/
website_url: https://www.promptfoo.dev/
backing:
  type: corporate
  orgs:
  - OpenAI
alternatives:
- framework/deepeval
- framework/ragas
- framework/langsmith
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 27488
  downloads_monthly: 5251379
  latest_version: 0.126.0
  latest_release_date: '2025-02-15'
  observed_at: '2026-11-20'
  source: https://github.com/promptfoo/promptfoo
aliases:
- promptfoo/promptfoo
tags:
- evaluation
- prompt-testing
- red-teaming
- comparison
updated: '2026-11-21'
sources:
- url: https://github.com/promptfoo/promptfoo
  title: GitHub repository
- url: https://www.promptfoo.dev/docs/
  title: Documentation
- url: https://www.promptfoo.dev/docs/intro/
  title: Intro
- url: https://pypi.org/project/promptfoo/
  title: promptfoo — PyPI
---

## Overview

Promptfoo is an open-source CLI and library for evaluating and red-teaming LLM apps. It runs declarative test cases against prompts, models and RAG pipelines, scores outputs with defined metrics, compares models side by side and scans applications for security vulnerabilities, from the command line, a library or CI/CD.
