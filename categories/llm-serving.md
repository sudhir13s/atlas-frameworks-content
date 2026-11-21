---
id: framework-category/llm-serving
type: framework-category
slug: llm-serving
schema_version: 2.1
title: Deployment & Serving
label: Deployment & Serving
layer: run
order: 10
short_description: Platforms that package, deploy, scale, and observe models as production services — the layer above the raw engine.
why_it_matters: An inference engine generates tokens; a serving platform turns it into a versioned, autoscaling, observable API.
defacto:
  framework_id: framework/bentoml
  reason: Python library that turns a model inference script into a REST API server using type hints, and builds Docker images for deployment.
rising:
- framework_id: framework/ray-serve
  reason: Framework-agnostic serving built on Ray, suited to model composition and multi-model services, and scaling to many machines.
- framework_id: framework/kserve
  reason: Kubernetes inference platform with request-based autoscaling (scale-to-zero for predictive models), canary rollouts and an OpenAI-compatible protocol.
alternatives:
- framework_id: framework/triton-inference-server
  reason: NVIDIA's open-source server for models from TensorRT, PyTorch, ONNX, OpenVINO and other frameworks, with dynamic batching and concurrent model execution.
- framework_id: framework/seldon-core
  reason: Seldon Core 2 deploys models and pipelines on Kubernetes, with experiments that route traffic between candidates for A/B tests and shadow deployments.
- framework_id: framework/tf-serving
  reason: Serving system for production with out-of-the-box TensorFlow model support, versioned models and canary releases.
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
  url: https://kserve.github.io/website/docs/intro
- title: Ray Serve — documentation
  url: https://docs.ray.io/en/latest/serve/index.html
tags:
- serving
- deployment
- mlops
- kubernetes
updated: '2026-11-21'
sources:
- url: https://github.com/bentoml/BentoML
  title: BentoML repository
  trust: 0.9
- url: https://docs.ray.io/en/latest/serve/index.html
  title: Ray Serve — documentation
  trust: 0.9
- url: https://github.com/kserve/kserve
  title: KServe repository
  trust: 0.9
- url: https://github.com/triton-inference-server/server
  title: Triton Inference Server repository
  trust: 0.9
- url: https://github.com/SeldonIO/seldon-core
  title: Seldon Core repository
  trust: 0.9
- url: https://github.com/tensorflow/serving
  title: TensorFlow Serving repository
  trust: 0.9
---
