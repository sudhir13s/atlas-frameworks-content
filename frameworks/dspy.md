---
id: framework/dspy
type: framework
slug: dspy
schema_version: 1.1
title: DSPy
kind: framework
category: framework-category/llm-frameworks
subcategory: prompt-optimization
tagline: The framework for programming—not prompting—language models.
description: DSPy is a Python framework for programming, rather than prompting, language models. Tasks are declared as signatures with typed inputs and outputs, modules control how a signature executes, and optimizers tune prompts and weights against a metric. It is used to build modular AI systems from simple classifiers to RAG pipelines and agent loops.
best_for: Building modular AI systems, Optimizing prompts and weights against a metric
key_features:
- Typed signatures for LLM modules
- Automatic prompt optimization (compile)
- Few-shot example bootstrapping
- Chain-of-thought and ReAct patterns as composable modules
- Metric-driven optimization
- Connects to multiple LM providers through dspy.LM
use_cases:
- Systematic prompt optimization
- LLM pipeline development
- RAG pipelines and agent loops
pros:
- Tasks declared as signatures instead of prompt strings
- Modules compose with plain Python control flow
- Optimizers such as GEPA and MIPROv2 come from published papers
language: Python
languages_supported:
- Python
maintained_by: Stanford NLP
license_spdx: MIT
github_url: https://github.com/stanfordnlp/dspy
docs_url: https://dspy.ai/
website_url: https://dspy-docs.vercel.app/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
maturity: experimental
alternatives:
- framework/langchain
- framework/guidance
- framework/outlines
ecosystem_connections:
- framework/ollama
registry_signals:
  github_stars: 39152
  downloads_monthly: 5976761
  latest_version: 3.5.0
  latest_release_date: '2026-11-10'
  observed_at: '2026-11-20'
  source: https://github.com/stanfordnlp/dspy
aliases:
- stanfordnlp/dspy
tags:
- llm
- prompt-optimization
- research
- programming-over-prompting
updated: '2026-11-21'
sources:
- url: https://github.com/stanfordnlp/dspy
  title: GitHub repository
- url: https://dspy.ai/
  title: Documentation
- url: https://dspy.ai/current/getting-started/installation/
  title: Documentation — Setting up DSPy
- url: https://pypi.org/project/dspy/
  title: dspy — PyPI
---

## Overview

DSPy is a Python framework for programming, rather than prompting, language models. Tasks are declared as signatures with typed inputs and outputs, modules control how a signature executes, and optimizers tune prompts and weights against a metric. It is used to build modular AI systems from simple classifiers to RAG pipelines and agent loops.
