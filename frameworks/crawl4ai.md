---
id: framework/crawl4ai
type: framework
slug: crawl4ai
schema_version: 3.0
title: Crawl4AI
status: curated
kind: library
category: framework-category/rag
subcategory: web-crawling
tagline: Apache-2.0 web crawler that turns pages into clean Markdown for RAG and extracts structured JSON, as a Python library or a self-hosted server.
description: Crawl4AI is an open-source web crawler and scraper that takes URLs, raw HTML or local files and returns clean Markdown for RAG or structured JSON. It drives Chromium, Firefox or WebKit through Playwright, crawls sites deeply or adaptively, filters boilerplate and extracts data with CSS and XPath schemas or an LLM. It runs as a Python library, a CLI, a self-hosted Docker server with a REST API and MCP, or the hosted Crawl4AI Cloud.
best_for: Turning web pages into Markdown for RAG, Structured data extraction from websites, Self-hosted crawling
key_features:
- Clean Markdown with headings, lists, tables and code blocks
- Fit Markdown filters, including a BM25 content filter for a query
- CSS, XPath and regex extraction without an LLM
- LLM extraction into a typed JSON schema
- Topic, regex and sentence chunking with cosine similarity matching
- Deep crawl with BFS, DFS and best-first strategies
- Adaptive crawling and URL discovery from sitemaps and Common Crawl
- Sessions, proxies, persistent browser profiles and stealth mode
- Docker server with REST API and MCP
use_cases:
- Web ingestion for RAG pipelines
- Structured data extraction from web pages
- Crawling sites to build datasets
- Web access for AI agents through MCP
pros:
- Library and self-hosted server are free under Apache-2.0
- Works with open-source or hosted LLM providers for extraction
- AMD64 and ARM64 Docker images
cons:
- Attribution is required when using Crawl4AI
- Web search, SERP and answer APIs are only in the hosted cloud
language: Python
languages_supported:
- Python
maintained_by: unclecode
license_spdx: Apache-2.0
github_url: https://github.com/unclecode/crawl4ai
docs_url: https://docs.crawl4ai.com/
website_url: https://crawl4ai.com/
registry_signals:
  github_stars: 87736
  downloads_monthly: 1676037
  latest_version: 0.9.6
  latest_release_date: '2026-11-20'
  observed_at: '2026-11-24'
  source: https://github.com/unclecode/crawl4ai
aliases:
- unclecode/crawl4ai
- crawl4ai
tags:
- crawler
- web-crawler
- web-scraping
- markdown
- data-extraction
- rag
- playwright
- mcp
updated: '2026-11-24'
sources:
- url: https://github.com/unclecode/crawl4ai
  title: GitHub repository
- url: https://raw.githubusercontent.com/unclecode/crawl4ai/HEAD/README.md
  title: README
- url: https://pypi.org/project/crawl4ai/
  title: crawl4ai — PyPI
- url: https://pypistats.org/api/packages/crawl4ai/recent
  title: crawl4ai — PyPI download statistics
---


