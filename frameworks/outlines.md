---
id: framework/outlines
type: framework
slug: outlines
schema_version: 3.0
title: Outlines
status: curated
kind: library
category: framework-category/llm-frameworks
subcategory: structured-generation
tagline: Outlines guarantees structured outputs during generation, directly from any LLM.
description: Outlines is a Python library that constrains LLM output during generation to a requested type such as a set of choices, a Pydantic model or JSON schema, a regular expression or a context-free grammar. The same code runs across model providers and inference engines, including transformers, llama.cpp, vLLM, Ollama, OpenAI and Gemini.
best_for: Structured outputs from LLMs, Extracting typed data from text
key_features:
- Constrained decoding through logits processors
- JSON Schema and Pydantic output types
- Regex-guided generation
- Context-free grammar generation
- Integration with vLLM and transformers
- Prompt templates
use_cases:
- Structured data extraction
- JSON generation from LLMs
- Classification into predefined categories
- Function calling from typed signatures
pros:
- Output structure enforced during generation rather than parsed afterwards
- Same code across model providers and inference engines
language: Python
languages_supported:
- Python
maintained_by: .txt
license_spdx: Apache-2.0
github_url: https://github.com/dottxt-ai/outlines
docs_url: https://dottxt-ai.github.io/outlines/
website_url: https://dottxt.co/
maturity: stable
backing:
  type: corporate
  orgs:
  - .txt
alternatives:
- framework/guidance
ecosystem_connections:
- framework/vllm
- framework/hugging-face-transformers
registry_signals:
  github_stars: 16016
  downloads_monthly: 1409867
  latest_version: 1.3.3
  latest_release_date: '2026-08-06'
  observed_at: '2026-11-20'
  source: https://github.com/dottxt-ai/outlines
aliases:
- dottxt-ai/outlines
tags:
- llm
- structured-generation
- json
- constrained-decoding
updated: '2026-11-21'
sources:
- url: https://github.com/dottxt-ai/outlines
  title: GitHub repository
- url: https://dottxt-ai.github.io/outlines/
  title: Documentation
- url: https://dottxt-ai.github.io/outlines/latest/features/models/
  title: Models
- url: https://pypi.org/project/outlines/
  title: outlines — PyPI
---


