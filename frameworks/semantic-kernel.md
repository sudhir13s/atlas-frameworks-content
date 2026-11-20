---
id: framework/semantic-kernel
type: framework
slug: semantic-kernel
schema_version: 1.1
title: Semantic Kernel
kind: framework
category: framework-category/llm-frameworks
subcategory: orchestration-framework
tagline: Microsoft's SDK for integrating LLMs into applications
description: Microsoft's open-source SDK for building AI-powered applications. Designed for enterprise integration with strong Azure OpenAI support. Provides plugins, planners, and memory abstractions. Supports C#, Python, and Java.
best_for: Enterprise .NET teams building on Azure/Microsoft stack
not_ideal_for: Python-first teams, vendor-agnostic requirements
key_features:
- Plugin architecture for extensibility
- Planner for multi-step reasoning
- Memory and vector store abstractions
- Azure OpenAI native integration
- Multi-language support (C#, Python, Java)
- Enterprise-ready patterns
use_cases:
- Enterprise AI applications on Azure
- .NET ecosystem AI integration
- Microsoft 365 Copilot plugins
- Enterprise automation with LLMs
pros:
- Best choice for .NET/C# teams
- Strong Azure/Microsoft ecosystem integration
- Enterprise-ready patterns out of the box
- Good documentation
cons:
- Python SDK less mature than C#
- Smaller community than LangChain
- Tightly coupled to Microsoft ecosystem
language: C#
languages_supported:
- C#
- Python
- Java
maintained_by: Microsoft
first_release: '2023-03-01'
license_spdx: MIT
github_url: https://github.com/microsoft/semantic-kernel
docs_url: https://learn.microsoft.com/en-us/semantic-kernel/
website_url: https://learn.microsoft.com/en-us/semantic-kernel/
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
updated: '2026-11-20'
sources:
- url: https://github.com/microsoft/semantic-kernel
  title: GitHub repository
- url: https://learn.microsoft.com/en-us/semantic-kernel/
  title: Documentation
---

## Overview

Microsoft's open-source SDK for building AI-powered applications. Designed for enterprise integration with strong Azure OpenAI support. Provides plugins, planners, and memory abstractions. Supports C#, Python, and Java.
