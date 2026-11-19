---
id: framework/claude-agent-sdk
type: framework
slug: claude-agent-sdk
schema_version: 1.1
title: Claude Agent SDK
kind: library
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Anthropic's SDK for building production agents on Claude with tool use, sub-agents, memory, and computer use.
description: 'Agent-building SDK from Anthropic, formerly the Claude Code SDK. Provides the primitives used internally for Claude Code: tool use, parallel tool calls, sub-agents, memory management, and the computer-use action set. Python is the primary implementation; a TypeScript variant is also available at anthropics/claude-agent-sdk-typescript.'
best_for: Teams building agents on Claude who want Anthropic's own primitives and computer-use support
not_ideal_for: Multi-provider routing (use LiteLLM/LangChain), teams not committed to Claude
key_features:
- Tool use with parallel tool calls
- Sub-agent orchestration
- Memory management primitives
- Computer-use action set
- Custom tools, hooks, and MCP server support
- Powers Claude Code internally
use_cases:
- Claude-native production agents
- Coding agents (the Claude Code pattern)
- Computer-use automation
- MCP-integrated agent systems
pros:
- Production-tested (powers Claude Code)
- First-party from Anthropic
- Native computer-use and MCP support
- Python and TypeScript available
cons:
- Claude-specific — not a universal LLM abstraction
- Smaller ecosystem than LangChain
- Pre-1.0 versioning (0.1.x)
language: Python
languages_supported:
- Python
- TypeScript
maintained_by: Anthropic
first_release: '2025-06-11'
license_spdx: MIT
github_url: https://github.com/anthropics/claude-agent-sdk-python
docs_url: https://docs.claude.com/en/docs/claude-code/sdk
website_url: https://docs.claude.com/en/docs/claude-code/sdk
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: stable
signal_strength: high
backing:
  type: corporate
  orgs:
  - Anthropic
  funding_or_parent: Anthropic — production-tested as the backbone of Claude Code
alternatives:
- framework/langchain
- framework/crewai
- framework/autogen
registry_signals:
  github_stars: 6300
  latest_version: 0.1.59
  latest_release_date: '2026-04-13'
  observed_at: '2026-06-15'
  source: https://github.com/anthropics/claude-agent-sdk-python
aliases:
- anthropics/claude-agent-sdk-python
tags:
- llm
- agents
- anthropic
- claude
- computer-use
- mcp
updated: '2026-11-19'
sources:
- url: https://github.com/anthropics/claude-agent-sdk-python
  title: GitHub repository
- url: https://docs.claude.com/en/docs/claude-code/sdk
  title: Documentation
---

## Overview

Agent-building SDK from Anthropic, formerly the Claude Code SDK. Provides the primitives used internally for Claude Code: tool use, parallel tool calls, sub-agents, memory management, and the computer-use action set. Python is the primary implementation; a TypeScript variant is also available at anthropics/claude-agent-sdk-typescript.
