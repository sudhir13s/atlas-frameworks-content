---
id: framework/giskard
type: framework
slug: giskard
schema_version: 1.1
title: Giskard
kind: library
category: framework-category/evaluation
subcategory: ml-testing
tagline: Open-Source Evaluation & Testing library for LLM Agents.
description: Open-source Python library for testing and evaluating agentic systems, from a single LLM to a black-box agent or a multi-step pipeline. It ships as modular packages, with giskard-checks for evals that range from simple assertions to LLM-as-judge checks and giskard-scan for red teaming, vulnerability scanning and RAG quality evaluation. The automatic scan for tabular ML models exists only in the previous major version, which is no longer actively maintained.
best_for: Testing and evaluating LLM-based agents, Red teaming agentic systems, RAG quality evaluation
not_ideal_for: Automatic scanning of tabular ML models (only in the previous major version)
key_features:
- Scenario API with built-in checks and test suites
- LLM-as-judge checks such as Groundedness and Conformity
- Multi-turn agent evaluation
- Vulnerability scan for prompt injection, jailbreaks and harmful content
- Adversarial test suites generated from a plain-language agent description
- Knowledge-base quality scan for RAG systems
use_cases:
- Regression testing of LLM-based systems
- Red teaming AI agents
- Checking that RAG answers are grounded in retrieved context
- Enforcing content policies on model outputs
pros:
- Modular packages that each carry only the dependencies they need
- Wraps any sync or async callable as the system under test
cons:
- The automatic tabular ML scan exists only in the previous major version, which is no longer actively maintained
- LLM judges and scan generators need an LLM provider and API key
- Team collaboration and continuous red teaming are in the separate enterprise Giskard Hub
language: Python
languages_supported:
- Python
maintained_by: Giskard AI
license_spdx: Apache-2.0
github_url: https://github.com/Giskard-AI/giskard-oss
docs_url: https://docs.giskard.ai/
website_url: https://giskard.ai/
backing:
  type: corporate
  orgs:
  - Giskard AI
alternatives:
- framework/deepeval
- framework/ragas
registry_signals:
  github_stars: 5962
  downloads_monthly: 11486
  latest_version: 3.0.1
  latest_release_date: '2026-10-02'
  observed_at: '2026-11-20'
  source: https://github.com/Giskard-AI/giskard
aliases:
- Giskard-AI/giskard
- Giskard-AI/giskard-oss
tags:
- evaluation
- testing
- bias
- safety
- compliance
updated: '2026-11-21'
sources:
- url: https://github.com/Giskard-AI/giskard-oss
  title: GitHub repository
- url: https://docs.giskard.ai/
  title: Documentation
- url: https://docs.giskard.ai/oss
  title: Giskard Open Source documentation
- url: https://pypi.org/project/giskard/
  title: giskard — PyPI
---

## Overview

Open-source Python library for testing and evaluating agentic systems, from a single LLM to a black-box agent or a multi-step pipeline. It ships as modular packages, with giskard-checks for evals that range from simple assertions to LLM-as-judge checks and giskard-scan for red teaming, vulnerability scanning and RAG quality evaluation. The automatic scan for tabular ML models exists only in the previous major version, which is no longer actively maintained.
