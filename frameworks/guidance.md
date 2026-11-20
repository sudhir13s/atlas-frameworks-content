---
id: framework/guidance
type: framework
slug: guidance
schema_version: 1.1
title: Guidance
kind: library
category: framework-category/llm-frameworks
subcategory: structured-generation
tagline: A guidance language for controlling LLMs — constrained generation
description: Microsoft Research library for constrained LLM generation. Interleaves generation with Python control flow, enforcing output structure with grammar-based constraints. Produces guaranteed-valid JSON, regex-matching strings, and structured data.
best_for: Applications requiring guaranteed structured output from LLMs
not_ideal_for: Free-form generation, chat applications
key_features:
- Grammar-based constrained generation
- Guaranteed valid JSON output
- Interleaved Python control flow
- Token-level healing
- Regex and CFG constraints
use_cases:
- Structured data extraction from LLMs
- Guaranteed-format output generation
- Template-based LLM applications
pros:
- Guarantees output format compliance
- Fast — works at token generation level
- Elegant template syntax
cons:
- Requires model-specific integration
- Not all models supported equally
- Smaller ecosystem than alternatives
language: Python
languages_supported:
- Python
maintained_by: Microsoft Research
first_release: '2023-03-01'
license_spdx: MIT
github_url: https://github.com/guidance-ai/guidance
docs_url: https://github.com/guidance-ai/guidance
website_url: https://github.com/guidance-ai/guidance
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Microsoft
  funding_or_parent: Microsoft Research
alternatives:
- framework/outlines
- framework/dspy
ecosystem_connections:
- framework/llama-cpp
- framework/hugging-face-transformers
registry_signals:
  github_stars: 21827
  downloads_monthly: 14672
  latest_version: 0.3.1
  latest_release_date: '2026-02-03'
  observed_at: '2026-11-20'
  source: https://github.com/guidance-ai/guidance
aliases:
- guidance-ai/guidance
tags:
- llm
- structured-generation
- constrained-decoding
updated: '2026-11-20'
sources:
- url: https://github.com/guidance-ai/guidance
  title: GitHub repository
---

## Overview

Microsoft Research library for constrained LLM generation. Interleaves generation with Python control flow, enforcing output structure with grammar-based constraints. Produces guaranteed-valid JSON, regex-matching strings, and structured data.
