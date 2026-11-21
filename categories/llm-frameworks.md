---
id: framework-category/llm-frameworks
type: framework-category
slug: llm-frameworks
schema_version: 2.1
title: LLM Frameworks
label: LLM Frameworks
layer: build
order: 1
short_description: Orchestration layers that turn a raw LLM into an application — prompts, chains, retrieval, and tools.
why_it_matters: They remove the boilerplate between a model call and a working app, and standardize retrieval and tool use.
defacto:
  framework_id: framework/langchain
  reason: The most-adopted orchestration framework; broad integrations and the LangGraph runtime for stateful apps.
rising:
- framework_id: framework/llamaindex
  reason: Data-first framework that leads on ingestion, indexing, and retrieval-centric applications.
- framework_id: framework/dspy
  reason: Compiles and optimizes prompts programmatically instead of hand-tuning them.
alternatives:
- framework_id: framework/haystack
  reason: Production-oriented pipelines from deepset, strong for search and RAG.
- framework_id: framework/semantic-kernel
  reason: Microsoft's SDK, popular in .NET/enterprise stacks.
- framework_id: framework/litellm
  reason: Not an orchestrator but the common gateway underneath — one API across 100+ model providers.
key_concepts:
- prompt templating
- chains and graphs
- tool calling
- retrieval
- structured output
canonical_reading:
- title: LangChain — Introduction
  url: https://python.langchain.com/docs/introduction/
- title: LlamaIndex — High-level concepts
  url: https://docs.llamaindex.ai/en/stable/getting_started/concepts/
- title: DSPy — documentation
  url: https://dspy.ai/
did_you_know:
- LangChain started as a weekend project by Harrison Chase in October 2022, weeks before ChatGPT launched.
- DSPy treats prompts like a program a compiler optimizes, rather than strings you tune by hand.
- Most production LLM apps use an orchestrator plus a separate model gateway (like LiteLLM) underneath.
tags:
- llm
- orchestration
- frameworks
updated: '2026-11-19'
sources:
- url: https://python.langchain.com/docs/introduction/
  title: LangChain documentation
  trust: 0.9
- url: https://docs.llamaindex.ai/en/stable/
  title: LlamaIndex documentation
  trust: 0.9
- url: https://dspy.ai/
  title: DSPy documentation
  trust: 0.85
---

## Overview

LLM frameworks are the application layer over a language model. They wire together prompt templates,
retrieval, memory, tool calls, and control flow so you write app logic instead of glue code, and they
standardize the patterns (RAG, agents, structured output) that would otherwise be reinvented per project.

## Landscape

LangChain is the default by adoption and integration breadth, with LangGraph handling stateful,
multi-step apps. LlamaIndex leads when the problem is data — ingestion, indexing, and retrieval. DSPy
is a different philosophy: optimize prompts programmatically. Haystack and Semantic Kernel serve
production and enterprise/.NET niches. Underneath most of them sits a gateway like LiteLLM.

## Notes

These frameworks move fast and their APIs churn — pin versions and expect breaking changes. The right
choice depends on the job: retrieval-heavy → LlamaIndex, agentic/stateful → LangGraph, prompt
optimization → DSPy.
