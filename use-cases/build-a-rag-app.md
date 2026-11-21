---
id: use-case/build-a-rag-app
type: use-case
slug: build-a-rag-app
schema_version: 2.0
title: Build a RAG App
label: Build a RAG app
order: 1
goal: Answer questions over your own documents by retrieving the passages that matter and generating a response grounded in them, with citations back to the source.
stages:
- id: indexing
  name: Indexing
  note: Runs offline whenever documents are added or changed.
- id: query
  name: Query
  note: Runs on every question a user asks.
- id: quality
  name: Quality and operations
  note: Runs before each release and continuously in production.
blocks:
- id: document-parsing
  stage: indexing
  name: Document parsing
  purpose: Turns PDFs, office files and HTML into clean text with headings, tables and reading order preserved, so later steps work on structure rather than raw bytes.
  options:
  - record: framework/docling
    choice: default
    when: MIT-licensed code hosted by the LF AI & Data Foundation that parses PDF, office, HTML and image files into one document model and exports Markdown or lossless JSON, with integrations for LangChain, LlamaIndex and Haystack.
  - record: framework/marker
    choice: alternative
    when: 'Pick it for PDFs heavy in tables, equations and code blocks; its code is Apache-2.0 but its model weights use a modified OpenRAIL-M licence that limits commercial use above a funding or revenue threshold.'
  - record: framework/paddleocr
    choice: alternative
    when: Pick it for scanned pages and images, where its PP-StructureV3 pipeline converts PDFs and images to Markdown or JSON under Apache-2.0.
  how_to_choose:
  - Born-digital PDFs and office files need layout parsing; scanned pages also need optical character recognition (OCR).
  - Check the model-weight licence, not only the code licence, before commercial use.
  - Keep the source file and page for every parsed element so answers can cite it.
  browse:
    label: All RAG data tools
    record: framework-category/rag
- id: chunking
  stage: indexing
  name: Chunking
  purpose: Splits parsed documents into passages small enough to embed and retrieve, keeping each passage on one topic.
  options:
  - record: framework/langchain
    choice: default
    when: Its separate text-splitters package recommends a recursive splitter for generic text that breaks on paragraphs, then sentences, then words, and adds Markdown, HTML, JSON and code splitters.
  - record: framework/llamaindex
    choice: alternative
    when: Pick it when you also index with LlamaIndex; its node parsers include sentence, semantic (embedding-similarity breakpoints) and hierarchical splitters.
  - record: framework/haystack
    choice: alternative
    when: Pick it when the rest of the system is a Haystack pipeline, which ships built-in indexing components.
  how_to_choose:
  - Split by document structure (headings, sections) first; fall back to length only when there is no structure.
  - Measure chunk size against retrieval metrics instead of fixing it once.
  - Use the chunker that ships with your orchestration framework unless a structure it lacks is required.
- id: embedding-model
  stage: indexing
  name: Embedding model
  purpose: Converts each chunk and each query into vectors so that passages with similar meaning sit close together.
  options:
  - record: model/bge-m3
    choice: default
    when: MIT-licensed, covers more than a hundred languages, and produces dense, sparse and multi-vector representations from one model, which gives hybrid search without a second model.
  - record: model/embeddinggemma-300m
    choice: alternative
    when: Pick it for phones, laptops and other constrained hardware; it is built for on-device use and is released under the Gemma terms.
  - record: framework/sentence-transformers
    choice: alternative
    when: Pick it as the library that runs and fine-tunes open embedding, sparse and reranker models when an off-the-shelf model misses your domain vocabulary.
  how_to_choose:
  - Embed documents and queries with the same model and version; changing the model means re-indexing.
  - Compare candidates on the retrieval tasks of the Massive Text Embedding Benchmark (MTEB), then on your own question set.
  - Prefer a model that also emits sparse vectors if you plan hybrid search.
  browse:
    label: All embedding models
    record: task/embedding-models
