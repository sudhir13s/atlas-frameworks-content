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
why_it_matters: They provide the prompt, retrieval and tool-calling code that sits between a model call and a working application.
defacto:
  framework_id: framework/langchain
  reason: Framework for building agents and LLM applications by chaining interoperable components and third-party integrations, with LangGraph for controllable agent workflows.
rising:
- framework_id: framework/llamaindex
  reason: Open-source framework for agentic and RAG applications over your data, with data connectors, indices, retrievers and query engines.
- framework_id: framework/dspy
  reason: Programs language models in Python code instead of prompts, with algorithms that optimize the prompts and weights.
alternatives:
- framework_id: framework/haystack
  reason: Open-source orchestration framework for production LLM applications, built from modular pipelines with explicit retrieval, routing, memory and generation.
- framework_id: framework/semantic-kernel
  reason: Microsoft's model-agnostic SDK for building agents and multi-agent systems; its README names Microsoft Agent Framework as the successor.
- framework_id: framework/litellm
  reason: Gateway that calls 100+ LLM providers through one OpenAI-format interface, as a Python SDK or a proxy server.
key_concepts:
- prompt templating
- chains and graphs
- tool calling
- retrieval
- structured output
canonical_reading:
- title: LangChain — overview
  url: https://docs.langchain.com/oss/python/langchain/overview
- title: LlamaIndex — high-level concepts
  url: https://developers.llamaindex.ai/python/framework/getting_started/concepts/
- title: DSPy — documentation
  url: https://dspy.ai/
tags:
- llm
- orchestration
- frameworks
updated: '2026-11-21'
sources:
- url: https://github.com/langchain-ai/langchain
  title: LangChain repository
  trust: 0.9
- url: https://github.com/run-llama/llama_index
  title: LlamaIndex repository
  trust: 0.9
- url: https://github.com/stanfordnlp/dspy
  title: DSPy repository
  trust: 0.9
- url: https://github.com/deepset-ai/haystack
  title: Haystack repository
  trust: 0.9
- url: https://github.com/microsoft/semantic-kernel
  title: Semantic Kernel repository
  trust: 0.9
- url: https://github.com/BerriAI/litellm
  title: LiteLLM repository
  trust: 0.9
---
