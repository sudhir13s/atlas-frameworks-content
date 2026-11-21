---
id: use-case/deploy-on-device
type: use-case
slug: deploy-on-device
schema_version: 2.0
title: Deploy a Model On-Device
label: Deploy on-device
order: 6
goal: Run a trained model inside an app on a phone, laptop or embedded board, using the device's own CPU, GPU or NPU with no server call.
stages:
- id: prepare
  name: Prepare
  note: Runs on a workstation to choose the model and export it.
- id: optimise
  name: Optimise
  note: Runs on the workstation before each app release to shrink the model for the target chip.
- id: run
  name: Run on device
  note: Runs inside the app on the user's device at every inference.
- id: measure
  name: Measure
  note: Runs on real target devices before each release and after every model change.
blocks:
- id: model
  stage: prepare
  name: Model
  purpose: The trained network that must fit the device's memory, compute and power budget.
  options:
  - record: model/llama-3-2-1b-instruct
    choice: default
    when: Its card targets highly constrained environments such as mobile devices and describes quantized variants designed for ExecuTorch and its Arm CPU backend.
  - record: model/qwen3-0-6b
    choice: alternative
    when: When the licence must be Apache-2.0; one set of weights switches between thinking and non-thinking modes.
  - record: model/gemma-3-1b-it
    choice: alternative
    when: When the target is a laptop or desktop, which its card names; use requires accepting the Gemma terms of use.
  how_to_choose:
  - The model must fit on the device's disk and in its memory next to the app itself.
  - Check whether the maker publishes a quantized variant for your runtime before quantizing yourself.
  - Read the licence; the Llama 3.2 licence is a custom commercial agreement with gated access.
  browse:
    label: All text-generation models
    record: task/text-generation
- id: export
  stage: prepare
  name: Export and conversion
  purpose: Captures the trained model as a graph in the file format the on-device runtime loads.
  options:
  - record: framework/executorch
    choice: default
    when: PyTorch's on-device path; torch.export captures the model and lowering produces a .pte program for a chosen backend, with unsupported operators falling back to CPU.
  - record: framework/coreml-tools
    choice: alternative
    when: When the app ships only on Apple devices; it converts PyTorch and TensorFlow models to the Core ML package format.
  - record: framework/tensorflow-lite
    choice: alternative
    when: LiteRT, the successor built on TensorFlow Lite, converts PyTorch, TensorFlow and JAX models to .tflite for Android, iOS, web, desktop and microcontrollers.
  - record: framework/onnx
    choice: alternative
    when: When one model file must run in several runtimes; an open format with a standard operator set and file format.
  - record: framework/llama-cpp
    choice: alternative
    when: For language models on laptops and phones; convert_hf_to_gguf turns a Hugging Face checkpoint into a GGUF file.
  how_to_choose:
  - Choose the export path by the runtime you will ship, since each path here pairs with one runtime below.
  - A PyTorch model shipped to several platforms points to ExecuTorch; an Apple-only app points to Core ML.
  browse:
    label: All edge and mobile frameworks
    record: framework-category/edge-mobile
- id: quantise
  stage: optimise
  name: Quantisation and compression
  purpose: Lowers weight and activation precision so the model fits device memory and runs on low-precision hardware.
  options:
  - record: framework/executorch
    choice: default
    when: Its quantization flow uses torchao with a quantizer per backend, such as the XNNPACK or Core ML quantizer, so the quantized model matches the chip it is lowered to.
  - record: framework/coreml-tools
    choice: alternative
    when: For Core ML targets; it compresses models with palettization, linear quantization and pruning, separately or combined.
  - record: framework/tensorflow-lite
    choice: alternative
    when: For LiteRT targets; the LiteRT quantizer applies post-training quantization during export.
  - record: framework/llama-cpp
    choice: alternative
    when: For GGUF models; llama-quantize lowers weight precision, and an importance matrix file reduces the accuracy loss.
  - record: framework/onnx-runtime
    choice: alternative
    when: For ONNX models; linear integer quantization, dynamic or static with calibration data, plus block-wise weight-only quantization for MatMul and Gather.
  how_to_choose:
  - Use the quantizer that belongs to your backend; ExecuTorch states the quantizer must match it.
  - Static quantization needs representative calibration inputs, while dynamic quantization computes activation ranges at run time.
  - Measure accuracy after quantizing; llama.cpp reports loss as perplexity or Kullback-Leibler divergence.
