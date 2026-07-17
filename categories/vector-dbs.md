---
id: framework-category/vector-dbs
type: framework-category
slug: vector-dbs
schema_version: 1.0
title: "Vector Databases"
label: "Vector Databases"
order: 8
shortDescription: "Stores that index embeddings for fast approximate nearest-neighbour search — the retrieval backbone of RAG and semantic search."
whyItMatters: "They turn embeddings into a queryable index at scale; the wrong choice caps recall, latency, or how far you can grow."
defacto:
  frameworkId: chromadb
  reason: "The zero-config, embedded default for development — runs in-process so there is no server to operate while you prototype."
rising:
  - frameworkId: qdrant
    reason: "Rust-based, high-performance, with rich filtering; a common production graduation from Chroma."
  - frameworkId: lancedb
    reason: "Embedded, on-disk vector store built on the Lance columnar format; scales locally without a server."
alternatives:
  - frameworkId: weaviate
    reason: "Feature-rich vector database with hybrid search and modules."
  - frameworkId: milvus
    reason: "Built for billion-scale vector search in production."
  - frameworkId: faiss
    reason: "Meta's ANN library — not a database, but the engine inside many of them."
  - frameworkId: pinecone
    reason: "Fully managed, hosted vector DB when you would rather not run infrastructure."
keyConcepts:
  - "embeddings"
  - "approximate nearest neighbour"
  - "HNSW"
  - "metadata filtering"
  - "hybrid search"
canonicalReading:
  - title: "Chroma — getting started"
    url: "https://docs.trychroma.com/docs/overview/getting-started"
  - title: "Qdrant — quickstart"
    url: "https://qdrant.tech/documentation/quickstart/"
  - title: "Faiss — wiki"
    url: "https://github.com/facebookresearch/faiss/wiki"
didYouKnow:
  - "FAISS was released by Meta in 2017 and still powers many commercial vector DBs internally."
  - "HNSW is the dominant ANN index; it has been the default for a decade."
  - "Qdrant is written in Rust; its query engine runs without a Python dependency."
tags: [vector-db, retrieval, ann, embeddings]
updated: 2026-07-17
sources:
  - { url: "https://docs.trychroma.com/", title: "Chroma documentation", trust: 0.9 }
  - { url: "https://qdrant.tech/documentation/", title: "Qdrant documentation", trust: 0.9 }
  - { url: "https://github.com/facebookresearch/faiss/wiki", title: "Faiss wiki", trust: 0.9 }
---

## Overview
A vector database indexes embeddings and answers nearest-neighbour queries fast. It is the retrieval
backbone under RAG, semantic search, recommendations, and deduplication — anywhere you compare meaning
rather than exact text.

## Landscape
Chroma is the zero-config embedded default for prototyping. Qdrant (Rust, strong filtering) and LanceDB
(embedded, on-disk) are the common next steps. Weaviate and Milvus target feature-rich and
billion-scale production respectively. Faiss is not a database but the ANN engine inside many of them,
and Pinecone is the fully managed option when you would rather not run infrastructure.

## Notes
Start embedded (Chroma/LanceDB) and graduate to a server (Qdrant/Weaviate/Milvus) when the corpus or
QPS demands it. Two things dominate quality: metadata filtering (to scope retrieval) and hybrid search
(dense + keyword), which usually beats pure vector search on real corpora.
