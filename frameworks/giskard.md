---
id: framework/giskard
type: framework
slug: giskard
schema_version: 1.1
title: Giskard
kind: library
category: framework-category/evaluation
subcategory: ml-testing
tagline: Testing framework for ML models — detect bias, performance issues, and vulnerabilities
description: Open-source testing framework for ML and LLM models. Automatically generates test suites to detect bias, data leakage, performance regressions, and adversarial vulnerabilities. Supports both traditional ML and LLM evaluation.
best_for: ML model testing with focus on bias, safety, and compliance
not_ideal_for: Simple LLM prompt testing (use Promptfoo)
key_features:
- Automatic test generation
- Bias detection
- LLM hallucination testing
- Data leakage detection
- Model debugging
- Regulatory compliance checks
use_cases:
- ML model quality assurance
- Bias and fairness testing
- LLM safety testing
- Regulatory compliance for AI
pros:
- Automatic test generation saves time
- Covers bias and fairness
- Works with traditional ML and LLMs
cons:
- Smaller community
- Auto-generated tests need manual curation
- Some features require paid plan
language: Python
languages_supported:
- Python
maintained_by: Giskard AI
first_release: '2022-01-01'
license_spdx: Apache-2.0
github_url: https://github.com/Giskard-AI/giskard
docs_url: https://docs.giskard.ai/
website_url: https://giskard.ai/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: small
maturity: stable
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Giskard AI
  funding_or_parent: Seed €3M led by Elaia Partners (2023)
alternatives:
- framework/deepeval
- framework/ragas
ecosystem_connections:
- framework/pytorch
- framework/hugging-face-transformers
registry_signals:
  github_stars: 5960
  downloads_monthly: 11486
  latest_version: 3.0.1
  latest_release_date: '2026-10-02'
  observed_at: '2026-11-20'
  source: https://github.com/Giskard-AI/giskard
aliases:
- Giskard-AI/giskard
tags:
- evaluation
- testing
- bias
- safety
- compliance
updated: '2026-11-20'
sources:
- url: https://github.com/Giskard-AI/giskard
  title: GitHub repository
- url: https://docs.giskard.ai/
  title: Documentation
---

## Overview

Open-source testing framework for ML and LLM models. Automatically generates test suites to detect bias, data leakage, performance regressions, and adversarial vulnerabilities. Supports both traditional ML and LLM evaluation.
