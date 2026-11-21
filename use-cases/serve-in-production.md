---
id: use-case/serve-in-production
type: use-case
slug: serve-in-production
schema_version: 2.0
title: Serve a Model in Production
label: Serve in production
order: 4
goal: Run a trained model behind a versioned, batched and observable API that scales with traffic and can be rolled back.
stages:
- id: build
  name: Package and optimise
  note: Runs once per model version, before deployment.
- id: serve
  name: Request path
  note: Runs on every inference request.
- id: operate
  name: Operations
  note: Runs continuously in production and before each rollout.
blocks:
- id: model-registry
  stage: build
  name: Model registry
  purpose: Stores each model version with its lineage, so a deployment names an exact version and a rollback is a pointer change.
  options:
  - record: framework/mlflow
    choice: default
    when: Apache-2.0 registry with versions, mutable aliases such as a production alias, tags, and links from each version to the run that produced it.
  how_to_choose:
  - Deploy by alias or version, never by a file path that can change underneath.
  - Record the evaluation results with the version they belong to.
  browse:
    label: All MLOps tools
    record: framework-category/mlops
- id: model-optimisation
  stage: build
  name: Model format and optimisation
  purpose: Converts the trained model into a format and precision the serving hardware runs efficiently.
  options:
  - record: framework/onnx-runtime
    choice: default
    when: Runs models exported from PyTorch or TensorFlow to the open ONNX format on many targets, through execution providers for CUDA, TensorRT, OpenVINO, DirectML and Core ML.
  - record: framework/tensorrt-llm
    choice: alternative
    when: Pick it to optimise language models for NVIDIA GPUs with custom kernels, quantized checkpoints and speculative decoding, under Apache-2.0.
  - record: framework/llama-cpp
    choice: alternative
    when: Pick it to run language models with minimal setup on a wide range of hardware, outside a GPU cluster.
  how_to_choose:
  - 'Classic and vision models: export to ONNX; large language models: use the engine''s own format and quantization.'
  - Re-run evaluation after every conversion or quantization step.
  browse:
    label: All inference engines
    record: framework-category/inference
- id: llm-engine
  stage: serve
  name: Language model inference engine
  purpose: Generates tokens for many concurrent requests, batching them and managing GPU memory for the attention cache.
  options:
  - record: framework/vllm
    choice: default
    when: Apache-2.0 engine with PagedAttention, continuous batching, prefix caching and many quantization formats behind an OpenAI-compatible server, on NVIDIA, AMD and Intel GPUs and CPUs.
  - record: framework/sglang
    choice: alternative
    when: Pick it for RadixAttention prefix caching and multi-GPU parallelism on a wide range of accelerators; it is hosted by the non-profit LMSYS.
  - record: framework/tensorrt-llm
    choice: alternative
    when: Pick it on NVIDIA GPUs when you want NVIDIA's optimised kernels and integration with Triton and Dynamo.
  how_to_choose:
  - Expose an OpenAI-compatible API so clients do not change when the engine does.
  - Benchmark engines on your own model, hardware and traffic shape before choosing.
  browse:
    label: All serving tools
    record: framework-category/llm-serving
- id: model-server
  stage: serve
  name: Model server
  purpose: Serves non-generative or mixed models over HTTP or gRPC, batching requests and running several models on shared hardware.
  options:
  - record: framework/triton-inference-server
    choice: default
    when: BSD-3-Clause server that runs TensorRT, PyTorch, ONNX, OpenVINO and Python models with dynamic batching, concurrent model execution, HTTP and gRPC, and GPU, throughput and latency metrics.
  - record: framework/bentoml
    choice: alternative
    when: Pick it to turn a Python inference script into a REST service with type hints, then build a container image, with batching and model composition.
  - record: framework/ray-serve
    choice: alternative
    when: Pick it to compose several models and business logic in Python with autoscaling and fractional GPUs on a Ray cluster.
  how_to_choose:
  - 'Many models from several frameworks on GPUs: Triton.'
  - 'Serving code is mostly Python logic around the model: BentoML or Ray Serve.'
