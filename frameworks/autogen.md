---
id: framework/autogen
type: framework
slug: autogen
schema_version: 3.0
title: AutoGen
status: curated
kind: framework
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: A programming framework for agentic AI.
description: AutoGen is a framework for creating multi-agent AI applications that can act autonomously or work alongside humans. Its layered design has a Core API for message passing and event-driven agents, an AgentChat API for common multi-agent patterns, and an Extensions API for LLM clients and capabilities such as code execution. The project has been archived and is no longer actively maintained by Microsoft, which points new users to Microsoft Agent Framework.
best_for: Research and experimentation with multi-agent orchestration patterns
not_ideal_for: Production use (Microsoft advises against it), New projects (Microsoft recommends Microsoft Agent Framework)
key_features:
- Agents that act autonomously or alongside humans
- Event-driven Core API with local and distributed runtimes
- AgentChat API for two-agent chat and group chats
- Extensions for LLM clients and code execution
- MCP server tools through McpWorkbench
- AutoGen Studio no-code GUI for multi-agent workflows
- AutoGen Bench benchmarking suite for agent performance
use_cases:
- Multi-agent prototypes for research
- Web browsing agents that use MCP servers
- No-code prototyping of multi-agent workflows in AutoGen Studio
pros:
- Layered APIs from high-level AgentChat to low-level Core
- Python and .NET packages
cons:
- This project has been archived and is no longer actively maintained by Microsoft
- Microsoft is not providing bug fixes, security fixes, new features, or support for this project
- AutoGen was developed for research and experimentation and Microsoft advises against production use
- AutoGen Studio is not meant to be a production-ready app
language: Python
languages_supported:
- Python
- .NET
maintained_by: Microsoft (archived, now community-managed)
license_spdx: MIT
github_url: https://github.com/microsoft/autogen
docs_url: https://microsoft.github.io/autogen/
website_url: https://microsoft.github.io/autogen/
maturity: experimental
backing:
  type: corporate
  orgs:
  - organization/microsoft
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
updated: '2026-11-21'
sources:
- url: https://github.com/microsoft/autogen
  title: GitHub repository
- url: https://microsoft.github.io/autogen/
  title: Documentation
- url: https://microsoft.github.io/autogen/stable/
  title: AutoGen documentation (stable)
- url: https://github.com/microsoft/autogen/blob/main/LICENSE-CODE
  title: AutoGen LICENSE-CODE
- url: https://pypi.org/project/autogen-agentchat/
  title: autogen-agentchat — PyPI
---


