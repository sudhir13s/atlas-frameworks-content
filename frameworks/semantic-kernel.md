---
id: framework/semantic-kernel
type: framework
slug: semantic-kernel
schema_version: 1.1
title: Semantic Kernel
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Integrate LLM technology into your apps.
description: Semantic Kernel is a model-agnostic, open-source SDK from Microsoft for building, orchestrating and deploying AI agents and multi-agent systems in C#, Python or Java. It connects to models from providers such as OpenAI, Azure OpenAI and Hugging Face, and extends agents with plugins built from native code, prompt templates, OpenAPI specs or the Model Context Protocol. Its README names Microsoft Agent Framework as its successor.
best_for: AI agents, Multi-agent systems, Adding AI models to existing codebases
key_features:
- Plugins from native code, prompt templates, OpenAPI specs or MCP
- Agents with tools, memory and planning
- Multi-agent orchestration
- Model connectors for OpenAI, Azure OpenAI, Hugging Face and NVIDIA
- Vector store connectors such as Azure AI Search, Elasticsearch and Chroma
- Local models through Ollama, LM Studio or ONNX
- Process Framework for business workflows
- SDKs for C#, Python and Java
use_cases:
- Chatbots and assistants
- Multi-agent workflows
- Business process automation
pros:
- Model-agnostic connectors
- Same concepts across C#, Python and Java SDKs
- Committed to non-breaking changes in its released APIs
- Telemetry, hooks and filters
cons:
- Succeeded by Microsoft Agent Framework according to its README
language: C#
languages_supported:
- C#
- Python
- Java
maintained_by: Microsoft
license_spdx: MIT
github_url: https://github.com/microsoft/semantic-kernel
docs_url: https://learn.microsoft.com/en-us/semantic-kernel/
website_url: https://learn.microsoft.com/en-us/semantic-kernel/
maturity: stable
backing:
  type: corporate
  orgs:
  - Microsoft
alternatives:
- framework/langchain
- framework/llamaindex
registry_signals:
  github_stars: 28790
  downloads_monthly: 350705
  latest_version: 1.47.0
  latest_release_date: '2026-11-05'
  observed_at: '2026-11-20'
  source: https://github.com/microsoft/semantic-kernel
aliases:
- microsoft/semantic-kernel
tags:
- llm
- enterprise
- microsoft
- dotnet
- azure
updated: '2026-11-21'
sources:
- url: https://github.com/microsoft/semantic-kernel
  title: GitHub repository
- url: https://learn.microsoft.com/en-us/semantic-kernel/
  title: Documentation
- url: https://learn.microsoft.com/en-us/semantic-kernel/overview/
  title: Introduction to Semantic Kernel
- url: https://pypi.org/project/semantic-kernel/
  title: semantic-kernel — PyPI
---

## Overview

Semantic Kernel is a model-agnostic, open-source SDK from Microsoft for building, orchestrating and deploying AI agents and multi-agent systems in C#, Python or Java. It connects to models from providers such as OpenAI, Azure OpenAI and Hugging Face, and extends agents with plugins built from native code, prompt templates, OpenAPI specs or the Model Context Protocol. Its README names Microsoft Agent Framework as its successor.
