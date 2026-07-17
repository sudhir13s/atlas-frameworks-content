---
id: use-case/serve-in-production
type: use-case
slug: serve-in-production
schema_version: 1.0
title: "Serve a Model in Production"
label: "Serve in production"
order: 4
goal: "Expose a trained model behind a fast, batched, observable HTTP endpoint that scales with traffic."
languages: [python]
levels: [intermediate, advanced]
stack:
  - frameworkId: vllm
    role: "LLM serving engine"
    why: "PagedAttention + continuous batching give the highest throughput per GPU for open LLMs, with an OpenAI-compatible server."
    install: "pip install vllm"
    quickstartUrl: "https://docs.vllm.ai/en/latest/getting_started/quickstart.html"
    docsUrl: "https://docs.vllm.ai/"
  - frameworkId: bentoml
    role: "Packaging + API"
    why: "Wraps the model as a versioned, containerizable service with autoscaling and a typed API."
    install: "pip install bentoml"
    quickstartUrl: "https://docs.bentoml.com/en/latest/get-started/hello-world.html"
    docsUrl: "https://docs.bentoml.com/"
  - frameworkId: triton-inference-server
    role: "Multi-framework serving"
    why: "For non-LLM or mixed models, Triton serves ONNX/TensorRT/PyTorch with dynamic batching on one server."
    install: "docker pull nvcr.io/nvidia/tritonserver"
    quickstartUrl: "https://github.com/triton-inference-server/server/blob/main/docs/getting_started/quickstart.md"
    docsUrl: "https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/"
  - frameworkId: onnx-runtime
    role: "Portable inference"
    why: "Export to ONNX for a dependency-light, cross-hardware runtime when you do not need a full LLM engine."
    install: "pip install onnxruntime"
    quickstartUrl: "https://onnxruntime.ai/docs/get-started/with-python.html"
    docsUrl: "https://onnxruntime.ai/docs/"
day1Plan:
  - step: 1
    task: "Stand up an inference server"
    estimate: "45 min"
    details: "Launch vLLM's OpenAI-compatible server pointed at your model; hit it with a curl request."
  - step: 2
    task: "Package as a service"
    estimate: "60 min"
    details: "Wrap it in a BentoML service with a typed request/response and a health endpoint."
  - step: 3
    task: "Load test and set batching"
    estimate: "45 min"
    details: "Drive concurrent requests; tune max batch size and confirm continuous batching is engaged."
  - step: 4
    task: "Add observability"
    estimate: "30 min"
    details: "Expose latency (p50/p95), throughput, and token counts as metrics; log every request id."
starterTemplates:
  - name: "vLLM examples"
    repo: "https://github.com/vllm-project/vllm/tree/main/examples"
    why: "Official server and offline-inference examples to copy."
  - name: "BentoML gallery"
    repo: "https://github.com/bentoml/BentoML/tree/main/examples"
    why: "End-to-end service examples with Dockerfile and deployment config."
learnNext:
  - title: "Efficient Memory Management for LLM Serving with PagedAttention"
    url: "https://arxiv.org/abs/2309.06180"
    kind: paper
  - title: "vLLM — production server"
    url: "https://docs.vllm.ai/en/latest/serving/openai_compatible_server.html"
    kind: docs
  - title: "BentoML — build and deploy"
    url: "https://docs.bentoml.com/en/latest/get-started/hello-world.html"
    kind: docs
pitfalls:
  - "Static batching: it wastes the GPU. Use continuous batching (vLLM) so requests join in flight."
  - "No p95 SLO: averages hide the tail. Track p95/p99 latency and set a budget."
  - "Cold starts on serverless: a multi-GB model can take minutes to load. Keep a warm replica for latency-sensitive paths."
whenToLevelUp: "When one replica saturates, move to Kubernetes-native serving (KServe/Ray Serve) with autoscaling and canary rollout; add a queue and request-level caching for spiky traffic."
community:
  - name: "vLLM Discord"
    url: "https://discord.gg/vllm-project"
  - name: "BentoML Slack"
    url: "https://l.bentoml.com/join-slack"
  - name: "MLOps Community"
    url: "https://mlops.community/"
dontUse:
  - what: "A raw Flask loop calling model.generate()"
    why: "No batching, no backpressure, no metrics — it falls over under real concurrency."
  - what: "vLLM for tiny non-LLM models"
    why: "It is an LLM engine; a small classifier is better served by ONNX Runtime or Triton."
relatedUseCases: [use-case/fine-tune, use-case/build-an-agent]
tags: [serving, inference, deployment, throughput]
updated: 2026-07-17
sources:
  - { url: "https://docs.vllm.ai/", title: "vLLM documentation", trust: 0.9 }
  - { url: "https://arxiv.org/abs/2309.06180", title: "Efficient Memory Management for LLM Serving with PagedAttention", trust: 0.95 }
  - { url: "https://docs.bentoml.com/", title: "BentoML documentation", trust: 0.85 }
---

## Overview
Serving turns a checkpoint into a service: a fast, batched, observable endpoint that holds up under
concurrent traffic. For open LLMs the throughput problem is dominated by memory management and
batching, which is exactly what a purpose-built engine like vLLM solves.

## Why this stack
vLLM's PagedAttention and continuous batching give the best throughput per GPU, and its
OpenAI-compatible server drops into existing clients. BentoML packages the model as a versioned,
containerizable service with a typed API. Triton covers the mixed/non-LLM case with dynamic batching,
and ONNX Runtime is the lightweight, portable path when you do not need a full LLM engine.

## Notes
Continuous batching is the single biggest throughput lever — never ship static batching. Measure the
tail (p95/p99), not the average, and budget for cold starts if you run serverless. Graduate to
KServe or Ray Serve when a single replica can no longer keep up.