- id: vector-database
  stage: indexing
  name: Vector database
  purpose: Stores chunk vectors with their text and metadata and returns the nearest chunks to a query, filtered by metadata.
  options:
  - record: framework/qdrant
    choice: default
    when: Apache-2.0, fuses dense and sparse queries for hybrid search, filters on payload fields, and its Python client runs the same API in local mode without a server.
  - record: framework/chromadb
    choice: alternative
    when: Pick it for prototypes; it runs in-process in Python with metadata filters and moves to client-server mode later.
  - record: framework/pgvector
    choice: alternative
    when: Pick it when your data already lives in Postgres; vectors sit next to the rest of your rows with ACID transactions and joins.
  - record: framework/milvus
    choice: alternative
    when: Pick it for horizontally scaled deployments; it runs as Lite, Standalone or distributed on Kubernetes and supports BM25 full-text and sparse vectors.
  - record: framework/pinecone
    choice: alternative
    when: Pick it when you want a service that serves full-text, semantic and hybrid search from one index, with embedding and reranking models hosted by Pinecone.
  how_to_choose:
  - Need metadata filtering (tenant, date, access rights) in the same query as similarity search.
  - Need hybrid search when users type exact names, codes or identifiers.
  - 'Already run Postgres and the corpus fits it: start with pgvector before adding a new system.'
  browse:
    label: All vector databases
    record: framework-category/vector-dbs
- id: retrieval-orchestration
  stage: query
  name: Retrieval and orchestration
  purpose: Rewrites the query if needed, runs retrieval, assembles the prompt with the retrieved chunks, and calls the model.
  options:
  - record: framework/llamaindex
    choice: default
    when: MIT-licensed toolkit built around RAG, with data connectors, indexes, query engines, BM25, fusion and router retrievers, node postprocessors and rerankers in one place.
  - record: framework/langchain
    choice: alternative
    when: Pick it when you need its integration library across model providers, vector stores and retrievers, or plan to grow into LangGraph agents.
  - record: framework/haystack
    choice: alternative
    when: Pick it for explicit, inspectable pipelines with branches and loops that control retrieval, ranking, filtering and routing.
  how_to_choose:
  - Pick one framework and keep the vector database, embedding model and model provider swappable behind it.
  - Prefer explicit pipelines when you must audit exactly which chunks reached the prompt.
  browse:
    label: All LLM frameworks
    record: framework-category/llm-frameworks
- id: reranker
  stage: query
  name: Reranker
  purpose: Rescores the top retrieved chunks against the query with a cross-encoder so the most relevant few reach the prompt.
  options:
  - record: model/qwen3-reranker-0-6b
    choice: default
    when: Apache-2.0 text reranker covering more than a hundred languages with a long context window, and the smallest model in its series.
  - record: model/qwen3-reranker-8b
    choice: alternative
    when: Pick it when reranking quality matters more than latency; it is the largest model in the same series and licence.
  - record: model/jina-reranker-v2-base-multilingual
    choice: alternative
    when: Pick it for research and evaluation only; it is a multilingual cross-encoder licensed CC-BY-NC-4.0.
  how_to_choose:
  - Add a reranker when the right chunk is retrieved but not ranked near the top.
  - Retrieve a wider candidate set, then rerank down to what fits the prompt.
  browse:
    label: All reranking models
    record: task/reranking-models
- id: generating-model
  stage: query
  name: Generating model
  purpose: Writes the answer from the question and the retrieved chunks, citing which chunk supports each claim.
  options:
  - record: model/qwen3-8b
    choice: default
    when: Apache-2.0 open weights, supports more than a hundred languages, and switches between a thinking mode and a non-thinking mode per request.
  - record: model/gpt-oss-20b
    choice: alternative
    when: Pick it for Apache-2.0 weights with configurable reasoning effort and structured outputs; it works correctly only with the harmony response format.
  how_to_choose:
  - Instruct the model to answer only from the supplied context and to say when the context is insufficient.
  - Size the context window to the number of reranked chunks you send.
  browse:
    label: All chat models
    record: task/chat-models
- id: model-serving
  stage: query
  name: Model serving
  purpose: Runs the generating model behind an API the orchestration layer can call.
  options:
  - record: framework/vllm
    choice: default
    when: Apache-2.0 engine with PagedAttention, continuous batching and prefix caching behind an OpenAI-compatible server, on NVIDIA, AMD and Intel GPUs and CPUs.
  - record: framework/ollama
    choice: alternative
    when: Pick it for local development on macOS, Windows or Linux; it pulls and runs open models behind a REST API.
  - record: framework/llama-cpp
    choice: alternative
    when: Pick it for minimal-setup inference on a wide range of hardware, with an OpenAI-compatible server.
  - record: framework/sglang
    choice: alternative
    when: Pick it for high-throughput serving with RadixAttention prefix caching and an OpenAI-compatible API.
  how_to_choose:
  - Use the same OpenAI-compatible API in development and production so only the base URL changes.
  - 'Match the engine to the hardware: GPU servers for vLLM or SGLang, developer machines for Ollama or llama.cpp.'
  browse:
    label: All serving tools
    record: framework-category/llm-serving
