---
id: use-case/make-llm-app-safe-and-accurate
type: use-case
slug: make-llm-app-safe-and-accurate
schema_version: 2.0
title: Make an LLM App Safe and Accurate
label: Make an LLM app safe and accurate
order: 9
goal: Wrap a large language model (LLM) application in checks before, at and after the model, and in tests before release and in production, so its answers are correct and its behaviour stays within the limits you set.
stages:
- id: input
  name: Before the model
  note: Runs on every request, before any text reaches the model.
- id: model
  name: At the model
  note: Runs while the model generates each answer.
- id: output
  name: After the model
  note: Runs on every answer, before it is shown to the user or acted on.
- id: quality
  name: Quality and operations
  note: Runs before each release and continuously in production.
blocks:
- id: injection-detection
  stage: input
  name: Prompt-injection and jailbreak detection
  purpose: Classifies user messages and untrusted text, such as retrieved documents, web pages and tool results, for prompt injection and jailbreak attempts before they reach the model.
  options:
  - record: model/llama-prompt-guard-2-86m
    choice: default
    when: A small classifier that detects both prompt injection and jailbreak attempts, built on a multilingual base model and trained to detect English and non-English attacks.
  - record: model/llama-prompt-guard-2-22m
    choice: alternative
    when: Pick it when latency and compute cost matter most; Meta describes it as the smaller, faster model of the same series, based on DeBERTa-xsmall.
  - record: framework/nemo-guardrails
    choice: alternative
    when: Pick it to run jailbreak detection with configured heuristics or classifiers as one rail in a policy that also covers topics, personal data and tool calls.
  how_to_choose:
  - Classify every untrusted source, not only the user's message; indirect injection arrives through websites and files the application reads.
  - A classifier lowers risk but does not remove it; OWASP states that it is unclear whether fool-proof prevention of prompt injection exists.
  browse:
    label: All safety and guard models
    record: task/safety-and-guard-models
- id: input-policy
  stage: input
  name: Topic and personal-data rules
  purpose: Keeps requests within the topics the application serves and detects or masks personal data before it is sent to the model.
  options:
  - record: framework/nemo-guardrails
    choice: default
    when: Apache-2.0 library whose guardrail catalog includes topic control, detection or masking of sensitive data in inputs, outputs and retrieved content, and deterministic regular-expression rules, all declared in configuration files.
  - record: framework/guardrails-ai
    choice: alternative
    when: Pick it to combine validators from Guardrails Hub, installed as Python packages, into input and output guards around the model call; it is Apache-2.0.
  how_to_choose:
  - Use local rules for patterns that can be matched exactly and model-backed checks for meaning; NeMo Guardrails combines both in one policy.
  - Mask personal data in retrieved documents as well as in user messages.
  browse:
    label: All guardrail and safety tools
    record: framework-category/guardrails
- id: structured-output
  stage: model
  name: Structured output
  purpose: Makes the model return its answer in a declared schema, so code can parse and validate it before anything acts on it.
  options:
  - record: framework/outlines
    choice: default
    when: Apache-2.0 library that enforces a JSON schema, regular expression or grammar during generation, so the structure of the output is guaranteed rather than repaired afterwards.
  - record: framework/instructor
    choice: alternative
    when: Pick it to validate responses against Pydantic models and retry the request when parsing or validation fails; it is MIT-licensed.
  how_to_choose:
  - Validate the parsed output with deterministic code before acting on it, as the OWASP prompt-injection guidance recommends.
  - Include fields for source citations in the schema so later checks can compare claims with sources.
- id: grounding
  stage: model
  name: Grounding in retrieved sources
  purpose: Retrieves passages from your own documents and gives them to the model with the instruction to answer only from them and cite them.
  options:
  - record: framework/llamaindex
    choice: default
    when: MIT-licensed retrieval-augmented generation (RAG) toolkit whose CitationQueryEngine returns answers with numbered citations to the retrieved source passages.
  how_to_choose:
  - Keep the source of each passage with the answer so a reader or a check can verify every claim.
  - The Build a RAG app guide covers parsing, embedding, retrieval and reranking in detail.
  browse:
    label: All RAG tools
    record: framework-category/rag