- id: deployment-platform
  stage: serve
  name: Deployment and autoscaling
  purpose: Runs the servers on a cluster, scales replicas with traffic, and shifts traffic gradually between model versions.
  options:
  - record: framework/kserve
    choice: default
    when: Apache-2.0 Cloud Native Computing Foundation (CNCF) incubating project for Kubernetes with request-based autoscaling, scale to zero, canary rollouts and an OpenAI-compatible protocol for generative models.
  - record: framework/seldon-core
    choice: alternative
    when: Pick it for Kubernetes pipelines that stream between components over Kafka; it is distributed under the Business Source License.
  - record: framework/ray-serve
    choice: alternative
    when: Pick it when you already run Ray; it deploys to Kubernetes through a Kubernetes operator.
  how_to_choose:
  - 'Need canary rollouts and scale to zero on KServe: use its serverless installation.'
  - Read Seldon Core's Business Source License before production use.
- id: gateway
  stage: serve
  name: API gateway
  purpose: Puts one endpoint in front of all model deployments with keys, budgets, rate limits and fallbacks.
  options:
  - record: framework/litellm
    choice: default
    when: Self-hosted gateway with one OpenAI-compatible endpoint, per-key budgets and rate limits, load balancing, fallbacks, guardrails and logging to Langfuse, OpenTelemetry or Prometheus.
  how_to_choose:
  - Add a gateway when several teams or several providers share the same models.
- id: guardrails
  stage: serve
  name: Guardrails
  purpose: Filters requests and responses of a generative model for unsafe content before they reach the model or the user.
  options:
  - record: model/llama-guard-4-12b
    choice: default
    when: Classifies prompts and responses, text and images, against the MLCommons hazard taxonomy; released under the Llama 4 Community License.
  - record: framework/nemo-guardrails
    choice: alternative
    when: Pick it for Apache-2.0 programmable input and output rails with jailbreak detection, configured as policy.
  how_to_choose:
  - Run input checks before the model and output checks before the response returns.
  - Count the guard model's latency in the request budget.
  browse:
    label: All safety and guard models
    record: task/safety-and-guard-models
- id: metrics
  stage: operate
  name: Metrics and alerting
  purpose: Collects latency, throughput, error and hardware metrics from every server and alerts when they leave their targets.
  options:
  - name: Prometheus
    url: https://prometheus.io/docs/introduction/overview/
    choice: default
    when: Open-source monitoring and alerting toolkit hosted by the CNCF that pulls time series over HTTP, queries them with PromQL and routes alerts through Alertmanager; vLLM exposes a Prometheus-compatible metrics endpoint.
  how_to_choose:
  - For language models, track time to first token, inter-token latency and attention-cache usage, which vLLM exports.
  - Alert on latency percentiles, not averages.
- id: tracing
  stage: operate
  name: Tracing
  purpose: Follows a single request through gateway, guardrails and model so a slow or wrong response can be traced to its step.
  options:
  - record: framework/langfuse
    choice: default
    when: Open-source platform built on OpenTelemetry with usage and cost tracking, deployable on Kubernetes through Helm.
  - record: framework/mlflow
    choice: alternative
    when: Pick it when MLflow is already your registry; its tracing is OpenTelemetry-compatible and the data stays on your infrastructure.
  - record: framework/arize-phoenix
    choice: alternative
    when: Pick it for self-hosted OpenTelemetry tracing; it is licensed under the Elastic License 2.0.
  how_to_choose:
  - Instrument with OpenTelemetry so traces and metrics share one pipeline.
- id: load-testing
  stage: operate
  name: Load and performance testing
  purpose: Measures latency and capacity under realistic traffic before a rollout, so you know the safe operating range.
  options:
  - record: framework/guidellm
    choice: default
    when: Apache-2.0 tool from the vLLM project that simulates traffic against OpenAI-compatible servers and reports time to first token, inter-token latency and end-to-end latency distributions.
  - name: Locust
    url: https://github.com/locustio/locust
    choice: alternative
    when: Pick it for any HTTP service; user behaviour is written in Python and load can be spread over several machines, under MIT.
  how_to_choose:
  - 'Language model endpoints: GuideLLM; other HTTP endpoints: Locust.'
  - Test with request sizes and arrival patterns taken from real traffic.
