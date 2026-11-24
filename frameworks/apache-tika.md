---
id: framework/apache-tika
type: framework
slug: apache-tika
schema_version: 3.0
title: Apache Tika
status: curated
kind: library
category: framework-category/document-parsing
subcategory: content-extraction
tagline: The Apache Tika toolkit detects and extracts metadata and text from over a thousand different file types (such as PPT, XLS, and PDF).
description: Apache Tika is a Java toolkit that detects file types and extracts metadata and text from over a thousand formats, used as a Java library, a command-line app or tika-server. Since 4.0.0 it emits Markdown by default, with plain text or structured recursive JSON that covers the document and anything embedded in it. It parses in crash-isolated forked processes and adds vision-language-model parsers for documents OCR cannot read.
best_for: Text and metadata extraction across many file types, Java document pipelines, Converting files to Markdown for RAG
key_features:
- File-type detection
- Text and metadata extraction from over a thousand file types
- Markdown output by default since 4.0.0
- Structured recursive JSON for embedded documents
- Crash-isolated forked parsing
- Vision-language-model parsers using Claude, Gemini or OpenAI
- Java API, command-line app and tika-server
use_cases:
- Converting documents to Markdown for LLM and RAG pipelines
- Metadata extraction at scale
- Extracting embedded files and attachments
pros:
- Process isolation so a hostile document takes down a fork, not the service
- Agent skills for file-to-Markdown included in the repository
- Reproducible builds
cons:
- Requires Java 17
language: Java
languages_supported:
- Java
maintained_by: Apache Software Foundation
license_spdx: Apache-2.0
github_url: https://github.com/apache/tika
website_url: https://tika.apache.org/
backing:
  type: foundation
  orgs:
  - Apache Software Foundation
registry_signals:
  github_stars: 4155
  latest_version: 4.2.0
  latest_release_date: '2026-10-28'
  observed_at: '2026-11-24'
  source: https://github.com/apache/tika
aliases:
- apache/tika
- Tika
tags:
- content
- extraction
- metadata
- java
- tika
updated: '2026-11-24'
sources:
- url: https://github.com/apache/tika
  title: GitHub repository
- url: https://raw.githubusercontent.com/apache/tika/HEAD/README.md
  title: README
- url: https://tika.apache.org/
  title: Website
---


