---
id: framework/firecrawl
type: framework
slug: firecrawl
schema_version: 3.0
title: Firecrawl
status: curated
kind: tool
category: framework-category/rag
subcategory: web-crawling
tagline: Search, scrape and access 550+ data providers through one API.
description: Firecrawl turns websites into LLM-ready output such as clean Markdown, HTML, links, screenshots or structured JSON, and gives AI agents web search through one API. Its Scrape, Crawl, Map and Batch Scrape endpoints take URLs, and Parse takes uploaded PDFs, Office files and other documents and returns Markdown, layout blocks or JSON, with OCR for scanned pages. It runs as Firecrawl Local on one machine, as a self-hosted server or as the hosted Firecrawl Cloud.
best_for: Web content ingestion for RAG and agents, Converting websites and documents to Markdown, Web search for AI agents
key_features:
- Scrape to Markdown, HTML, raw HTML and links
- Crawl, Map and Batch Scrape for whole sites
- Parse for PDF, Word, Excel, PowerPoint, OpenDocument, EPUB, CSV and HTML files
- Layout blocks with bounding boxes and OCR fallback for scanned pages
- Structured JSON extraction from a schema or prompt
- Web search with full page content
- MCP server, CLI and agent skills
- SDKs for Python, Node.js, Go, Java, Rust, Ruby, .NET, PHP and Elixir
use_cases:
- Web data ingestion for RAG
- Document parsing to Markdown or JSON
- Web search and browsing for AI agents
- Structured data extraction from websites
pros:
- Firecrawl Local runs as one binary without a database, queue or container
- Self-hosting with Docker Compose, Kubernetes manifests or a Helm chart
- Integrations with Zapier, n8n and Lovable
cons:
- Structured JSON, screenshots, Interact, Agent and search need Firecrawl Cloud
- Alexandria data providers are not included in the self-hosted server
- By default a page Firecrawl Local cannot load is fetched through Firecrawl Cloud unless FIRECRAWL_CLOUD is turned off
language: TypeScript
languages_supported:
- Python
- JavaScript
- Go
- Java
- Rust
- Ruby
- C#
- PHP
- Elixir
maintained_by: Firecrawl
license_spdx: AGPL-3.0
github_url: https://github.com/firecrawl/firecrawl
docs_url: https://docs.firecrawl.dev
website_url: https://firecrawl.dev
backing:
  type: corporate
  orgs:
  - Firecrawl
registry_signals:
  github_stars: 208127
  downloads_monthly: 6700227
  latest_version: 4.57.0
  latest_release_date: '2026-11-12'
  observed_at: '2026-11-24'
  source: https://github.com/firecrawl/firecrawl
aliases:
- firecrawl/firecrawl
- firecrawl
tags:
- crawler
- web-scraping
- web-crawler
- html-to-markdown
- data-extraction
- web-search
- ai-agents
- markdown
updated: '2026-11-24'
sources:
- url: https://github.com/firecrawl/firecrawl
  title: GitHub repository
- url: https://raw.githubusercontent.com/firecrawl/firecrawl/HEAD/README.md
  title: README
- url: https://docs.firecrawl.dev/features/parse
  title: Parse
- url: https://pypi.org/project/firecrawl-py/
  title: firecrawl-py — PyPI
- url: https://pypistats.org/api/packages/firecrawl-py/recent
  title: firecrawl-py — PyPI download statistics
---


