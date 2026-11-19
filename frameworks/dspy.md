---
id: framework/dspy
type: framework
slug: dspy
schema_version: 1.1
title: DSPy
kind: framework
category: framework-category/llm-frameworks
subcategory: prompt-optimization
tagline: Programming—not prompting—foundation models
description: Stanford research framework that replaces manual prompt engineering with programmatic optimization. Defines LLM modules as typed signatures, then automatically optimizes prompts and few-shot examples using a compiler. A paradigm shift from manual prompting.
best_for: Teams wanting systematic prompt optimization over manual engineering
not_ideal_for: Simple LLM calls, teams wanting quick prototypes without learning new paradigm
key_features:
- Typed signatures for LLM modules
- Automatic prompt optimization (compile)
- Few-shot example bootstrapping
- Chain-of-thought and ReAct patterns as composable modules
- Metric-driven optimization
- Model-agnostic — works with any LLM
use_cases:
- Systematic prompt optimization
- LLM pipeline development
- Research on LLM programming
- Building reliable LLM systems
pros:
- Eliminates manual prompt engineering
- Reproducible LLM behavior
- Composable modular design
- Research-backed optimization
cons:
- Steep conceptual learning curve
- Optimization can be slow and expensive
- Smaller community than LangChain
language: Python
languages_supported:
- Python
maintained_by: Stanford NLP (Omar Khattab)
first_release: '2023-08-01'
license_spdx: MIT
github_url: https://github.com/stanfordnlp/dspy
docs_url: https://dspy-docs.vercel.app/
website_url: https://dspy-docs.vercel.app/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: high
community_size: medium
maturity: stable
signal_strength: high
backing:
  type: foundation
  orgs:
  - Stanford NLP
  funding_or_parent: Stanford NLP (led by Omar Khattab)
alternatives:
- framework/langchain
- framework/guidance
- framework/outlines
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 22000
  downloads_monthly: 1000000
  latest_version: '2.6'
  latest_release_date: '2025-02-01'
  observed_at: '2026-06-15'
  source: https://github.com/stanfordnlp/dspy
aliases:
- stanfordnlp/dspy
tags:
- llm
- prompt-optimization
- research
- programming-over-prompting
updated: '2026-11-19'
sources:
- url: https://github.com/stanfordnlp/dspy
  title: GitHub repository
- url: https://dspy-docs.vercel.app/
  title: Documentation
---

## Overview

Stanford research framework that replaces manual prompt engineering with programmatic optimization. Defines LLM modules as typed signatures, then automatically optimizes prompts and few-shot examples using a compiler. A paradigm shift from manual prompting.
