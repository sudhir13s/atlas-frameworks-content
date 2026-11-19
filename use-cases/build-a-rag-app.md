---
id: use-case/build-a-rag-app
type: use-case
slug: build-a-rag-app
schema_version: 1.1
title: Build a RAG App
label: Build a RAG app
order: 1
goal: Answer questions over your own documents by retrieving relevant chunks and grounding an LLM's response in them.
languages:
- python
- typescript
levels:
- beginner
- intermediate
stack:
- framework_id: framework/langchain
  role: Orchestration
  why: Ties loaders, splitters, retriever, and the LLM into one chain with minimal glue code.
  install: pip install langchain langchain-community
  quickstart_url: https://python.langchain.com/docs/tutorials/rag/
  docs_url: https://python.langchain.com/docs/introduction/
- framework_id: framework/chromadb
  role: Vector store
  why: Embedded, zero-config vector DB — runs in-process so there is no server to operate on day one.
  install: pip install chromadb
  quickstart_url: https://docs.trychroma.com/docs/overview/getting-started
  docs_url: https://docs.trychroma.com/
- framework_id: framework/sentence-transformers
  role: Embeddings
  why: High-quality open embedding models (e.g. all-MiniLM-L6-v2) that run locally and free.
  install: pip install sentence-transformers
  quickstart_url: https://www.sbert.net/docs/quickstart.html
  docs_url: https://www.sbert.net/
- framework_id: framework/ollama
  role: LLM inference
  why: Runs an open chat model locally with an OpenAI-compatible API, so the loop costs nothing to iterate on.
  install: curl -fsSL https://ollama.com/install.sh | sh
  quickstart_url: https://github.com/ollama/ollama/blob/main/README.md#quickstart
  docs_url: https://github.com/ollama/ollama/tree/main/docs
day1_plan:
- step: 1
  task: Load and split your documents
  estimate: 30 min
  details: Use a LangChain document loader, then a RecursiveCharacterTextSplitter (~1000 chars, 200 overlap).
- step: 2
  task: Embed and index the chunks
  estimate: 30 min
  details: Embed with all-MiniLM-L6-v2 via sentence-transformers and upsert into a persistent Chroma collection.
- step: 3
  task: Wire retrieval + generation
  estimate: 45 min
  details: Retrieve top-k chunks, stuff them into a prompt template, and call the local Ollama model.
- step: 4
  task: Evaluate and tune
  estimate: 45 min
  details: Spot-check 10 questions; adjust chunk size, k, and the prompt. Add a citation of the source chunk.
starter_templates:
- name: rag-from-scratch
  repo: https://github.com/langchain-ai/rag-from-scratch
  why: Official LangChain notebooks that build RAG up from first principles.
- name: Chroma examples
  repo: https://github.com/chroma-core/chroma/tree/main/examples
  why: Minimal, runnable indexing + query examples straight from the Chroma repo.
learn_next:
- title: Retrieval-Augmented Generation (Lewis et al., 2020)
  url: https://arxiv.org/abs/2005.11401
  kind: paper
- title: LangChain RAG tutorial
  url: https://python.langchain.com/docs/tutorials/rag/
  kind: docs
- title: 'Sentence-Transformers: Semantic Search'
  url: https://www.sbert.net/examples/applications/semantic-search/README.html
  kind: docs
pitfalls:
- 'Chunking too large: 4k-char chunks bury the answer in noise. Start ~1000 chars with overlap and measure.'
- 'Skipping evaluation: ''it looks right'' is not a metric. Keep a small labelled question set from day one.'
- 'Ignoring the embedding-model / query mismatch: embed documents and queries with the *same* model.'
when_to_level_up: When recall is the bottleneck, add hybrid search (dense + BM25) and a reranker; when the corpus outgrows in-process Chroma, move to a server-backed store like Qdrant or Weaviate.
community:
- name: LangChain Discord
  url: https://www.langchain.com/join-community
- name: r/LocalLLaMA
  url: https://www.reddit.com/r/LocalLLaMA/
- name: Hugging Face Forums
  url: https://discuss.huggingface.co/
dont_use:
- what: Fine-tuning the base model
  why: RAG injects fresh knowledge at query time; fine-tuning to add facts is slower, costlier, and goes stale.
- what: A hosted vector DB (Pinecone) on day one
  why: Adds an account, a key, and network latency before you have even validated retrieval quality locally.
related_use_cases:
- use-case/build-an-agent
- use-case/build-multimodal-app
tags:
- rag
- retrieval
- embeddings
- llm
updated: '2026-11-19'
sources:
- url: https://python.langchain.com/docs/tutorials/rag/
  title: LangChain — RAG tutorial
  trust: 0.9
- url: https://docs.trychroma.com/docs/overview/getting-started
  title: Chroma — Getting Started
  trust: 0.9
- url: https://arxiv.org/abs/2005.11401
  title: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
  trust: 0.95
---

## Overview

Retrieval-Augmented Generation grounds an LLM in your own documents: you index the corpus once, then
at query time retrieve the most relevant chunks and pass them to the model as context. The result is
answers backed by sources you control, with none of the base model's knowledge cut-off problem.

## Why this stack

LangChain removes the boilerplate between a loader, a splitter, a retriever, and the LLM. Chroma runs
in-process, so there is no server to stand up while you are still validating retrieval quality.
Sentence-Transformers gives you strong open embeddings for free, and Ollama serves an open chat model
locally so every iteration of the loop costs nothing. Every piece here is open source and swappable.

## Notes

The two dials that move quality most are chunking and `k` (how many chunks you retrieve). Measure on a
small labelled set before reaching for a bigger model. Keep the source of each retrieved chunk so the
answer can cite it — trust in a RAG system comes from traceability, not fluency.