- id: grounding-checks
  stage: quality
  name: Grounding and hallucination checks
  purpose: Checks that every claim in an answer is supported by the retrieved chunks before or after it reaches the user.
  options:
  - record: framework/ragas
    choice: default
    when: Its Faithfulness metric splits an answer into claims and scores the share supported by the retrieved context, with an option to replace the model judge with a small classifier.
  - name: HHEM-2.1-Open
    url: https://huggingface.co/vectara/hallucination_evaluation_model
    choice: alternative
    when: Pick it for a per-answer check in production; it is an Apache-2.0 classifier that scores whether a text is supported by its evidence and runs on a CPU.
  - record: framework/deepeval
    choice: alternative
    when: Pick it to run faithfulness and hallucination metrics as pytest-style test cases.
  how_to_choose:
  - Use a small classifier for checks on live traffic and a model judge for offline analysis.
  - Decide in advance what happens to an unsupported answer (block, regenerate, or answer with a warning).
- id: evaluation
  stage: quality
  name: Evaluation
  purpose: Scores retrieval and answers against a labelled question set so every change to chunking, models or prompts is measured.
  options:
  - record: framework/deepeval
    choice: default
    when: Apache-2.0 framework that runs contextual precision, contextual recall, faithfulness and answer relevancy as unit tests, so retrieval regressions fail a CI run.
  - record: framework/ragas
    choice: alternative
    when: Pick it for RAG-specific metrics such as context precision, context recall, noise sensitivity and response relevancy, with experiment and dataset management.
  - record: framework/promptfoo
    choice: alternative
    when: Pick it for MIT-licensed declarative test configs that run locally and in CI, with red teaming of the same app.
  - name: MTEB leaderboard
    url: https://huggingface.co/spaces/mteb/leaderboard
    choice: alternative
    when: Use it before indexing to shortlist embedding and reranking models on public retrieval tasks.
  how_to_choose:
  - Measure retrieval (did the right chunk come back) separately from generation (was the answer correct and supported).
  - Keep a fixed labelled question set and rerun it on every change.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
- id: guardrails
  stage: quality
  name: Guardrails
  purpose: Filters unsafe questions and answers and catches instructions hidden inside retrieved documents.
  options:
  - record: model/llama-guard-4-12b
    choice: default
    when: Classifies both prompts and responses against the MLCommons hazard taxonomy and returns the violated categories; released under the Llama 4 Community License.
  - record: model/llama-prompt-guard-2-86m
    choice: alternative
    when: Pick it to scan retrieved chunks and user input for prompt injection and jailbreaks; it is a small multilingual classifier.
  - record: framework/nemo-guardrails
    choice: alternative
    when: Pick it for Apache-2.0 programmable input, output and retrieval rails, including filtering retrieved content and checking answers against evidence.
  how_to_choose:
  - Treat retrieved documents as untrusted input; indirect prompt injection arrives through them.
  - Filter the input before retrieval and the output before display.
  browse:
    label: All safety and guard models
    record: task/safety-and-guard-models
- id: tracing
  stage: quality
  name: Tracing and observability
  purpose: Records each request's query, retrieved chunks, prompt, answer, latency and cost so failures can be traced to the step that caused them.
  options:
  - record: framework/langfuse
    choice: default
    when: Open-source platform built on OpenTelemetry that traces retrieval, embedding and model calls, runs evaluations on traces, and can be self-hosted.
  - record: framework/langsmith
    choice: alternative
    when: Pick it for tracing and evaluation in one platform, with cloud, hybrid or self-hosted setups.
  - record: framework/mlflow
    choice: alternative
    when: Pick it when you already run MLflow; its tracing is OpenTelemetry-compatible and the data stays on your infrastructure.
  - record: framework/arize-phoenix
    choice: alternative
    when: Pick it for self-hosted OpenTelemetry tracing with retrieval evals; it is licensed under the Elastic License 2.0.
  how_to_choose:
  - Log the IDs of the retrieved chunks with every answer; that is what makes a wrong answer debuggable.
  - Prefer a tool that accepts OpenTelemetry so you can switch backends later.
learn_next:
- title: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
  url: https://arxiv.org/abs/2005.11401
  kind: paper
- title: LangChain text splitters
  url: https://docs.langchain.com/oss/python/integrations/splitters
  kind: docs
- title: Ragas metrics
  url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
  kind: docs
- title: Qdrant hybrid queries
  url: https://qdrant.tech/documentation/concepts/hybrid-queries/
  kind: docs
related_use_cases:
- use-case/build-an-agent
- use-case/build-multimodal-app
- use-case/serve-in-production
- use-case/make-llm-app-safe-and-accurate
tags:
- rag
- retrieval
- embeddings
- vector-search
- evaluation
- llm
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2005.11401
  title: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks (arXiv)
  trust: 0.95
