---
id: framework/crewai
type: framework
slug: crewai
schema_version: 1.1
title: CrewAI
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Framework for orchestrating role-playing, autonomous AI agents.
description: CrewAI is an open-source Python framework with high-level abstractions and low-level APIs for building multi-agent workflows. Crews are teams of role-based AI agents that collaborate and delegate tasks, and Flows are event-driven workflows with state, branching and routing for precise control. It is a standalone framework with its own primitives for agents, tasks, crews, flows, tools and orchestration.
best_for: Role-based multi-agent collaboration, Event-driven agent workflows that combine autonomy with explicit business logic
key_features:
- Role-based agents with goals, backstories and tools
- Task delegation and collaboration between agents
- Sequential and hierarchical processes
- Event-driven Flows with state, branching and routing
- Memory, knowledge and checkpointing
- MCP and A2A support
- Human input and structured outputs
- CrewAI Toolkit and LangChain Tools for agents
use_cases:
- Trip planning
- Stock analysis
- Writing job descriptions
- Landing page generation
- Multi-step automations that combine agents with deterministic steps
pros:
- Combines autonomous Crews with event-driven Flows
- Standalone framework with its own primitives
- Uses the OpenAI API by default and supports local models through Ollama
cons:
- Collects anonymous telemetry by default (disabled with the OTEL_SDK_DISABLED variable)
- Managed deployment and the tracing control plane are part of the commercial CrewAI AMP Suite
language: Python
languages_supported:
- Python
maintained_by: CrewAI Inc.
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
maturity: stable
backing:
  type: corporate
  orgs:
  - CrewAI Inc
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
updated: '2026-11-21'
sources:
- url: https://github.com/crewAIInc/crewAI
  title: GitHub repository
- url: https://docs.crewai.com/
  title: Documentation
- url: https://docs.crewai.com/en/concepts/tools
  title: Tools
- url: https://pypi.org/project/crewai/
  title: crewai — PyPI
---

## Overview

CrewAI is an open-source Python framework with high-level abstractions and low-level APIs for building multi-agent workflows. Crews are teams of role-based AI agents that collaborate and delegate tasks, and Flows are event-driven workflows with state, branching and routing for precise control. It is a standalone framework with its own primitives for agents, tasks, crews, flows, tools and orchestration.
