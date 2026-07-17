---
id: framework-category/rag
type: framework-category
slug: rag
schema_version: 1.0
title: "RAG Frameworks"
label: "RAG"
order: 4
shortDescription: "Tooling for retrieval-augmented generation — ingest, chunk, embed, retrieve, and ground the LLM in sources."
whyItMatters: "RAG is how you give a model fresh, private, or domain knowledge without retraining it."
defacto:
  frameworkId: llamaindex
  reason: "Data-first framework purpose-built for RAG: loaders, indices, retrievers, and query engines out of the box."
rising:
  - frameworkId: langchain
    reason: "Broadest integrations; its retriever + chain abstractions are a common RAG starting point."
  - frameworkId: haystack
    reason: "Production-grade retrieval pipelines from deepset, strong on hybrid search and evaluation."
alternatives:
  - frameworkId: dspy
    reason: "Optimizes the retrieve-then-generate program end to end instead of hand-tuning prompts."
  - frameworkId: sentence-transformers
    reason: "The embedding + reranking workhorse most RAG stacks depend on underneath."
keyConcepts:
  - "chunking"
  - "embeddings"
  - "retrieval"
  - "hybrid search"
  - "reranking"
canonicalReading:
  - title: "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
    url: "https://arxiv.org/abs/2005.11401"
  - title: "LlamaIndex — high-level concepts"
    url: "https://docs.llamaindex.ai/en/stable/getting_started/concepts/"
  - title: "LangChain — RAG tutorial"
    url: "https://python.langchain.com/docs/tutorials/rag/"
didYouKnow:
  - "The original RAG paper (Lewis et al., 2020) predates ChatGPT by two years."
  - "Hybrid search (dense + BM25) usually beats pure vector search on real corpora."
  - "Rerankers can recover more quality than a 10x larger embedding model."
tags: [rag, retrieval, embeddings]
updated: 2026-07-17
sources:
  - { url: "https://docs.llamaindex.ai/en/stable/", title: "LlamaIndex documentation", trust: 0.9 }
  - { url: "https://arxiv.org/abs/2005.11401", title: "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks", trust: 0.95 }
  - { url: "https://haystack.deepset.ai/", title: "Haystack documentation", trust: 0.85 }
---

## Overview
RAG grounds an LLM in retrieved context: you index a corpus, retrieve the most relevant chunks per
query, and pass them to the model. It is the standard cure for stale knowledge and hallucination when
the answer lives in documents you control.

## Landscape
LlamaIndex is the RAG-first choice, with the richest set of loaders, indices, and query engines.
LangChain is the broad, integration-heavy alternative many teams start with. Haystack targets
production retrieval with strong hybrid search and evaluation. DSPy optimizes the whole
retrieve-then-generate program, and Sentence-Transformers is the embedding/reranking layer underneath
most stacks.

## Notes
Quality comes from retrieval, not the model — invest in chunking, hybrid search, and a reranker before
reaching for a bigger LLM. Always keep a small labelled question set; "it looks right" is not a metric,
and RAG systems earn trust through traceable citations.
