---
id: framework/rocm
type: framework
slug: rocm
schema_version: 3.0
title: ROCm
status: curated
category: framework-category/gpu-programming
subcategory: compute-stack
tagline: AMD's open software stack for GPU-accelerated computing.
description: ROCm is AMD's open software stack for programming AMD GPUs, from low-level kernels to end-user applications. It is built around HIP, a C++ runtime and kernel language with a CUDA-like interface, and bundles compilers, runtimes, math and deep-learning libraries such as rocBLAS, hipBLASLt and MIOpen, the RCCL communication library, profilers, debuggers and monitoring tools. Deep-learning frameworks such as PyTorch run on top of it. Since ROCm 7.14 it is built and released through TheRock, AMD's open build and release system.
best_for: Running and programming machine-learning workloads on AMD GPUs
not_ideal_for: GPUs from other makers
key_features:
- HIP C++ runtime and kernel language with a CUDA-like interface
- HIPIFY for porting CUDA code to HIP
- Math and compute libraries (rocBLAS, hipBLASLt, MIOpen, Composable Kernel)
- RCCL collective communication library
- Profilers and debuggers (ROCm Compute Profiler, ROCgdb)
- Monitoring tools (AMD SMI, rocminfo)
use_cases:
- Training and inference with PyTorch on AMD GPUs
- Porting CUDA applications to AMD GPUs
- High-performance computing on AMD GPUs
pros:
- Most components are open source
- CUDA-like programming model eases porting
- Tools for Linux and Windows
cons:
- Each component carries its own licence, so redistribution needs a per-component check
- Supports only the AMD GPUs on AMD's compatibility list
languages_supported:
- C++
maintained_by: AMD
license_note: ROCm is licensed per component separately; most components use MIT, others Apache 2.0, NCSA, BSD-2-Clause or GPL, and a few binary components ship under separate licence agreements
github_url: https://github.com/ROCm/TheRock
docs_url: https://rocm.docs.amd.com/
backing:
  type: corporate
  orgs:
  - AMD
alternatives:
- framework/oneapi
- framework/triton
ecosystem_connections:
- framework/pytorch
registry_signals:
  latest_version: 10.2.0
  observed_at: '2026-11-25'
  source: https://rocm.docs.amd.com/en/latest/what-is-rocm.html
aliases:
- AMD ROCm
- ROCm/ROCm
- ROCm/TheRock
tags:
- gpu-programming
- amd
- hip
- gpu
updated: '2026-11-25'
sources:
- url: https://rocm.docs.amd.com/en/latest/what-is-rocm.html
  title: What is ROCm? (AMD ROCm documentation)
- url: https://github.com/ROCm/ROCm
  title: ROCm repository (archived)
- url: https://github.com/ROCm/TheRock
  title: TheRock repository
- url: https://rocm.docs.amd.com/en/latest/about/license.html
  title: ROCm licensing terms
---


