---
id: framework/polars
type: framework
slug: polars
schema_version: 1.1
title: Polars
kind: library
category: framework-category/data
subcategory: dataframe
tagline: Query engine for DataFrames, written in Rust.
description: Polars is an analytical query engine for DataFrames written in Rust, with APIs for Python, Rust, Node.js and R. Queries written with the DataFrame API or in SQL run through the same optimizer and engine, with multi-threaded vectorized execution, a streaming API for data that does not fit in memory and optional NVIDIA GPU acceleration.
best_for: Structured data manipulation, Analytical queries over DataFrames and SQL
key_features:
- Multi-threaded vectorized execution in Rust
- Lazy evaluation with query optimization
- Apache Arrow interoperability with zero-copy sharing
- Streaming for larger-than-memory datasets
- SQL interface
- Expression-based API
use_cases:
- Data processing and analysis
- Reading and writing data across files, cloud storage and databases
- Migrating DataFrame code from pandas
pros:
- DataFrame and SQL queries share one optimizer and engine
- Operations that exceed available RAM can spill to disk
- Expression and I/O plugins for custom code
cons:
- GPU support is in open beta
language: Rust
languages_supported:
- Python
- Rust
- Node.js
- R
maintained_by: Polars B.V.
license_spdx: MIT
github_url: https://github.com/pola-rs/polars
docs_url: https://docs.pola.rs/
website_url: https://www.pola.rs/
maturity: production
backing:
  type: corporate
  orgs:
  - Polars B.V.
alternatives:
- framework/dask
registry_signals:
  github_stars: 40394
  downloads_monthly: 69107592
  latest_version: 2.1.0
  latest_release_date: '2026-10-25'
  observed_at: '2026-11-20'
  source: https://github.com/pola-rs/polars
aliases:
- pola-rs/polars
tags:
- data-processing
- high-performance
- rust
- dataframe
updated: '2026-11-21'
sources:
- url: https://github.com/pola-rs/polars
  title: GitHub repository
- url: https://docs.pola.rs/
  title: Documentation
- url: https://pola.rs/
  title: Website
- url: https://pypi.org/project/polars/
  title: polars — PyPI
---

## Overview

Polars is an analytical query engine for DataFrames written in Rust, with APIs for Python, Rust, Node.js and R. Queries written with the DataFrame API or in SQL run through the same optimizer and engine, with multi-threaded vectorized execution, a streaming API for data that does not fit in memory and optional NVIDIA GPU acceleration.