- id: regression-tests
  stage: operate
  name: Quality regression tests
  purpose: Checks that a new model version, engine or quantization still answers correctly before it takes traffic.
  options:
  - record: framework/promptfoo
    choice: default
    when: MIT-licensed tool with declarative test configs that run locally and in CI/CD, plus red teaming.
  - record: framework/deepeval
    choice: alternative
    when: Pick it to write the same checks as pytest-style unit tests.
  how_to_choose:
  - Gate every rollout on the same fixed test set.
  - Run the tests against the deployed endpoint, not only the model files.
  browse:
    label: All evaluation tools
    record: framework-category/evaluation
learn_next:
- title: MLflow Model Registry
  url: https://mlflow.org/docs/latest/ml/model-registry/
  kind: docs
- title: vLLM metrics
  url: https://docs.vllm.ai/en/latest/design/metrics.html
  kind: docs
- title: KServe
  url: https://github.com/kserve/kserve
  kind: docs
- title: GuideLLM
  url: https://github.com/vllm-project/guidellm
  kind: docs
related_use_cases:
- use-case/build-a-rag-app
- use-case/build-an-agent
- use-case/build-multimodal-app
tags:
- serving
- inference
- deployment
- kubernetes
- observability
- mlops
updated: '2026-11-21'
sources:
- url: https://mlflow.org/docs/latest/ml/model-registry/
  title: MLflow Model Registry documentation
  trust: 0.9
- url: https://onnxruntime.ai/docs/
  title: ONNX Runtime documentation
  trust: 0.9
- url: https://github.com/NVIDIA/TensorRT-LLM
  title: TensorRT-LLM repository
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp repository
  trust: 0.9
- url: https://github.com/vllm-project/vllm
  title: vLLM repository
  trust: 0.9
- url: https://github.com/sgl-project/sglang
  title: SGLang repository
  trust: 0.9
- url: https://docs.sglang.io/
  title: SGLang documentation
  trust: 0.9
- url: https://github.com/triton-inference-server/server
  title: Triton Inference Server repository
  trust: 0.9
- url: https://github.com/bentoml/BentoML
  title: BentoML repository
  trust: 0.9
- url: https://docs.ray.io/en/latest/serve/index.html
  title: Ray Serve documentation
  trust: 0.9
- url: https://github.com/kserve/kserve
  title: KServe repository
  trust: 0.9
- url: https://github.com/SeldonIO/seldon-core
  title: Seldon Core repository
  trust: 0.9
- url: https://github.com/BerriAI/litellm
  title: LiteLLM repository
  trust: 0.9
- url: https://docs.litellm.ai/docs/simple_proxy
  title: LiteLLM AI Gateway documentation
  trust: 0.9
- url: https://huggingface.co/meta-llama/Llama-Guard-4-12B
  title: meta-llama/Llama-Guard-4-12B model card
  trust: 0.9
- url: https://github.com/NVIDIA-NeMo/Guardrails
  title: NeMo Guardrails repository
  trust: 0.9
- url: https://prometheus.io/docs/introduction/overview/
  title: Prometheus overview
  trust: 0.9
- url: https://docs.vllm.ai/en/latest/design/metrics.html
  title: vLLM metrics design
  trust: 0.9
- url: https://github.com/langfuse/langfuse
  title: Langfuse repository
  trust: 0.9
- url: https://mlflow.org/docs/latest/genai/tracing/
  title: MLflow Tracing documentation
  trust: 0.9
- url: https://github.com/Arize-ai/phoenix
  title: Arize Phoenix repository
  trust: 0.9
- url: https://github.com/vllm-project/guidellm
  title: GuideLLM repository
  trust: 0.9
- url: https://github.com/locustio/locust
  title: Locust repository
  trust: 0.9
- url: https://github.com/promptfoo/promptfoo
  title: promptfoo repository
  trust: 0.9
- url: https://github.com/confident-ai/deepeval
  title: DeepEval repository
  trust: 0.9
---

## Overview

Serving a model in production means a fixed model version behind a stable API. **Package and optimise** blocks register the version and convert it for the target hardware.

The **request path** runs an inference engine or model server on a cluster that autoscales, behind a gateway and guardrails. **Operations** blocks collect metrics and traces, load-test before rollout, and gate each release on regression tests.
