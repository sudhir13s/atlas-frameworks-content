---
id: framework-category/agents
type: framework-category
slug: agents
schema_version: 2.1
title: Agent Frameworks
label: Agents
layer: build
order: 5
short_description: Frameworks for LLM applications that plan and act by calling tools in a loop, as one agent or as several agents with separate roles.
why_it_matters: An agent runs model calls, tool calls and their results in a loop, and the framework manages that loop's state and control flow.
defacto:
  framework_id: framework/langchain
  reason: Its README describes LangChain as a framework for building agents and LLM applications; LangGraph, from the same team, is the orchestration runtime with durable execution, streaming, human-in-the-loop and persistence.
rising:
- framework_id: framework/crewai
  reason: 'Open-source Python framework for multi-agent workflows: role-based agents that collaborate in Crews, and event-driven control in Flows.'
alternatives:
- framework_id: framework/semantic-kernel
  reason: Microsoft's model-agnostic SDK for building agents and multi-agent systems; its README names Microsoft Agent Framework as the successor.
- framework_id: framework/google-adk
  reason: Google's open-source, code-first framework for building, evaluating and deploying agents; optimized for Gemini but model-agnostic.
- framework_id: framework/claude-agent-sdk
  reason: Anthropic's Python SDK for building agents on the Claude Code toolset, with custom tools as in-process MCP servers.
key_concepts:
- ReAct loop
- tool calling
- planning
- multi-agent orchestration
- tracing and evals
canonical_reading:
- title: 'ReAct: Synergizing Reasoning and Acting in Language Models'
  url: https://arxiv.org/abs/2210.03629
- title: LangGraph overview
  url: https://docs.langchain.com/oss/python/langgraph/overview
- title: CrewAI — Agents
  url: https://docs.crewai.com/en/concepts/agents
tags:
- agents
- tools
- orchestration
updated: '2026-11-21'
sources:
- url: https://github.com/langchain-ai/langchain
  title: LangChain repository
  trust: 0.9
- url: https://docs.langchain.com/oss/python/langgraph/overview
  title: LangGraph overview
  trust: 0.9
- url: https://github.com/crewAIInc/crewAI
  title: CrewAI repository
  trust: 0.9
- url: https://github.com/microsoft/autogen
  title: AutoGen repository
  trust: 0.9
- url: https://github.com/microsoft/semantic-kernel
  title: Semantic Kernel repository
  trust: 0.9
- url: https://github.com/google/adk-python
  title: Agent Development Kit (ADK) repository
  trust: 0.9
- url: https://github.com/anthropics/claude-agent-sdk-python
  title: Claude Agent SDK for Python repository
  trust: 0.9
- url: https://arxiv.org/abs/2210.03629
  title: 'ReAct: Synergizing Reasoning and Acting in Language Models'
  trust: 0.9
---
