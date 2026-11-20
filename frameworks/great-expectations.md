---
id: framework/great-expectations
type: framework
slug: great-expectations
schema_version: 1.1
title: Great Expectations
kind: framework
category: framework-category/data
subcategory: data-quality
tagline: Data quality, testing, and documentation for data pipelines
description: Data quality framework that helps validate, document, and profile data. Define expectations about your data, run them against datasets, and generate documentation. Essential for ML data pipeline reliability.
best_for: ML teams needing systematic data quality validation
not_ideal_for: Simple one-off data checks
key_features:
- Declarative data expectations
- 200+ built-in expectations
- Auto-generated data documentation
- Data profiling
- Checkpoint and validation pipeline
- Multiple data backends (pandas, Spark, SQL)
use_cases:
- ML data pipeline validation
- Data quality monitoring
- Data documentation generation
pros:
- Rich set of built-in expectations
- Good documentation generation
- Framework-agnostic
cons:
- Setup can be complex
- v1.x rewrite changed many APIs
- Overhead for simple validation needs
language: Python
languages_supported:
- Python
maintained_by: Great Expectations / Superconductive
first_release: '2018-09-01'
license_spdx: Apache-2.0
github_url: https://github.com/great-expectations/great_expectations
docs_url: https://docs.greatexpectations.io/
website_url: https://greatexpectations.io/
gpu_support:
  nvidia_cuda: false
  amd_rocm: false
  apple_mps: false
  intel_oneapi: false
  google_tpu: false
learning_curve: medium
community_size: medium
maturity: production
signal_strength: medium
backing:
  type: corporate
  orgs:
  - Superconductive
  funding_or_parent: Series B $40M led by Tiger Global (2022)
registry_signals:
  github_stars: 11942
  downloads_monthly: 1500000
  latest_version: 1.25.0
  latest_release_date: '2026-11-12'
  observed_at: '2026-11-20'
  source: https://github.com/great-expectations/great_expectations
aliases:
- great-expectations/great_expectations
tags:
- data-processing
- data-quality
- validation
- testing
updated: '2026-11-20'
sources:
- url: https://github.com/great-expectations/great_expectations
  title: GitHub repository
- url: https://docs.greatexpectations.io/
  title: Documentation
---

## Overview

Data quality framework that helps validate, document, and profile data. Define expectations about your data, run them against datasets, and generate documentation. Essential for ML data pipeline reliability.
