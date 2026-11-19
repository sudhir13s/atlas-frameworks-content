---
id: framework-category/llm-serving
type: framework-category
slug: llm-serving
schema_version: 1.1
title: Deployment & Serving
label: Deployment & Serving
order: 10
short_description: Platforms that package, deploy, scale, and observe models as production services — the layer above the raw engine.
why_it_matters: An inference engine generates tokens; a serving platform turns it into a versioned, autoscaling, observable API.
defacto:
  framework_id: framework/bentoml
  reason: Packages any model as a versioned, containerizable service with a typed API, autoscaling, and simple deploys.
rising:
- framework_id: framework/ray-serve
  reason: Python-native serving that scales from a laptop to a cluster and composes multi-model pipelines.
- framework_id: framework/kserve
  reason: Kubernetes-native serving with autoscaling (to zero), canary rollout, and standard inference protocols.
alternatives:
- framework_id: framework/triton-inference-server
  reason: NVIDIA's high-performance server for ONNX/TensorRT/PyTorch with dynamic batching.
- framework_id: framework/torchserve
  reason: Straightforward serving for PyTorch models.
- framework_id: framework/seldon-core
  reason: Kubernetes-native serving with advanced routing and explainability.
- framework_id: framework/tf-serving
  reason: The battle-tested server for TensorFlow SavedModels.
key_concepts:
- model packaging
- autoscaling
- canary rollout
- dynamic batching
- observability (p95/p99)
canonical_reading:
- title: BentoML — hello world
  url: https://docs.bentoml.com/en/latest/get-started/hello-world.html
- title: KServe — documentation
  url: https://kserve.github.io/website/latest/
- title: Ray Serve — documentation
  url: https://docs.ray.io/en/latest/serve/index.html
did_you_know:
- Triton started as TensorRT Inference Server before rebranding.
- Cold start is often the silent killer of serverless LLM deployments.
- Continuous batching can 2-5x throughput versus static batching.
tags:
- serving
- deployment
- mlops
- kubernetes
updated: '2026-11-19'
sources:
- url: https://docs.bentoml.com/
  title: BentoML documentation
  trust: 0.9
- url: https://kserve.github.io/website/latest/
  title: KServe documentation
  trust: 0.9
- url: https://docs.ray.io/en/latest/serve/index.html
  title: Ray Serve documentation
  trust: 0.9
---

## Overview

Deployment and serving is the layer above the inference engine: it packages a model as a service,
exposes a stable API, scales with traffic, rolls out safely, and emits the metrics you operate on.
Where an engine like vLLM maximizes tokens per GPU, this layer makes the whole thing a dependable
production endpoint.

## Landscape

BentoML is a strong default for packaging and deploying any model with a typed API. Ray Serve scales
Python-native serving from laptop to cluster and composes multi-model pipelines. KServe is the
Kubernetes-native choice with autoscaling and canary rollout. Triton, TorchServe, Seldon Core, and
TF-Serving cover high-performance, PyTorch, advanced-routing, and TensorFlow niches respectively.

## Notes

Pick based on where you run: standalone/containers → BentoML; Kubernetes → KServe/Seldon; multi-model
Python pipelines → Ray Serve; NVIDIA-heavy mixed models → Triton. Whatever you choose, track p95/p99
(not averages) and budget for cold starts on serverless paths.