- id: output-moderation
  stage: output
  name: Output moderation
  purpose: Classifies the model's reply for unsafe content before it is shown or acted on.
  options:
  - record: model/llama-guard-4-12b
    choice: default
    when: Classifies both prompts and responses, including text with multiple images, against the MLCommons hazard taxonomy and lists the violated categories; released under the Llama 4 Community License.
  - record: framework/nemo-guardrails
    choice: alternative
    when: Pick it to run content-safety output rails with a safety model of your choice, configured in the same policy as the input rails.
  how_to_choose:
  - Count the guard model's latency in the response budget, since it runs on every answer.
  - Decide in advance whether a blocked reply becomes a refusal, a regenerated answer or an error.
  browse:
    label: All safety and guard models
    record: task/safety-and-guard-models
- id: groundedness-check
  stage: output
  name: Groundedness and hallucination checks
  purpose: Checks that the claims in an answer are supported by the retrieved sources before or after it reaches the user.
  options:
  - record: framework/nemo-guardrails
    choice: default
    when: Its fact-checking and hallucination rails check answers against evidence or compare several model responses for consistency while the request is being served.
  - record: framework/ragas
    choice: alternative
    when: Pick it for offline analysis; its Faithfulness metric splits an answer into claims and scores the share supported by the retrieved context, with an option to use the HHEM-2.1-Open classifier instead of a model judge.
  - record: framework/deepeval
    choice: alternative
    when: Pick it to run faithfulness and hallucination metrics as pytest-style test cases.
  how_to_choose:
  - The OWASP guidance lists checking an answer's groundedness and relevance to the retrieved context as an output filter.
  - Decide whether an unsupported answer is blocked, regenerated or shown with a warning.
- id: evaluation
  stage: quality
  name: Evaluation sets and metrics
  purpose: Scores answers against a fixed labelled set so every change to prompts, models, retrieval or guardrails is measured before release.
  options:
  - record: framework/deepeval
    choice: default
    when: Apache-2.0 framework that runs metrics such as answer relevancy, faithfulness and hallucination as unit tests, so a regression fails a continuous integration (CI) run.
  - record: framework/ragas
    choice: alternative
    when: Pick it for RAG-specific metrics such as context precision, context recall and faithfulness.
  - record: framework/promptfoo
    choice: alternative
    when: Pick it for MIT-licensed declarative test configs that run locally and in CI and compare several models side by side on the same tests.
  how_to_choose:
  - Keep the labelled set fixed and rerun it on every change so scores stay comparable.
  - Add examples from production traces to the set so the tests reflect real traffic.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
- id: red-teaming
  stage: quality
  name: Red-teaming
  purpose: Attacks the application before release to find inputs that break its rules, leak data or get past its guardrails.
  options:
  - record: framework/garak
    choice: default
    when: Apache-2.0 command-line scanner that probes for prompt injection, jailbreaks, data leakage, hallucination and toxic output, and connects to Hugging Face models, the OpenAI API, AWS Bedrock and REST endpoints.
  - record: framework/pyrit
    choice: alternative
    when: Pick it for adaptive multi-turn attacks and human-led testing; it is MIT-licensed, with a command-line scanner, a browser interface and a Python framework that reach applications over HTTP, WebSockets or browser automation.
  - record: framework/promptfoo
    choice: alternative
    when: Pick it to run red teaming and vulnerability scanning from the same tool as your evaluation tests, in CI.
  how_to_choose:
  - Treat the model as an untrusted user and test the trust boundaries and access controls around it, as OWASP recommends.
  - Rerun the scan after every change to prompts, models or guardrails.
  browse:
    label: All guardrail and safety tools
    record: framework-category/guardrails
- id: safety-benchmarks
  stage: quality
  name: Safety benchmarks
  purpose: Compares candidate models and defences on public attack sets before you test them on your own application.
  options:
  - record: benchmark/harmbench
    choice: default
    when: A standardized, open-source evaluation framework for automated red teaming that compares attack methods against models and defences on the same harmful behaviours.
  - record: benchmark/jailbreakbench
    choice: alternative
    when: Use it to measure jailbreak robustness and, through its benign behaviours, how often a model refuses requests it should answer.
  - record: benchmark/strongreject
    choice: alternative
    when: Use it to score how useful a response is to a forbidden request; its authors found that earlier evaluators overstate jailbreak success.
  - record: benchmark/agentdojo
    choice: alternative
    when: Use it to compare how well models and defences resist prompt injection in tool-using agents.
  how_to_choose:
  - Check how each benchmark judges a response; several rely on a classifier or a model as the judge.
  - Public benchmarks do not cover your own tools and data, so red-team the application as well.
