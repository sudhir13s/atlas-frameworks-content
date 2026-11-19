---
id: use-case/deploy-on-device
type: use-case
slug: deploy-on-device
schema_version: 1.1
title: Deploy a Model On-Device
label: Deploy on-device
order: 6
goal: Run a model locally on a phone, laptop, or edge board — offline, private, and with no server bill.
languages:
- python
- swift
- kotlin
levels:
- intermediate
- advanced
stack:
- framework_id: framework/onnx-runtime
  role: Cross-platform runtime
  why: One portable model format that runs on CPU, mobile, and browsers with hardware acceleration.
  install: pip install onnxruntime
  quickstart_url: https://onnxruntime.ai/docs/get-started/with-python.html
  docs_url: https://onnxruntime.ai/docs/
- framework_id: framework/llama-cpp
  role: On-device LLM inference
  why: Runs quantized GGUF LLMs efficiently on CPU/Metal/consumer GPUs — even a 7B on a laptop.
  install: pip install llama-cpp-python
  quickstart_url: https://github.com/ggml-org/llama.cpp#quick-start
  docs_url: https://github.com/ggml-org/llama.cpp/tree/master/docs
- framework_id: framework/executorch
  role: PyTorch on edge
  why: PyTorch's on-device runtime for mobile/embedded, exporting straight from a PyTorch model.
  install: pip install executorch
  quickstart_url: https://pytorch.org/executorch/stable/getting-started.html
  docs_url: https://pytorch.org/executorch/
- framework_id: framework/coreml-tools
  role: Apple deployment
  why: Converts models to Core ML so they run on the Apple Neural Engine on iPhone/iPad/Mac.
  install: pip install coremltools
  quickstart_url: https://apple.github.io/coremltools/docs-guides/source/introductory-quickstart.html
  docs_url: https://apple.github.io/coremltools/
day1_plan:
- step: 1
  task: Quantize the model
  estimate: 45 min
  details: Convert to INT8 (or 4-bit GGUF for LLMs). Measure the size and accuracy drop — usually <1% for INT8.
- step: 2
  task: Export to a device format
  estimate: 45 min
  details: Export to ONNX, GGUF, ExecuTorch, or Core ML depending on the target platform.
- step: 3
  task: Run and benchmark locally
  estimate: 45 min
  details: Measure latency, memory, and battery/thermal impact on the actual device, not a simulator.
- step: 4
  task: Integrate into the app
  estimate: 60 min
  details: Load the model with the platform runtime and wire the pre/post-processing on-device.
starter_templates:
- name: llama.cpp
  repo: https://github.com/ggml-org/llama.cpp
  why: Reference on-device LLM runtime with mobile and desktop examples.
- name: ExecuTorch examples
  repo: https://github.com/pytorch/executorch/tree/main/examples
  why: Official demos for running PyTorch models on Android and iOS.
learn_next:
- title: ONNX Runtime — mobile deployment
  url: https://onnxruntime.ai/docs/tutorials/mobile/
  kind: docs
- title: Core ML Tools — quickstart
  url: https://apple.github.io/coremltools/docs-guides/source/introductory-quickstart.html
  kind: docs
- title: llama.cpp — quantization guide
  url: https://github.com/ggml-org/llama.cpp/blob/master/examples/quantize/README.md
  kind: docs
pitfalls:
- 'Benchmarking on a simulator: on-device latency and thermals only show up on real hardware.'
- 'Over-aggressive quantization: 2-bit can wreck quality. Start at INT8 / 4-bit and measure.'
- 'Forgetting pre/post-processing: tokenization and image transforms must run on-device too, not just the model.'
when_to_level_up: When one model format cannot cover all your targets, maintain per-platform exports (Core ML for Apple, ONNX/NNAPI for Android); add on-device delegation to the NPU/GPU for latency-critical paths.
community:
- name: llama.cpp Discussions
  url: https://github.com/ggml-org/llama.cpp/discussions
- name: ONNX Runtime GitHub
  url: https://github.com/microsoft/onnxruntime/discussions
- name: r/LocalLLaMA
  url: https://www.reddit.com/r/LocalLLaMA/
dont_use:
- what: A full-precision model on a phone
  why: It will be too big and too slow. Quantize before you even try to deploy on-device.
- what: A cloud-serving engine (vLLM) on edge
  why: It targets datacenter GPUs; on-device needs a lightweight runtime like ONNX Runtime or llama.cpp.
related_use_cases:
- use-case/serve-in-production
- use-case/build-multimodal-app
tags:
- edge
- mobile
- on-device
- quantization
updated: '2026-11-19'
sources:
- url: https://onnxruntime.ai/docs/
  title: ONNX Runtime documentation
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: llama.cpp
  trust: 0.9
- url: https://apple.github.io/coremltools/
  title: Core ML Tools documentation
  trust: 0.9
---

## Overview

On-device deployment runs the model where the data is — on a phone, laptop, or edge board. That buys
you privacy (nothing leaves the device), offline capability, and zero per-request server cost, at the
price of a tight memory and latency budget.

## Why this stack

ONNX Runtime is the portable baseline: one format across CPU, mobile, and browser. llama.cpp is the
proven path for on-device LLMs via quantized GGUF. ExecuTorch exports PyTorch models to mobile, and
Core ML Tools targets Apple's Neural Engine. Which one you pick is driven by the target platform, not
preference.

## Notes

Quantization is the enabling step — INT8 typically costs under 1% accuracy for a 4x memory saving, and
4-bit makes 7B LLMs run on a laptop. Always benchmark on the real device (thermals and battery do not
show up in a simulator), and remember the pre/post-processing has to run on-device too.
