---
id: framework-category/rag
type: framework-category
slug: rag
schema_version: 3.0
title: RAG Frameworks
label: RAG
layer: build
order: 4
short_description: Tooling for retrieval-augmented generation — ingest, chunk, embed, retrieve, and ground the LLM in sources.
why_it_matters: RAG is how you give a model fresh, private, or domain knowledge without retraining it.
defacto:
  framework_id: framework/llamaindex
  reason: Open-source framework for retrieval over your data, with data connectors, indices, retrievers and query engines.
rising:
- framework_id: framework/langchain
  reason: Interoperable components and third-party integrations, including document loaders, embeddings and vector stores for retrieval.
- framework_id: framework/haystack
  reason: Modular pipelines with built-in components for retrieval, indexing and evaluation.
alternatives:
- framework_id: framework/dspy
  reason: Optimizes the prompts and weights of a modular program, such as a RAG pipeline, instead of hand-written prompts.
- framework_id: framework/sentence-transformers
  reason: Computes embeddings and reranker (Cross-Encoder) scores for semantic search and retrieval.
key_concepts:
- chunking
- embeddings
- retrieval
- hybrid search
- reranking
canonical_reading:
- title: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
  url: https://arxiv.org/abs/2005.11401
- title: LlamaIndex — high-level concepts
  url: https://developers.llamaindex.ai/python/framework/getting_started/concepts/
- title: LangChain — RAG with Deep Agents
  url: https://docs.langchain.com/oss/python/deepagents/rag
tags:
- rag
- retrieval
- embeddings
updated: '2026-11-21'
sources:
- url: https://github.com/run-llama/llama_index
  title: LlamaIndex repository
  trust: 0.9
- url: https://github.com/langchain-ai/langchain
  title: LangChain repository
  trust: 0.9
- url: https://docs.langchain.com/oss/python/deepagents/retrieval
  title: LangChain — Retrieval
  trust: 0.9
- url: https://github.com/deepset-ai/haystack
  title: Haystack repository
  trust: 0.9
- url: https://github.com/stanfordnlp/dspy
  title: DSPy repository
  trust: 0.9
- url: https://github.com/huggingface/sentence-transformers
  title: Sentence Transformers repository
  trust: 0.9
- url: https://arxiv.org/abs/2005.11401
  title: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
  trust: 0.9
---