- id: tracing
  stage: quality
  name: Tracing and feedback
  purpose: Records each request's checks, retrieved passages, prompt, answer and user feedback so failures can be traced to their step and turned into regression tests.
  options:
  - record: framework/langfuse
    choice: default
    when: Open-source platform built on OpenTelemetry that traces model calls, retrieval and agent actions, collects user feedback and model-judged scores, keeps datasets for pre-deployment tests, and can be self-hosted.
  - record: framework/arize-phoenix
    choice: alternative
    when: Pick it for self-hosted OpenTelemetry-based tracing with response and retrieval evals; it is licensed under the Elastic License 2.0.
  how_to_choose:
  - Log every guardrail decision with its trace so a blocked or passed request can be explained.
  - Prefer a tool that accepts OpenTelemetry so you can switch backends later.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
learn_next:
- title: OWASP LLM01:2025 Prompt Injection
  url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  kind: docs
- title: 'NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications with Programmable Rails'
  url: https://arxiv.org/abs/2310.10501
  kind: paper
- title: 'Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations'
  url: https://arxiv.org/abs/2312.06674
  kind: paper
- title: 'garak: A Framework for Security Probing Large Language Models'
  url: https://arxiv.org/abs/2406.11036
  kind: paper
related_use_cases:
- use-case/build-a-rag-app
- use-case/build-an-agent
- use-case/serve-in-production
tags:
- guardrails
- safety
- prompt-injection
- hallucination
- evaluation
- red-teaming
- llm
updated: '2026-11-21'
sources:
- url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  title: OWASP LLM01:2025 Prompt Injection
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-86M
  title: meta-llama/Llama-Prompt-Guard-2-86M model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-22M
  title: meta-llama/Llama-Prompt-Guard-2-22M model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B model card
  trust: 0.9
- url: https://github.com/NVIDIA-NeMo/Guardrails
  title: NeMo Guardrails repository
  trust: 0.9
- url: https://github.com/guardrails-ai/guardrails
  title: Guardrails AI repository
  trust: 0.9
- url: https://github.com/dottxt-ai/outlines
  title: Outlines repository
  trust: 0.9
- url: https://python.useinstructor.com/concepts/retrying/
  title: Instructor documentation, retrying
  trust: 0.9
- url: https://developers.llamaindex.ai/python/examples/query_engine/citation_query_engine/
  title: LlamaIndex CitationQueryEngine example
  trust: 0.9
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/faithfulness/
  title: Ragas Faithfulness metric
  trust: 0.9
- url: https://github.com/confident-ai/deepeval
  title: DeepEval repository
  trust: 0.9
- url: https://github.com/promptfoo/promptfoo
  title: promptfoo repository
  trust: 0.9
- url: https://github.com/NVIDIA/garak
  title: garak repository
  trust: 0.9
- url: https://github.com/microsoft/PyRIT
  title: PyRIT repository
  trust: 0.9
- url: https://arxiv.org/abs/2402.04249
  title: 'HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal'
  trust: 0.95
- url: https://arxiv.org/abs/2404.01318
  title: 'JailbreakBench: An Open Robustness Benchmark for Jailbreaking Large Language Models'
  trust: 0.95
- url: https://arxiv.org/abs/2402.10260
  title: A StrongREJECT for Empty Jailbreaks
  trust: 0.95
- url: https://github.com/ethz-spylab/agentdojo
  title: AgentDojo repository
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://github.com/Arize-ai/phoenix
  title: Arize Phoenix repository
  trust: 0.9
---

## Overview

OWASP notes that it is unclear whether prompt injection can be fully prevented, so a team layers checks around the model. **Before the model**, classifiers and rules screen requests and untrusted text for injection, off-topic requests and personal data.

**At the model**, structured output makes answers parse and grounding ties them to your sources. **After the model**, a guard model moderates the reply and a groundedness check tests its claims. **Before release and in production**, evaluation sets, red-teaming, safety benchmarks and tracing catch regressions.
