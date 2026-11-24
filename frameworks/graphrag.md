---
id: framework/graphrag
type: framework
slug: graphrag
schema_version: 3.0
title: GraphRAG
status: curated
kind: tool
category: framework-category/rag
subcategory: graph-rag
tagline: A modular graph-based Retrieval-Augmented Generation (RAG) system.
description: GraphRAG is a data pipeline and transformation suite from Microsoft Research that uses LLMs to extract a knowledge graph from unstructured text. Indexing slices the corpus into TextUnits, extracts entities, relationships and claims, clusters the graph into a community hierarchy with the Leiden technique and summarizes each community. At query time these structures fill the LLM context through Global, Local, DRIFT or Basic search.
best_for: Questions that connect information across many documents, Holistic questions over a whole private corpus
key_features:
- Entity, relationship and claim extraction with LLMs
- Hierarchical community clustering with the Leiden technique
- Bottom-up community summaries
- Global Search over community summaries
- Local Search fanning out from specific entities
- DRIFT Search with community context
- Basic Search with top-k vector search
- Prompt tuning guide and command-line interface
use_cases:
- Question answering over private document collections
- Summarizing themes across a large corpus
- Building a knowledge graph from text
pros:
- Graph structures add references back to the source TextUnits
- Several query modes for holistic and entity-specific questions
cons:
- Largely in maintenance mode, with no new features or pull requests accepted
- Indexing can be an expensive operation
- Out-of-the-box prompts may not give the best results without prompt tuning
- Code is a demonstration and not an officially supported Microsoft offering
language: Python
languages_supported:
- Python
maintained_by: Microsoft Research
license_spdx: MIT
github_url: https://github.com/microsoft/graphrag
docs_url: https://microsoft.github.io/graphrag/
website_url: https://microsoft.github.io/graphrag/
backing:
  type: corporate
  orgs:
  - organization/microsoft
registry_signals:
  github_stars: 36729
  downloads_monthly: 43816
  latest_version: 3.3.0
  latest_release_date: '2026-10-08'
  observed_at: '2026-11-24'
  source: https://github.com/microsoft/graphrag
aliases:
- microsoft/graphrag
- graphrag
tags:
- graphrag
- rag
- knowledge-graph
- llm
updated: '2026-11-24'
sources:
- url: https://github.com/microsoft/graphrag
  title: GitHub repository
- url: https://raw.githubusercontent.com/microsoft/graphrag/HEAD/README.md
  title: README
- url: https://microsoft.github.io/graphrag/
  title: Documentation
- url: https://pypi.org/project/graphrag/
  title: graphrag — PyPI
- url: https://pypistats.org/api/packages/graphrag/recent
  title: graphrag — PyPI download statistics
---


