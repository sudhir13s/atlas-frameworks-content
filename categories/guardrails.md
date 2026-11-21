---
id: framework-category/guardrails
type: framework-category
slug: guardrails
schema_version: 2.1
title: Guardrails & Safety
label: Guardrails & Safety
layer: operate
short_description: Tools that check the inputs, outputs and tool calls of large language model (LLM) applications against safety and security policies, and that probe those applications for weaknesses before release.
why_it_matters: An LLM application accepts text from users and from documents it does not control, so prompt injection, jailbreaks and unsafe output have to be checked for outside the model itself.
key_concepts:
- input and output rails
- prompt injection
- jailbreak detection
- content safety classification
- red teaming
- vulnerability scanning
canonical_reading:
- title: OWASP LLM01:2025 Prompt Injection
  url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
- title: 'NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications with Programmable Rails'
  url: https://arxiv.org/abs/2310.10501
- title: 'Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations'
  url: https://arxiv.org/abs/2312.06674
- title: 'garak: A Framework for Security Probing Large Language Models'
  url: https://arxiv.org/abs/2406.11036
tags:
- guardrails
- safety
- security
- red-teaming
- prompt-injection
updated: '2026-11-21'
sources:
- url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  title: OWASP LLM01:2025 Prompt Injection
  trust: 0.9
- url: https://github.com/NVIDIA-NeMo/Guardrails
  title: NeMo Guardrails repository
  trust: 0.9
- url: https://arxiv.org/abs/2310.10501
  title: 'NeMo Guardrails: A Toolkit for Controllable and Safe LLM Applications with Programmable Rails (arXiv:2310.10501)'
  trust: 0.95
- url: https://arxiv.org/abs/2312.06674
  title: 'Llama Guard: LLM-based Input-Output Safeguard for Human-AI Conversations (arXiv:2312.06674)'
  trust: 0.95
- url: https://arxiv.org/abs/2406.11036
  title: 'garak: A Framework for Security Probing Large Language Models (arXiv:2406.11036)'
  trust: 0.95
- url: https://github.com/microsoft/PyRIT
  title: PyRIT repository
  trust: 0.9
---
