---
id: framework/directml
type: framework
slug: directml
schema_version: 3.0
title: DirectML
status: curated
kind: library
category: framework-category/gpu-programming
subcategory: vendor-api
tagline: A high-performance, hardware-accelerated DirectX 12 library for machine learning.
description: DirectML (Direct Machine Learning) is Microsoft's low-level Windows API for running machine-learning inference on any DirectX 12-compatible GPU. It supplies a library of hardware-accelerated operators, executed one layer at a time or as a graph, behind a single vendor-agnostic C++ interface in the style of DirectX 12. ONNX Runtime and Windows ML can use it as a backend. It shipped with Windows 10 version 1903 and is now in sustained engineering, with new feature work moved to Windows ML.
best_for: Machine-learning inference on any DirectX 12 GPU under Windows
not_ideal_for: New projects that want new features (Microsoft points to Windows ML), or operating systems other than Windows
key_features:
- Hardware-accelerated operators such as convolution, GEMM, LSTM and pooling
- Layer-by-layer and graph-based execution
- Vendor-agnostic interface across AMD, Intel, NVIDIA and Qualcomm GPUs
- Native C++ (nano-COM) API in the style of DirectX 12
- Execution provider for ONNX Runtime
- PyDirectML Python projection
use_cases:
- Inference inside games, engines and rendering pipelines
- Running ONNX models on Windows GPUs from any vendor
- Building custom ML frameworks and middleware on Windows
pros:
- Runs on any DirectX 12-compatible GPU
- Built into Windows 10 version 1903 and later
- Usable indirectly through ONNX Runtime without writing DirectML code
cons:
- In sustained engineering; no new features are planned
- Windows only (PyTorch and TensorFlow support extends to WSL)
- The developer handles resource allocation, memory management and scheduling
languages_supported:
- C++
- Python
maintained_by: Microsoft
license_note: 'DirectML redistributable: Microsoft Software License Terms, Microsoft DirectX Machine Learning (DirectML). GitHub samples repository: MIT'
github_url: https://github.com/microsoft/DirectML
docs_url: https://learn.microsoft.com/en-us/windows/ai/directml/dml
backing:
  type: corporate
  orgs:
  - organization/microsoft
ecosystem_connections:
- framework/onnx-runtime
registry_signals:
  github_stars: 2590
  observed_at: '2026-11-25'
  source: https://github.com/microsoft/DirectML
aliases:
- Direct Machine Learning
- DirectX Machine Learning
- microsoft/DirectML
tags:
- gpu-programming
- windows
- directx
- inference
updated: '2026-11-25'
sources:
- url: https://learn.microsoft.com/en-us/windows/ai/directml/dml
  title: Introduction to DirectML (Microsoft Learn)
- url: https://github.com/microsoft/DirectML
  title: GitHub repository
- url: https://www.nuget.org/packages/Microsoft.AI.DirectML
  title: Microsoft.AI.DirectML — NuGet
- url: https://www.nuget.org/packages/Microsoft.AI.DirectML/1.15.4/License
  title: Microsoft Software License Terms — DirectML
---


