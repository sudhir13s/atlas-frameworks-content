---
id: framework-category/inference
type: framework-category
slug: inference
schema_version: 3.0
title: Inference Engines
label: Inference
layer: run
order: 3
short_description: Runtimes that generate tokens from LLMs efficiently, through request batching, KV-cache management and quantization.
why_it_matters: The engine decides how many requests one GPU can serve at once; the PagedAttention paper reports 2-4x the throughput of earlier serving systems at the same latency.
defacto:
  framework_id: framework/vllm
  reason: Library for LLM inference and serving with PagedAttention memory management, continuous batching and an OpenAI-compatible API server.
rising:
- framework_id: framework/tensorrt-llm
  reason: NVIDIA's library that optimizes LLM inference with specialized kernels and an efficient runtime.
- framework_id: framework/llama-cpp
  reason: LLM inference in C/C++ with minimal setup on a wide range of hardware, locally and in the cloud.
alternatives:
- framework_id: framework/ollama
  reason: Runs open models locally through a command line and a REST API; its README lists llama.cpp as its backend.
- framework_id: framework/onnx-runtime
  reason: Cross-platform model accelerator for models trained in different frameworks, with an interface for hardware-specific libraries.
key_concepts:
- continuous batching
- KV cache
- paged attention
- quantization
- throughput vs latency
canonical_reading:
- title: vLLM — quickstart
  url: https://docs.vllm.ai/en/latest/getting_started/quickstart/
- title: Efficient Memory Management for Large Language Model Serving with PagedAttention
  url: https://arxiv.org/abs/2309.06180
- title: llama.cpp — repository
  url: https://github.com/ggml-org/llama.cpp
tags:
- inference
- serving
- throughput
- quantization
updated: '2026-11-21'
sources:
- url: https://github.com/vllm-project/vllm
  title: vLLM repository
  trust: 0.9
- url: https://arxiv.org/abs/2309.06180
  title: Efficient Memory Management for Large Language Model Serving with PagedAttention
  trust: 0.9
- url: https://github.com/NVIDIA/TensorRT-LLM
  title: TensorRT LLM repository
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp repository
  trust: 0.9
- url: https://github.com/ollama/ollama
  title: Ollama repository
  trust: 0.9
- url: https://onnxruntime.ai/docs/
  title: ONNX Runtime documentation
  trust: 0.9
---


