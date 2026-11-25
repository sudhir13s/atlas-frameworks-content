---
id: framework-category/gpu-programming
type: framework-category
slug: gpu-programming
schema_version: 3.0
title: GPU Programming
label: GPU Programming
layer: run
order: 11
short_description: The software layer that lets ML code run on a maker's accelerators — kernel languages, compute stacks and vendor APIs.
why_it_matters: Which accelerators a model can use depends on this layer, since each maker's GPUs are reached through its own stack or through a portable kernel language.
alternatives:
- framework_id: framework/triton
  reason: Python-based language and compiler for custom GPU kernels, running on NVIDIA GPUs and on AMD GPUs through ROCm.
- framework_id: framework/rocm
  reason: AMD's open software stack for its GPUs, built around the HIP C++ runtime and kernel language.
- framework_id: framework/oneapi
  reason: Intel's SYCL-based platform for Intel CPUs and GPUs, reaching NVIDIA and AMD GPUs through Codeplay plug-ins.
- framework_id: framework/directml
  reason: Microsoft's low-level Windows API for ML inference on any DirectX 12 GPU; now in sustained engineering.
key_concepts:
- GPU kernels
- compute stack
- CUDA-like portability (HIP, SYCL)
- vendor-agnostic operator APIs
- compute capability
canonical_reading:
- title: Triton — documentation
  url: https://triton-lang.org/main/index.html
- title: What is ROCm?
  url: https://rocm.docs.amd.com/en/latest/what-is-rocm.html
- title: Intel oneAPI — overview
  url: https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
- title: Introduction to DirectML
  url: https://learn.microsoft.com/en-us/windows/ai/directml/dml
tags:
- gpu-programming
- kernels
- gpu
- accelerators
updated: '2026-11-25'
sources:
- url: https://github.com/triton-lang/triton
  title: Triton repository
  trust: 0.9
- url: https://rocm.docs.amd.com/en/latest/what-is-rocm.html
  title: What is ROCm? (AMD ROCm documentation)
  trust: 0.95
- url: https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html
  title: Intel oneAPI overview
  trust: 0.9
- url: https://www.intel.com/content/www/us/en/developer/articles/system-requirements/oneapi-base-toolkit/2025.html
  title: Intel oneAPI Base Toolkit system requirements
  trust: 0.95
- url: https://learn.microsoft.com/en-us/windows/ai/directml/dml
  title: Introduction to DirectML (Microsoft Learn)
  trust: 0.95
---