- id: runtime
  stage: run
  name: On-device runtime
  purpose: Loads the model file inside the app and runs inference.
  options:
  - record: framework/executorch
    choice: default
    when: A lightweight runtime for Android, iOS, desktop and microcontrollers that runs the .pte program produced at export.
  - record: framework/tensorflow-lite
    choice: alternative
    when: LiteRT runs .tflite models with CPU, GPU and NPU backends, and LiteRT-LM adds the language-model loop with key-value (KV) cache, streaming and tool calling.
  - record: framework/onnx-runtime
    choice: alternative
    when: Runs ONNX models on Android and iOS, and a custom build keeps only the operators your models need.
  - record: framework/llama-cpp
    choice: alternative
    when: For GGUF language models; C/C++ inference with minimal setup and documented Android builds.
  how_to_choose:
  - Keep export and runtime from the same family; .pte with ExecuTorch, .tflite with LiteRT, ONNX with ONNX Runtime, GGUF with llama.cpp.
  - Prefer the runtime whose delegates cover the chips your users own.
  browse:
    label: All edge and mobile frameworks
    record: framework-category/edge-mobile
- id: delegate
  stage: run
  name: Hardware delegate
  purpose: Routes supported operators to the device's NPU, GPU or optimized CPU kernels.
  options:
  - name: XNNPACK
    url: https://github.com/google/XNNPACK
    choice: default
    when: Optimized CPU operators for Arm, x86, WebAssembly and RISC-V used by ExecuTorch, TensorFlow Lite, ONNX Runtime and MediaPipe, so it works on every target and serves as the CPU fallback.
  - record: framework/coreml-tools
    choice: alternative
    when: On Apple devices; Core ML, the format Core ML Tools produces, runs models across the CPU, GPU and Neural Engine.
  - name: Qualcomm AI Engine Direct
    url: https://www.qualcomm.com/developer/software/qualcomm-ai-engine-direct-sdk
    choice: alternative
    when: On Snapdragon Android devices; ExecuTorch's Qualcomm backend uses it to delegate work to the Hexagon NPU and Adreno GPU.
  how_to_choose:
  - Operators a delegate does not support fall back to CPU and can split the model into partitions, so check how much of the graph each delegate takes.
  - ONNX Runtime advises starting with CPU for quantized models and XNNPACK for float models before trying NNAPI or Core ML.
- id: measure
  stage: measure
  name: On-device measurement
  purpose: Measures load time, latency, memory and output accuracy on the actual device.
  options:
  - record: framework/executorch
    choice: default
    when: Its Developer Tools (ETRecord, ETDump, Inspector) give per-operator profiling, delegate timings and a comparison of intermediate outputs between export and runtime.
  - name: Xcode Core ML performance report and Instruments
    url: https://developer.apple.com/videos/play/wwdc2022/10027/
    choice: alternative
    when: On Apple devices; reports load and prediction time and the compute unit each layer ran on, measured on a connected device.
  - name: Android Studio Profiler
    url: https://developer.android.com/studio/profile
    choice: alternative
    when: On Android; profiles CPU, memory and battery use of the app process on a physical or virtual device.
  - record: framework/tensorflow-lite
    choice: alternative
    when: For LiteRT models; benchmark apps and command-line binaries report initialization, warmup and steady-state inference time and memory.
  - record: framework/llama-cpp
    choice: alternative
    when: For GGUF models; llama-bench reports prompt processing and text generation throughput in tokens per second.
  how_to_choose:
  - Measure the release build on the lowest-end device you support.
  - Check output accuracy as well as speed after every quantization or delegate change.
learn_next:
- title: ExecuTorch backends overview
  url: https://docs.pytorch.org/executorch/stable/backends-overview.html
  kind: docs
