---
id: framework/crewai
type: framework
slug: crewai
schema_version: 1.1
title: CrewAI
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Framework for orchestrating role-playing autonomous AI agents
description: Multi-agent orchestration framework where agents take on roles (researcher, writer, analyst) and collaborate to complete tasks. Emphasizes simplicity and role-based agent design. Built on top of LangChain.
best_for: Quick multi-agent prototypes, role-based collaboration workflows
not_ideal_for: Production systems requiring deterministic behavior, complex state machines
key_features:
- Role-based agent design
- Task delegation and collaboration
- Tool integration for agents
- Sequential and hierarchical process flows
- Memory and context sharing between agents
use_cases:
- Multi-agent research workflows
- Content generation pipelines
- Data analysis with specialized agents
- Automated business processes
pros:
- Simple and intuitive API
- Good for role-based multi-agent setups
- Active development
cons:
- Limited control over agent internals
- Can be unpredictable with complex workflows
- LangChain dependency
language: Python
languages_supported:
- Python
maintained_by: CrewAI Inc.
first_release: '2023-12-01'
license_spdx: MIT
github_url: https://github.com/crewAIInc/crewAI
docs_url: https://docs.crewai.com/
website_url: https://www.crewai.com/
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
  - CrewAI Inc
  funding_or_parent: Seed $18M led by Insight Partners (Oct 2024)
alternatives:
- framework/autogen
ecosystem_connections:
- framework/langchain
registry_signals:
  github_stars: 61126
  downloads_monthly: 2571825
  latest_version: 1.15.44
  latest_release_date: '2026-11-19'
  observed_at: '2026-11-20'
  source: https://github.com/crewAIInc/crewAI
aliases:
- crewAIInc/crewAI
tags:
- llm
- agents
- multi-agent
- orchestration
updated: '2026-11-20'
sources:
- url: https://github.com/crewAIInc/crewAI
  title: GitHub repository
- url: https://docs.crewai.com/
  title: Documentation
---

## Overview

Multi-agent orchestration framework where agents take on roles (researcher, writer, analyst) and collaborate to complete tasks. Emphasizes simplicity and role-based agent design. Built on top of LangChain.