- url: https://github.com/docling-project/docling
  title: Docling repository
  trust: 0.9
- url: https://github.com/datalab-to/marker
  title: marker repository
  trust: 0.9
- url: https://github.com/PaddlePaddle/PaddleOCR
  title: PaddleOCR repository
  trust: 0.9
- url: https://docs.langchain.com/oss/python/integrations/splitters
  title: LangChain text splitters documentation
  trust: 0.9
- url: https://developers.llamaindex.ai/python/framework/module_guides/loading/node_parsers/modules/
  title: LlamaIndex node parser modules
  trust: 0.9
- url: https://huggingface.co/BAAI/bge-m3
  title: BAAI/bge-m3 model card
  trust: 0.9
- url: https://huggingface.co/google/embeddinggemma-300m
  title: google/embeddinggemma-300m model card
  trust: 0.9
- url: https://sbert.net/
  title: Sentence Transformers documentation
  trust: 0.9
- url: https://qdrant.tech/documentation/concepts/hybrid-queries/
  title: Qdrant hybrid queries
  trust: 0.9
- url: https://qdrant.tech/documentation/concepts/filtering/
  title: Qdrant filtering
  trust: 0.9
- url: https://github.com/qdrant/qdrant-client
  title: Qdrant Python client repository
  trust: 0.9
- url: https://github.com/chroma-core/chroma
  title: Chroma repository
  trust: 0.9
- url: https://github.com/pgvector/pgvector
  title: pgvector repository
  trust: 0.9
- url: https://github.com/milvus-io/milvus
  title: Milvus repository
  trust: 0.9
- url: https://docs.pinecone.io/guides/get-started/overview
  title: Pinecone documentation overview
  trust: 0.9
- url: https://developers.llamaindex.ai/python/framework/
  title: LlamaIndex framework documentation
  trust: 0.9
- url: https://github.com/langchain-ai/langchain
  title: LangChain repository
  trust: 0.9
- url: https://github.com/deepset-ai/haystack
  title: Haystack repository
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen3-Reranker-0.6B
  title: Qwen/Qwen3-Reranker-0.6B model card
  trust: 0.9
- url: https://huggingface.co/jinaai/jina-reranker-v2-base-multilingual
  title: jinaai/jina-reranker-v2-base-multilingual model card
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen3-8B
  title: Qwen/Qwen3-8B model card
  trust: 0.9
- url: https://huggingface.co/openai/gpt-oss-20b
  title: openai/gpt-oss-20b model card
  trust: 0.9
- url: https://github.com/vllm-project/vllm
  title: vLLM repository
  trust: 0.9
- url: https://github.com/ollama/ollama
  title: Ollama repository
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp repository
  trust: 0.9
- url: https://docs.sglang.io/
  title: SGLang documentation
  trust: 0.9
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/faithfulness/
  title: Ragas Faithfulness metric
  trust: 0.9
- url: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/
  title: Ragas available metrics
  trust: 0.9
- url: https://huggingface.co/vectara/hallucination_evaluation_model
  title: vectara/hallucination_evaluation_model (HHEM-2.1-Open) model card
  trust: 0.9
- url: https://github.com/confident-ai/deepeval
  title: DeepEval repository
  trust: 0.9
- url: https://github.com/promptfoo/promptfoo
  title: promptfoo repository
  trust: 0.9
- url: https://github.com/embeddings-benchmark/mteb
  title: MTEB repository
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B model card
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-86M
  title: meta-llama/Llama-Prompt-Guard-2-86M model card
  trust: 0.9
- url: https://github.com/NVIDIA-NeMo/Guardrails
  title: NeMo Guardrails repository
  trust: 0.9
- url: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  title: OWASP LLM01:2025 Prompt Injection
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://docs.langchain.com/langsmith
  title: LangSmith documentation
  trust: 0.9
- url: https://mlflow.org/docs/latest/genai/tracing/
  title: MLflow Tracing documentation
  trust: 0.9
- url: https://github.com/Arize-ai/phoenix
  title: Arize Phoenix repository
  trust: 0.9
---

## Overview

A retrieval-augmented generation (RAG) app answers from your documents instead of from what a model memorised. **Indexing** runs offline: parse, chunk, embed, and store chunks in a vector database.

At **query** time the orchestration layer retrieves candidates, reranks them, and passes the best to the generating model. **Quality** blocks check grounding, measure each change, filter unsafe input and output, and trace every request.
