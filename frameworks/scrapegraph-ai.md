---
id: framework/scrapegraph-ai
type: framework
slug: scrapegraph-ai
schema_version: 3.0
title: ScrapeGraphAI
status: curated
kind: library
category: framework-category/rag
subcategory: web-scraping
tagline: Python scraper based on AI.
description: ScrapeGraphAI is a Python web scraping library that uses an LLM and graph logic to build scraping pipelines for websites and local documents such as XML, HTML, JSON and Markdown. You give a prompt and a source URL or file, and a graph such as SmartScraperGraph returns the requested information as a dictionary. It works with LLMs through APIs such as OpenAI, Groq, Azure and Gemini, or with local models through Ollama.
best_for: Prompt-driven extraction of structured data from web pages, Scraping with local LLMs
key_features:
- SmartScraperGraph for single-page extraction from a prompt
- SearchGraph over the top search engine results
- Multi-page graphs that call the LLM in parallel
- ScriptCreatorGraph that generates a Python scraping script
- SpeechGraph that generates an audio file
- Local documents in XML, HTML, JSON and Markdown
- Playwright for fetching website content
use_cases:
- Extracting structured information from web pages
- Collecting data across multiple pages or search results
- Generating scraping scripts
pros:
- Works with hosted LLM APIs or local models through Ollama
- Integrations with LangChain, LlamaIndex, CrewAI, Agno and Dify
- MCP server available
cons:
- Browsers, proxies, anti-bot handling and scaling are the user's responsibility in the open-source library
- Collects anonymous usage metrics unless SCRAPEGRAPHAI_TELEMETRY_ENABLED is set to false
- Meant for data exploration and research purposes only
language: Python
languages_supported:
- Python
maintained_by: ScrapeGraphAI
license_spdx: MIT
github_url: https://github.com/ScrapeGraphAI/Scrapegraph-ai
docs_url: https://docs.scrapegraphai.com/introduction
website_url: https://scrapegraphai.com
ecosystem_connections:
- framework/langchain
- framework/llamaindex
- framework/crewai
- framework/agno
- framework/dify
- framework/ollama
registry_signals:
  github_stars: 32903
  downloads_monthly: 46112
  latest_version: 2.3.1
  latest_release_date: '2026-10-06'
  observed_at: '2026-11-24'
  source: https://github.com/ScrapeGraphAI/Scrapegraph-ai
aliases:
- ScrapeGraphAI/Scrapegraph-ai
- Scrapegraph-ai
- scrapegraphai
tags:
- web-scraping
- ai-scraping
- data-extraction
- crawler
- llm
- markdown
- rag
updated: '2026-11-24'
sources:
- url: https://github.com/ScrapeGraphAI/Scrapegraph-ai
  title: GitHub repository
- url: https://raw.githubusercontent.com/ScrapeGraphAI/Scrapegraph-ai/HEAD/README.md
  title: README
- url: https://pypi.org/project/scrapegraphai/
  title: scrapegraphai — PyPI
- url: https://pypistats.org/api/packages/scrapegraphai/recent
  title: scrapegraphai — PyPI download statistics
---


