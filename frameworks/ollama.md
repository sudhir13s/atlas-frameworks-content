---
id: framework/ollama
type: framework
slug: ollama
schema_version: 1.1
title: Ollama
kind: tool
category: framework-category/llm-frameworks
subcategory: inference-runtime
tagline: Start building with open models, locally or in the cloud.
description: Ollama runs open models on your own computer or through Ollama's cloud models, from a CLI, a REST API and official Python and JavaScript libraries. It uses llama.cpp as its supported backend and can connect models to desktop apps and coding agents.
best_for: Running open models locally, Building applications on open models
key_features:
- Download and run models from the CLI
- REST API for running and managing models
- Modelfile for custom models
- Concurrent model loading
- OpenAI and Anthropic compatible APIs
- Cloud models without a local GPU
use_cases:
- Running open models on a local machine
- Connecting coding agents to open models
- Building applications on local or cloud models
pros:
- Installers for macOS Windows and Linux plus an official Docker image
- Official Python and JavaScript libraries
language: Go
languages_supported:
- Python
- JavaScript
maintained_by: Ollama
license_spdx: MIT
github_url: https://github.com/ollama/ollama
docs_url: https://docs.ollama.com/
website_url: https://ollama.com/
backing:
  type: corporate
  orgs:
  - Ollama
alternatives:
- framework/llama-cpp
ecosystem_connections:
- framework/llama-cpp
- framework/langchain
registry_signals:
  github_stars: 187735
  downloads_monthly: 5000000
  latest_version: 0.40.16
  latest_release_date: '2026-11-09'
  observed_at: '2026-11-20'
  source: https://github.com/ollama/ollama
aliases:
- ollama/ollama
tags:
- llm
- local
- developer-tools
- inference
- easy-setup
updated: '2026-11-21'
sources:
- url: https://github.com/ollama/ollama
  title: GitHub repository
- url: https://docs.ollama.com/
  title: Documentation
- url: https://docs.ollama.com/gpu
  title: Hardware support
- url: https://docs.ollama.com/faq
  title: Local FAQ
- url: https://docs.ollama.com/api/openai-compatibility
  title: OpenAI compatibility
---

## Overview

Ollama runs open models on your own computer or through Ollama's cloud models, from a CLI, a REST API and official Python and JavaScript libraries. It uses llama.cpp as its supported backend and can connect models to desktop apps and coding agents.
