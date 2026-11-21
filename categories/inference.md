---
id: framework-category/inference
type: framework-category
slug: inference
schema_version: 2.1
title: Inference Engines
label: Inference
layer: run
order: 3
short_description: Runtimes that make LLM generation fast and cheap — batching, KV-cache management, and quantization.
why_it_matters: Inference is where most production cost lives; the engine you choose can change throughput per GPU several-fold.
defacto:
  framework_id: framework/vllm
  reason: PagedAttention plus continuous batching set the throughput bar for open LLMs, with an OpenAI-compatible server.
rising:
- framework_id: framework/tensorrt-llm
  reason: NVIDIA's compiled engine can beat raw vLLM by 1.5-3x on specific models and hardware.
- framework_id: framework/llama-cpp
  reason: The reference for quantized, CPU/edge-friendly inference — a 7B on a laptop or Raspberry Pi.
alternatives:
- framework_id: framework/ollama
  reason: The easiest local runtime; wraps llama.cpp with one-command model management.
- framework_id: framework/onnx-runtime
  reason: Portable, dependency-light runtime for smaller or non-LLM models across hardware.
key_concepts:
- continuous batching
- KV cache
- paged attention
- quantization
- throughput vs latency
canonical_reading:
- title: vLLM — quickstart
  url: https://docs.vllm.ai/en/latest/getting_started/quickstart.html
- title: Efficient Memory Management for LLM Serving with PagedAttention
  url: https://arxiv.org/abs/2309.06180
- title: llama.cpp — repository
  url: https://github.com/ggml-org/llama.cpp
did_you_know:
- vLLM's PagedAttention borrows virtual-memory paging ideas from operating systems.
- TensorRT-LLM can beat raw vLLM on NVIDIA hardware by 1.5-3x on specific models.
- llama.cpp runs 7B models on a Raspberry Pi with 4-bit quantization.
tags:
- inference
- serving
- throughput
- quantization
updated: '2026-11-19'
sources:
- url: https://docs.vllm.ai/
  title: vLLM documentation
  trust: 0.9
- url: https://arxiv.org/abs/2309.06180
  title: Efficient Memory Management for LLM Serving with PagedAttention
  trust: 0.95
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp
  trust: 0.9
---

## Overview

Inference engines execute a trained model efficiently. For LLMs the hard problems are managing the
KV-cache and keeping the GPU busy across many concurrent requests — which is why a purpose-built engine
can dramatically outperform a naive `model.generate()` loop.

## Landscape

vLLM sets the throughput bar with PagedAttention and continuous batching, and its OpenAI-compatible
server drops into existing clients. TensorRT-LLM squeezes out more on NVIDIA hardware at the cost of a
compile step. llama.cpp owns quantized CPU/edge inference, and Ollama wraps it for painless local use.
ONNX Runtime is the portable choice for smaller or non-LLM models.

## Notes

The single biggest lever is continuous batching — never ship static batching for a busy endpoint.
Match the engine to the target: datacenter GPU throughput → vLLM/TensorRT-LLM; local or edge →
llama.cpp/Ollama; small portable models → ONNX Runtime.
