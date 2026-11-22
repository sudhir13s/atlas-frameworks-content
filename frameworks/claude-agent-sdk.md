---
id: framework/claude-agent-sdk
type: framework
slug: claude-agent-sdk
schema_version: 1.1
title: Claude Agent SDK
kind: library
category: framework-category/llm-frameworks
subcategory: agent-framework
tagline: Build production AI agents with Claude Code as a library.
description: The Claude Agent SDK gives you the same tools, agent loop and context management that power Claude Code, programmable in Python and TypeScript. It is a library that runs the Claude Code binary inside your own application, with built-in tools, permissions, sessions and hooks. It replaces the earlier Claude Code SDK packages.
best_for: Embedding Claude Code's agent in your own Python or TypeScript application
not_ideal_for: Languages other than Python or TypeScript (the docs suggest running the CLI as a subprocess), Calling the Claude API directly (the docs point to the Client SDK)
key_features:
- Built-in tools to read, write and edit files, run commands and search the web
- Hooks at key points in the agent lifecycle
- Subagents for focused subtasks
- MCP servers, including in-process SDK MCP servers for custom tools
- Permissions that control which tools run automatically
- Sessions that can be resumed or forked
- Skills, commands and memory loaded from .claude directories
- Plugins loaded by local path
- Claude Code CLI bundled with the Python package
use_cases:
- Agents that find and fix bugs in existing code
- Agents with custom tools exposed through MCP
- Embedding the Claude Code agent loop in your own application
pros:
- Same tools and agent loop as Claude Code
- First-party SDK from Anthropic
- Custom tools run in-process as Python functions
- Python and TypeScript SDKs
cons:
- Use is governed by Anthropic's Commercial Terms of Service
- Third-party products may not offer claude.ai login or rate limits unless previously approved
- Marked Alpha in its PyPI development status
language: Python
languages_supported:
- Python
- TypeScript
maintained_by: Anthropic
github_url: https://github.com/anthropics/claude-agent-sdk-python
docs_url: https://code.claude.com/docs/en/agent-sdk/overview
website_url: https://code.claude.com/docs/en/agent-sdk/overview
maturity: experimental
backing:
  type: corporate
  orgs:
  - Anthropic
alternatives:
- framework/langchain
- framework/crewai
- framework/autogen
registry_signals:
  github_stars: 8599
  downloads_monthly: 38330618
  latest_version: 0.2.186
  latest_release_date: '2026-11-19'
  observed_at: '2026-11-20'
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
updated: '2026-11-21'
sources:
- url: https://github.com/anthropics/claude-agent-sdk-python
  title: GitHub repository
- url: https://code.claude.com/docs/en/agent-sdk/overview
  title: Agent SDK overview - Claude Code Docs
- url: https://pypi.org/project/claude-agent-sdk/
  title: claude-agent-sdk — PyPI
license_note: Use is governed by Anthropic's Commercial Terms of Service, except components covered by their own LICENSE file (the repository LICENSE file is MIT)
---

## Overview

The Claude Agent SDK gives you the same tools, agent loop and context management that power Claude Code, programmable in Python and TypeScript. It is a library that runs the Claude Code binary inside your own application, with built-in tools, permissions, sessions and hooks. It replaces the earlier Claude Code SDK packages.
