---
id: framework-category/agents
type: framework-category
slug: agents
schema_version: 1.1
title: Agent Frameworks
label: Agents
order: 5
short_description: Frameworks for LLMs that plan and act — calling tools in a loop, alone or as collaborating roles.
why_it_matters: Agents extend a model from answering to *doing*; the framework decides how reliable and debuggable that loop is.
defacto:
  framework_id: framework/langchain
  reason: LangGraph gives the reason-act loop a durable, inspectable graph, with LangSmith tracing built into the stack.
rising:
- framework_id: framework/crewai
  reason: Role-based multi-agent orchestration; hit 20k+ GitHub stars within a year of release.
- framework_id: framework/autogen
  reason: Microsoft Research's multi-agent conversation framework, strong for agent-to-agent collaboration.
alternatives:
- framework_id: framework/semantic-kernel
  reason: Microsoft's SDK with planners and plugins, favoured in enterprise/.NET.
- framework_id: framework/google-adk
  reason: Google's Agent Development Kit, aligned with Gemini and Vertex.
- framework_id: framework/claude-agent-sdk
  reason: Anthropic's SDK for building agents around Claude with tool use and MCP.
key_concepts:
- ReAct loop
- tool calling
- planning
- multi-agent orchestration
- tracing and evals
canonical_reading:
- title: 'ReAct: Synergizing Reasoning and Acting in Language Models'
  url: https://arxiv.org/abs/2210.03629
- title: LangGraph — documentation
  url: https://langchain-ai.github.io/langgraph/
- title: CrewAI — core concepts
  url: https://docs.crewai.com/concepts/agents
did_you_know:
- LangChain was started as a weekend project by Harrison Chase in October 2022.
- The ReAct pattern (Reason + Act) is the template most agent frameworks still follow.
- CrewAI hit 20k+ GitHub stars within a year of its first release.
tags:
- agents
- tools
- orchestration
updated: '2026-11-19'
sources:
- url: https://langchain-ai.github.io/langgraph/
  title: LangGraph documentation
  trust: 0.9
- url: https://arxiv.org/abs/2210.03629
  title: 'ReAct: Synergizing Reasoning and Acting in Language Models'
  trust: 0.95
- url: https://docs.crewai.com/
  title: CrewAI documentation
  trust: 0.85
---

## Overview

An agent framework runs an LLM in a loop with tools: reason, act, observe, repeat. Single-agent
designs follow the ReAct pattern; multi-agent designs assign roles that collaborate. The framework's
real job is making that loop reliable, bounded, and debuggable.

## Landscape

LangGraph (in the LangChain stack) is the default for durable, inspectable single-agent loops, with
LangSmith tracing alongside. CrewAI and AutoGen lead the multi-agent space — role-based crews and
agent-to-agent conversation respectively. Semantic Kernel, Google's ADK, and Anthropic's Claude Agent
SDK cover vendor-aligned and enterprise stacks.

## Notes

Two rules keep agents from misbehaving: bound the loop (max steps) and add tools one at a time.
Tracing is non-negotiable — agents fail mid-loop and are undebuggable without it. Reach for multi-agent
designs only after a single agent has clearly hit its ceiling.
