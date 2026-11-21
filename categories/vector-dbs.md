---
id: framework-category/vector-dbs
type: framework-category
slug: vector-dbs
schema_version: 2.1
title: Vector Databases
label: Vector Databases
layer: build
order: 8
short_description: Stores that index embeddings for fast approximate nearest-neighbour search, used for retrieval in RAG and semantic search.
why_it_matters: They keep nearest-neighbour search over embeddings fast as a collection grows, together with filtering on metadata.
defacto:
  framework_id: framework/chromadb
  reason: Open-source; its getting-started guide runs an in-memory client inside your program, with a persistent client or client-server mode when data must persist.
rising:
- framework_id: framework/qdrant
  reason: Vector database written in Rust that stores a payload with each vector and has extended filtering support.
- framework_id: framework/lancedb
  reason: Built on the Lance columnar format; the open-source edition is embedded in your application's process, with data on local disk or in object storage.
alternatives:
- framework_id: framework/weaviate
  reason: Vector database that stores objects and vectors, combining vector search with keyword filtering, RAG and reranking in one query interface.
- framework_id: framework/milvus
  reason: Distributed, Kubernetes-native vector database built for search over billions of vectors, with a standalone mode and Milvus Lite.
- framework_id: framework/faiss
  reason: Meta's library for similarity search and clustering of dense vectors, in C++ with Python wrappers and GPU implementations; a library, not a database.
- framework_id: framework/pinecone
  reason: Fully managed vector database, used through its client SDKs.
key_concepts:
- embeddings
- approximate nearest neighbour
- HNSW
- metadata filtering
- hybrid search
canonical_reading:
- title: Chroma — getting started
  url: https://docs.trychroma.com/docs/overview/getting-started
- title: Qdrant — quickstart
  url: https://qdrant.tech/documentation/quickstart/
- title: Faiss — wiki
  url: https://github.com/facebookresearch/faiss/wiki
tags:
- vector-db
- retrieval
- ann
- embeddings
updated: '2026-11-21'
sources:
- url: https://github.com/chroma-core/chroma
  title: Chroma repository
  trust: 0.9
- url: https://docs.trychroma.com/docs/overview/getting-started
  title: Chroma — getting started
  trust: 0.9
- url: https://github.com/qdrant/qdrant
  title: Qdrant repository
  trust: 0.9
- url: https://github.com/lancedb/lancedb
  title: LanceDB repository
  trust: 0.9
- url: https://github.com/weaviate/weaviate
  title: Weaviate repository
  trust: 0.9
- url: https://github.com/milvus-io/milvus
  title: Milvus repository
  trust: 0.9
- url: https://github.com/facebookresearch/faiss
  title: Faiss repository
  trust: 0.9
- url: https://www.pinecone.io/
  title: Pinecone
  trust: 0.9
---
