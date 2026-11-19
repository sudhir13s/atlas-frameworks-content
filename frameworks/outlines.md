---
id: framework/outlines
type: framework
slug: outlines
schema_version: 1.1
title: Outlines
kind: library
category: framework-category/llm-frameworks
subcategory: structured-generation
tagline: Structured text generation with LLMs — guaranteed valid output
description: Library for structured generation from LLMs using finite-state machine based decoding. Guarantees outputs match a JSON schema, regex, or grammar. Works with any model through logit-level constrained sampling.
best_for: Production systems requiring guaranteed-format LLM output
not_ideal_for: Free-form creative generation
key_features:
- FSM-based constrained decoding
- JSON Schema enforcement
- Regex-guided generation
- Grammar-based generation (EBNF)
- Integration with vLLM and transformers
use_cases:
- Structured data extraction
- Reliable JSON generation from LLMs
- Type-safe LLM outputs
pros:
- Mathematical guarantees on output format
- Works with vLLM for high-throughput serving
- Clean API
cons:
- Can slow down generation with complex schemas
- Limited to text generation models
language: Python
languages_supported:
- Python
maintained_by: .txt (formerly Outlines-dev)
first_release: '2023-07-01'
license_spdx: Apache-2.0
github_url: https://github.com/dottxt-ai/outlines
docs_url: https://dottxt-ai.github.io/outlines/
website_url: https://dottxt.co/
gpu_support:
  nvidia_cuda: true
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: low-medium
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - .txt
  funding_or_parent: Formerly Outlines-dev; maintained by .txt (dottxt) with seed funding
alternatives:
- framework/guidance
ecosystem_connections:
- framework/vllm
- framework/hugging-face-transformers
registry_signals:
  github_stars: 10500
  downloads_monthly: 800000
  latest_version: '0.2'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/dottxt-ai/outlines
aliases:
- dottxt-ai/outlines
tags:
- llm
- structured-generation
- json
- constrained-decoding
updated: '2026-11-19'
sources:
- url: https://github.com/dottxt-ai/outlines
  title: GitHub repository
- url: https://dottxt-ai.github.io/outlines/
  title: Documentation
---

## Overview

Library for structured generation from LLMs using finite-state machine based decoding. Guarantees outputs match a JSON schema, regex, or grammar. Works with any model through logit-level constrained sampling.
