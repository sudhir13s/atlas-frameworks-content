---
id: framework-category/observability
type: framework-category
slug: observability
schema_version: 2.1
title: Observability & Tracing
label: Observability & Tracing
layer: operate
short_description: Tools that record what a large language model (LLM) application does at run time (each model call, retrieval and tool call, with its latency and cost) so a team can inspect, debug and monitor it.
why_it_matters: An LLM application is a chain of model, retrieval and tool steps, and a wrong answer cannot be traced to its cause without a recorded trace of each step.
key_concepts:
- traces and spans
- instrumentation
- OpenTelemetry (OTel)
- latency and cost tracking
- prompt versioning
- trace-linked evaluation
canonical_reading:
- title: OpenTelemetry observability primer
  url: https://opentelemetry.io/docs/concepts/observability-primer/
- title: OpenTelemetry semantic conventions for generative AI
  url: https://github.com/open-telemetry/semantic-conventions-genai
tags:
- observability
- tracing
- monitoring
- opentelemetry
updated: '2026-11-21'
sources:
- url: https://opentelemetry.io/docs/concepts/observability-primer/
  title: OpenTelemetry observability primer
  trust: 0.9
- url: https://github.com/open-telemetry/semantic-conventions-genai
  title: OpenTelemetry semantic conventions for generative AI repository
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://github.com/Arize-ai/phoenix
  title: Arize Phoenix repository
  trust: 0.9
- url: https://docs.langchain.com/langsmith/home
  title: LangSmith documentation
  trust: 0.9
---
