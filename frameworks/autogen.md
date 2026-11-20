---
id: framework/autogen
type: framework
slug: autogen
schema_version: 1.1
title: AutoGen
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Multi-agent conversation framework by Microsoft Research
description: Microsoft Research framework for building multi-agent systems where agents communicate through conversations. Supports human-in-the-loop, code execution, and complex multi-agent topologies. AutoGen v0.4 is a complete rewrite with an event-driven architecture.
best_for: Research teams exploring multi-agent architectures, Microsoft ecosystem
not_ideal_for: Production systems needing stability, simple single-agent tasks
key_features:
- Conversational multi-agent framework
- Human-in-the-loop patterns
- Code execution sandboxing
- Group chat topologies
- Event-driven architecture (v0.4)
- Flexible agent communication patterns
use_cases:
- Multi-agent code generation
- Research assistant systems
- Human-AI collaborative workflows
- Complex reasoning chains
pros:
- Flexible agent communication patterns
- Good for research and experimentation
- Microsoft Research backing
- v0.4 event-driven rewrite is promising
cons:
- Major API changes between versions
- Complex setup for production use
- Agent behavior can be unpredictable
language: Python
languages_supported:
- Python
- .NET
maintained_by: Microsoft Research
first_release: '2023-09-01'
license_spdx: MIT
github_url: https://github.com/microsoft/autogen
docs_url: https://microsoft.github.io/autogen/
website_url: https://microsoft.github.io/autogen/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium-high
community_size: large
maturity: stable
signal_strength: high
backing:
  type: corporate
  orgs:
  - Microsoft
  funding_or_parent: Microsoft Research
alternatives:
- framework/crewai
registry_signals:
  github_stars: 61955
  downloads_monthly: 2000000
  latest_version: python-v0.7.5
  latest_release_date: '2025-09-30'
  observed_at: '2026-11-20'
  source: https://github.com/microsoft/autogen
aliases:
- microsoft/autogen
tags:
- llm
- agents
- multi-agent
- research
- microsoft
updated: '2026-11-20'
sources:
- url: https://github.com/microsoft/autogen
  title: GitHub repository
- url: https://microsoft.github.io/autogen/
  title: Documentation
---

## Overview

Microsoft Research framework for building multi-agent systems where agents communicate through conversations. Supports human-in-the-loop, code execution, and complex multi-agent topologies. AutoGen v0.4 is a complete rewrite with an event-driven architecture.
