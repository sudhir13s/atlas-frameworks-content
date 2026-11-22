---
id: framework/guidance
type: framework
slug: guidance
schema_version: 1.1
title: Guidance
kind: library
category: framework-category/llm-frameworks
subcategory: structured-generation
tagline: A guidance language for controlling large language models.
description: Python programming paradigm for steering language models. It constrains generation with regular expressions, context-free grammars and JSON schemas, and interleaves generation with control flow such as conditionals, loops and tool use. Backends include Transformers, llama.cpp and OpenAI.
best_for: Constraining LLM output to a regex or grammar, Generating JSON that matches a schema
key_features:
- Regular expression and context-free grammar constraints
- JSON generation from a JSON schema or Pydantic model
- Selection from a fixed list of options
- Generation interleaved with Python control flow
- Fast-forwarding of tokens fixed by the grammar
- Offline grammar testing with a mock model
- Jupyter notebook widget
use_cases:
- Structured JSON output from LLMs
- Multiple-choice answer selection
- Composing grammars for formats such as HTML
pros:
- Inserts tokens fixed by the grammar without a model forward pass
- Grammars can be tested locally without model API calls
cons:
- Full context-free grammar constraints need a backend with full Guidance support
language: Python
languages_supported:
- Python
maintained_by: Guidance maintainers (guidance-ai)
license_spdx: MIT
github_url: https://github.com/guidance-ai/guidance
docs_url: https://github.com/guidance-ai/guidance
website_url: https://github.com/guidance-ai/guidance
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
updated: '2026-11-21'
sources:
- url: https://github.com/guidance-ai/guidance
  title: GitHub repository
- url: https://pypi.org/project/guidance/
  title: guidance — PyPI
---

## Overview

Python programming paradigm for steering language models. It constrains generation with regular expressions, context-free grammars and JSON schemas, and interleaves generation with control flow such as conditionals, loops and tool use. Backends include Transformers, llama.cpp and OpenAI.