- title: ExecuTorch quantization overview
  url: https://docs.pytorch.org/executorch/stable/quantization-overview.html
  kind: docs
- title: Optimize your Core ML usage (WWDC22)
  url: https://developer.apple.com/videos/play/wwdc2022/10027/
  kind: video
- title: LiteRT overview
  url: https://developers.google.com/edge/litert
  kind: docs
- title: llama.cpp quantize tool
  url: https://github.com/ggml-org/llama.cpp/blob/master/tools/quantize/README.md
  kind: docs
related_use_cases:
- use-case/fine-tune
- use-case/serve-in-production
tags:
- on-device
- edge
- mobile
- quantization
- executorch
updated: '2026-11-21'
sources:
- url: https://huggingface.co/meta-llama/Llama-3.2-1B-Instruct
  title: meta-llama/Llama-3.2-1B-Instruct, model card
  trust: 0.9
- url: https://huggingface.co/Qwen/Qwen3-0.6B
  title: Qwen/Qwen3-0.6B, model card
  trust: 0.9
- url: https://huggingface.co/google/gemma-3-1b-it
  title: google/gemma-3-1b-it, model card
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/index.html
  title: ExecuTorch documentation
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/using-executorch-export.html
  title: ExecuTorch documentation, model export and lowering
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/backends-overview.html
  title: ExecuTorch documentation, backends overview
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/quantization-overview.html
  title: ExecuTorch documentation, quantization overview
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/devtools-overview.html
  title: ExecuTorch documentation, developer tools
  trust: 0.9
- url: https://docs.pytorch.org/executorch/stable/backends-qualcomm.html
  title: ExecuTorch documentation, Qualcomm backend
  trust: 0.9
- url: https://github.com/pytorch/ao
  title: pytorch/ao, GitHub repository
  trust: 0.85
- url: https://apple.github.io/coremltools/docs-guides/
  title: Core ML Tools guide
  trust: 0.9
- url: https://apple.github.io/coremltools/docs-guides/source/overview-coremltools.html
  title: Core ML Tools overview
  trust: 0.9
- url: https://developers.google.com/edge/litert
  title: LiteRT overview
  trust: 0.9
- url: https://developers.google.com/edge/litert/models/measurement
  title: LiteRT performance measurement
  trust: 0.9
- url: https://onnx.ai/
  title: ONNX
  trust: 0.9
- url: https://onnxruntime.ai/docs/execution-providers/
  title: ONNX Runtime documentation, execution providers
  trust: 0.9
- url: https://onnxruntime.ai/docs/tutorials/mobile/
  title: ONNX Runtime documentation, mobile
  trust: 0.9
- url: https://onnxruntime.ai/docs/performance/model-optimizations/quantization.html
  title: ONNX Runtime documentation, quantization
  trust: 0.9
- url: https://github.com/ggml-org/llama.cpp
  title: ggml-org/llama.cpp, GitHub repository
  trust: 0.85
- url: https://github.com/ggml-org/llama.cpp/blob/master/tools/quantize/README.md
  title: llama.cpp, llama-quantize README
  trust: 0.85
- url: https://github.com/ggml-org/llama.cpp/blob/master/tools/llama-bench/README.md
  title: llama.cpp, llama-bench README
  trust: 0.85
- url: https://github.com/google/XNNPACK
  title: google/XNNPACK, GitHub repository
  trust: 0.85
- url: https://developer.apple.com/videos/play/wwdc2022/10027/
  title: Optimize your Core ML usage, WWDC22
  trust: 0.9
- url: https://developer.android.com/studio/profile
  title: Android Studio, profile your app performance
  trust: 0.9
---

## Overview

On-device deployment runs the model inside the app, so inference needs no network round trip. A workstation picks a small model, exports it to the runtime's format and quantizes it with the quantizer that matches the target backend.

On the device a runtime loads the file and hands supported operators to a hardware delegate, with the CPU as fallback. Every model or delegate change is measured on real devices for latency, memory and output accuracy.
