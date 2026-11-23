---
id: framework/great-expectations
type: framework
slug: great-expectations
schema_version: 3.0
title: Great Expectations
status: curated
kind: framework
category: framework-category/data
subcategory: data-quality
tagline: 'Data quality testing with Expectations: expressive and extensible unit tests for your data.'
description: GX Core is a Python library for data quality testing built on Expectations, which are expressive and extensible unit tests for data. Expectations are grouped into suites and run against data sources such as SQL tables and Spark DataFrames through validation definitions and Checkpoints. Data Docs turn Expectation Suites and validation results into human-readable documentation.
best_for: Data quality testing, Validating data in production data pipelines
key_features:
- Expectations as checkable statements about data
- Expectation Suites applied together
- Checkpoints for validating data in production
- Actions that process validation results such as sending alerts
- Data Docs generated from validation results
- SQL, Spark and cloud object storage data sources
use_cases:
- Data pipeline validation
- Data quality monitoring
- Data documentation generation
pros:
- Generates documentation for each set of validation results
- Expectations are extensible
language: Python
languages_supported:
- Python
maintained_by: Fivetran
license_spdx: Apache-2.0
github_url: https://github.com/fivetran/great_expectations
docs_url: https://docs.greatexpectations.io/
website_url: https://greatexpectations.io/
maturity: production
backing:
  type: corporate
  orgs:
  - Fivetran
registry_signals:
  github_stars: 11942
  downloads_monthly: 1500000
  latest_version: 1.25.0
  latest_release_date: '2026-11-12'
  observed_at: '2026-11-20'
  source: https://github.com/great-expectations/great_expectations
aliases:
- great-expectations/great_expectations
- fivetran/great_expectations
tags:
- data-processing
- data-quality
- validation
- testing
updated: '2026-11-21'
sources:
- url: https://github.com/fivetran/great_expectations
  title: GitHub repository
- url: https://docs.greatexpectations.io/
  title: Documentation
- url: https://docs.greatexpectations.io/docs/core/introduction/gx_overview
  title: GX Core overview
- url: https://github.com/fivetran
  title: Fivetran on GitHub
- url: https://pypi.org/project/great-expectations/
  title: great-expectations — PyPI
---


