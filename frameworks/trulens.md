---
id: framework/trulens
type: framework
slug: trulens
schema_version: 3.0
title: TruLens
status: curated
kind: library
category: framework-category/evaluation
subcategory: llm-app-evaluation
tagline: Evaluation and Tracking for LLM Experiments and AI Agents.
description: TruLens is a Python library for tracing and evaluating LLM applications and agents. It instruments an app with a decorator, records each step as an OpenTelemetry span with inputs, outputs, latency, tokens and cost, and scores the steps with LLM judges such as the RAG triad of context relevance, groundedness and answer relevance. It sits beside a RAG or agent app, inline as traces arrive or in batch over a dataset, and compares app versions on a leaderboard.
best_for: Evaluating RAG apps with the RAG triad, Tracing and evaluating agents, Comparing app versions on quality, latency and cost
key_features:
- OpenTelemetry-based tracing exportable to any OTLP backend
- RAG triad metrics for context relevance, groundedness and answer relevance
- Seven agentic evaluators, including plan adherence and tool selection
- Inline and batch evaluation
- MCP tool call instrumentation
- Selector API for evaluating any span attribute
- Leaderboard of scores, latency and cost per app version
- Providers for OpenAI, LiteLLM, Gemini, Bedrock, Snowflake Cortex and Hugging Face
use_cases:
- RAG evaluation
- Agent evaluation
- Hallucination detection in RAG answers
- Comparing app versions before release
pros:
- Traces are portable to Jaeger, Grafana Tempo, Datadog, New Relic and other OTLP backends
- Integrations with LangChain, LangGraph and LlamaIndex apps
- Judges graded against human annotations
language: Python
languages_supported:
- Python
maintained_by: Snowflake
license_spdx: MIT
github_url: https://github.com/truera/trulens
docs_url: https://www.trulens.org/getting_started/
website_url: https://www.trulens.org/
maturity: experimental
backing:
  type: corporate
  orgs:
  - Snowflake
alternatives:
- framework/ragas
- framework/deepeval
ecosystem_connections:
- framework/langchain
- framework/langgraph
- framework/llamaindex
- framework/litellm
registry_signals:
  github_stars: 3668
  downloads_monthly: 23969
  latest_version: 2.16.0
  latest_release_date: '2026-10-19'
  observed_at: '2026-11-24'
  source: https://github.com/truera/trulens
aliases:
- truera/trulens
- trulens_eval
tags:
- llm-evaluation
- agent-evaluation
- evals
- ai-observability
- llmops
- ai-agents
updated: '2026-11-24'
sources:
- url: https://github.com/truera/trulens
  title: GitHub repository
- url: https://raw.githubusercontent.com/truera/trulens/HEAD/README.md
  title: README
- url: https://www.trulens.org/getting_started/core_concepts/rag_triad/
  title: The RAG Triad
- url: https://pypi.org/project/trulens/
  title: trulens — PyPI
- url: https://pypistats.org/api/packages/trulens/recent
  title: trulens — PyPI download statistics
---


